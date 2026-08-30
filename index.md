# Tonigma Publication Index

This index is the public reference for Tonigma protocol readers, integrators, auditors, and report readers. Project-wide documents are maintained in this repository. Component technical documentation remains in its owning repository and is linked here.

## Project-Wide Documentation

- Protocol And Policy
  - [Tokamak Private App Channels White Paper](whitepaper.md) — architecture, custody, channel policy, privacy model, and security posture.
  - Legal
    - [Terms of Service](legal/terms.md) — terms governing access to and use of Tonigma.
    - [Privacy Notice](legal/privacy-notice.md) — Service data processing and public blockchain-data boundaries.
- Transparency
  - [Monitoring Packet](monitoring/Monitoring-Packet.md) — public monitoring scope, evidence sources, and data-backed packet files.

## Protocol Reference

- Bridge
  - [Bridge Documentation](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/bridge/index.md) — public bridge documentation hub.
  - [Bridge Gas Assessment](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/bridge/gas-assessment.md) — gas-cost reference for bridge calls.
- Private-State DApp
  - [Private-State DApp Documentation](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/dapps/private-state/index.md) — reading order for the complete DApp documentation set.
  - Protocol And Security
    - [Background Theory](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/dapps/private-state/background-theory.md)
    - [Contract Specification](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/dapps/private-state/contract-spec.md)
    - [Function Constraints](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/dapps/private-state/function-constraints.md)
    - [Security Model](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/dapps/private-state/security-model.md)
  - Interoperability
    - [Channel Workspace Mirror Protocol](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/dapps/private-state/channel-workspace-mirror-protocol.md)

## Engineering Documentation

- Tokamak zk-EVM
  - [Version Rules](https://github.com/JehyukJang/Tokamak-zk-EVM/blob/main/docs/version-rules.md) — public package and compatibility versioning rules.
  - QAP Compiler And Subcircuit Library
    - [Consumer Integration](https://github.com/JehyukJang/Tokamak-zk-EVM/blob/main/packages/frontend/qap-compiler/docs/consumer-integration.md)
    - [Generation And Release](https://github.com/JehyukJang/Tokamak-zk-EVM/blob/main/packages/frontend/qap-compiler/docs/subcircuit-library-generation-and-release.md)
## Assurance And Performance Reports

- Security Audits
  - [Mainnet Deployment Security Audit](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/audit/mainnet-deploy/audit-for-mainnet-deploy.md) — consolidated deployment audit and current review status.
  - [Merged ALU Security Audit](https://github.com/JehyukJang/Tokamak-zk-EVM/blob/main/packages/frontend/qap-compiler/docs/merged-alu-security-audit.md) — current circuit security audit and historical findings.
- Optimization And Performance
  - Bridge
    - [Bridge Optimization Report](https://github.com/JehyukJang/Tonigma-contracts/blob/main/bridge/docs/optimization/optimization_report.md) — bridge gas-optimization report with links to its dated mini-reports.
  - Proving
    - [Proving Performance History](https://github.com/JehyukJang/Tokamak-zk-EVM/blob/main/packages/backend/prove/optimization/optimization-report.md) — continuously updated accepted, provisional, and rejected performance history.

## Scope Notes

This index excludes usage guides, command walkthroughs, repository README files, internal development references, implementation notes, planning documents, and dated review snapshots that are superseded by a current public report. Usage guidance belongs in the README of the component that provides the interface.
