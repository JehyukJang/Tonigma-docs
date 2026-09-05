# Tonigma Privacy And Disclosure System Policy

## Audience And Purpose

This policy is for protocol readers, integrators, auditors, and users who need to understand the privacy properties of Tonigma and the technical boundaries of selective disclosure.

Tonigma is developed by Tokamak Network. Its source code is published as open source, executable builds are publicly available, and its Ethereum smart contracts are publicly deployed. This policy describes the system's technical data boundaries; it does not describe a hosted application as a single system-wide endpoint.

## System Model

Tonigma uses Ethereum for contract execution, settlement, custody, and public verification. Ethereum nodes execute the deployed contracts and replicate their public state.

The private-state DApp uses channel-local state, proof-backed transitions, and user-held secret material. A public contract state does not, by itself, reconstruct Private Note plaintext or every internal sender-recipient relationship. This property does not make all activity secret: public transactions, timing, amounts, metadata, endpoint behavior, user disclosures, device compromise, and external systems can reveal information.

## Public Records

Ethereum transactions and public Channel records can expose Ethereum accounts, contract addresses, token amounts, transaction hashes, block numbers, timestamps, gas-paying accounts, Bridge deposits and withdrawals, Channel joins, registrations, note commitments, nullifiers, encrypted note-delivery events, accepted transitions, and root updates.

Anyone can read, copy, index, analyze, and retain these public records. A Channel observer may derive and display public state from these records, but it cannot derive user-held secret material from the public chain alone.

## User-Held Material

Users control their own Ethereum accounts, private keys, seed phrases, wallet secrets, spending keys, viewing keys, source files, backup files, Private Note plaintext, local evidence exports, and local workspace data.

Loss of every required copy of user-held material prevents the associated recovery or disclosure action. Neither deployed contracts nor the public chain reconstruct lost secrets or local plaintext.

## Selective Disclosure

Selective disclosure is a user-controlled process. A user may create a bounded evidence export from local material for a chosen purpose and disclose only the facts needed for that purpose.

Selective disclosure does not make public-chain records private, erase third-party copies, guarantee a recipient's interpretation, or prove facts not present in the selected evidence. A viewing key, spending key, wallet secret, or full local history is not required for the ordinary public monitoring surfaces described by the Monitoring Packet.

## Disclosure Boundaries

The system separates the following surfaces:

- **Public chain and Channel state:** observable by any participant that reads Ethereum or an index built from it.
- **Local workspace state:** held on the user's device and controlled by the user.
- **User-selected disclosure material:** exported from local material for a stated, bounded purpose.
- **Observer and workspace-mirror code:** open-source components that can read public state or publish recovery-related data without receiving a user's wallet secrets, spending keys, viewing keys, or Private Note plaintext.

The source for both the Channel observer and the workspace mirror is [channel-workspace-mirror](https://github.com/JehyukJang/channel-workspace-mirror). This document does not designate a system-wide observer or workspace-mirror endpoint. Channel metadata may contain component endpoints for a particular Channel; those values are Channel-specific and are not a Tonigma-wide default.

## External Technical Surfaces

Wallets, browsers, RPC providers, package registries, code hosts, artifact stores, explorers, analytics products, and hosting platforms are independent technical surfaces. Their clients and platforms can observe request metadata or public blockchain data according to their own designs.

Users select their wallet, RPC endpoint, software distribution source, and device environment. Before sending a transaction or sharing a disclosure bundle, users should inspect the selected component and the data it will receive.

## Monitoring And Evidence

The [Monitoring Packet](monitoring/Monitoring-Packet.md) describes public evidence sources, packet generation, and the limits of public observation. It does not replace local evidence when a user needs to demonstrate a fact that exists only in user-held material.

The [Tonigma White Paper](whitepaper.md) describes the system architecture, custody boundaries, channel model, privacy model, and security posture.
