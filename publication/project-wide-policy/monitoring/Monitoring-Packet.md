# Monitoring Packet

This document explains how the repository generates the public, data-backed Monitoring Packet files.

The packet generator source is in [Tonigma-contracts](https://github.com/JehyukJang/Tonigma-contracts/blob/main/scripts/monitoring-packet/generate.mjs). It is a read-only script that collects current evidence from the mainnet bridge deployment artifacts, Ethereum RPC, Etherscan, and the configured Google Drive artifact folder.

The external policy model for monitoring, public disclosure boundaries, user-controlled selective disclosure, and channel policy is described in the [White Paper](../whitepaper.md). The generator creates data files that support the white paper's policy statements. The packet may also include manually maintained companion files for narrow audit or exchange-dispute scopes.

## Channel Observer And Workspace Mirror Source

Channel observer and workspace-mirror code is published in
[channel-workspace-mirror](https://github.com/JehyukJang/channel-workspace-mirror). The packet
generator can read Channel-specific endpoint metadata when the bridge deployment supports that
registry, but this document does not enumerate or designate a live endpoint. An observer processes
public Channel state and does not require wallet secrets, spending keys, viewing keys, or private
note plaintext.

## How To Generate

```bash
node scripts/monitoring-packet/generate.mjs
```

Useful options:

```bash
node scripts/monitoring-packet/generate.mjs \
  --chain-id 1 \
  --dapp private-state \
  --channel the-great-first-channel \
  --rpc-url "$MAINNET_RPC_URL" \
  --drive-folder-id "$TOKAMAK_MPC_DRIVE_FOLDER_ID"
```

For final publication regeneration, pass the exact artifact directories that the packet must
represent:

```bash
node scripts/monitoring-packet/generate.mjs \
  --chain-id 1 \
  --dapp private-state \
  --channel the-great-first-channel \
  --bridge-artifact-dir deployment/chain-id-1/bridge/20260511T065651Z \
  --dapp-artifact-dir deployment/chain-id-1/dapps/private-state/20260504T003212Z \
  --rpc-url "$MAINNET_RPC_URL" \
  --drive-folder-id "$TOKAMAK_MPC_DRIVE_FOLDER_ID"
```

When either artifact directory option is omitted, the generator keeps the historical behavior and
selects the latest matching local artifact directory for that side. When an explicit directory is
provided, the generator reads that directory and fails if the required files are not present.

The default public output directory is:

```text
monitoring/data/
```

Passing `--output <dir>` changes only the script's internal validation output directory. The canonical public packet data is published under `monitoring/data/` in this repository.

## Method

The generator performs the following steps:

1. Locates the selected bridge and private-state DApp deployment artifacts for the selected chain.
2. Reads mainnet state through RPC, including channel state, owner state, proxy implementation slots, verifier pointers, root-vector state, and bytecode hashes.
3. Reads Etherscan source verification status, using the API when available and falling back to Etherscan's public contract page status when the API cannot be read.
4. Reads Google Drive artifact metadata from the configured artifact publication folder.
5. Builds ABI-derived event monitoring coverage for the Monitoring Packet checklist.
6. Publishes public packet data to `monitoring/data/` in this repository.

## Public Outputs

These files are intended to be included in the public Monitoring Packet.

| File | Path | Description |
| --- | --- | --- |
| `TPAC-Contract-Addresses.json` | [data/TPAC-Contract-Addresses.json](data/TPAC-Contract-Addresses.json) | Chain ID, canonical TON address, bridge and DApp contract addresses, proxy and implementation addresses, owner/admin information, verifier addresses, deployment anchors, source verification status, ABI references, bytecode hashes, and monitored event checklist coverage. |
| `the-great-first-channel-Policy-Snapshot.json` | [data/the-great-first-channel-Policy-Snapshot.json](data/the-great-first-channel-Policy-Snapshot.json) | Current channel policy snapshot for `the-great-first-channel`, including channel manager, vault, leader/operator, join toll, operation status, managed storage addresses, root-vector hash, workspace mirror URL, Channel observer URL when readable from on-chain metadata, DApp metadata digest, function root, verifier snapshot, and storage-layout source. |
| `Private-State-Observability-Matrix.md` | [data/Private-State-Observability-Matrix.md](data/Private-State-Observability-Matrix.md) | Human-readable matrix mapping each Monitoring Packet event checklist item to the current public event surface, including event names, contract addresses, indexed fields, non-indexed fields, explorer query examples, what the event reveals, what it does not reveal, and exchange monitoring meaning. The matrix includes channel exit refund, burn-address transfer, and Channel Operation Abandonment surfaces when present in the monitored ABI. |
| `Admin-Wallets-and-Upgrade-Policy.md` | [data/Admin-Wallets-and-Upgrade-Policy.md](data/Admin-Wallets-and-Upgrade-Policy.md) | Current owner and proxy-slot state for the monitored mainnet bridge deployment, plus notes that connect the generated data to the white paper's upgrade and channel-immutability policy. |
| `User-Controlled-Evidence-Scope.md` | [data/User-Controlled-Evidence-Scope.md](data/User-Controlled-Evidence-Scope.md) | Manually maintained scope note for exceptional exchange disputes or compliance questions. It defines public data, user-held local wallet facts, the raw evidence bundle, the static investigator filtering step, and which keys or wallet materials should not be submitted. |

## User-Controlled Filtering Tool

The private-state DApp includes a local browser investigator that can be opened with
`private-state-cli investigator` or directly from `packages/apps/private-state/cli/investigator/index.html`.
It is not generated by the Monitoring Packet script. Users can load a local raw evidence ZIP created
by `wallet get-notes --export-evidence`, including retained exited wallet epochs when present,
choose a purpose-first disclosure request, inspect an interactive note-linkage graph, filter by note,
nullifier, transaction, block range, status, available counterparty metadata, or user-provided bridge
transaction context, and export either a narrower user-consent disclosure ZIP or a Markdown
plain-text linkage report.

This tool supports bounded review workflows without giving an observer, workspace mirror, channel
operator, exchange, or other reviewer a viewing key, spending key, wallet secret, or full raw
wallet history by default. Its scope and limitations are documented in
[data/User-Controlled-Evidence-Scope.md](data/User-Controlled-Evidence-Scope.md).

## Notes

Plain Ethereum RPC cannot discover every contract creation block without an indexer. When the generator cannot derive a field from RPC or local artifacts, it records the limitation in the generated JSON instead of silently inventing a value.

Source verification is read through Etherscan. A `partial` source verification status means at least one monitored address was not verified or could not be checked successfully at generation time.
