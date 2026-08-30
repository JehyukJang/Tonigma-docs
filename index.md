# Tonigma Publication Index

This index is the public reference for Tonigma protocol readers, integrators, auditors, and report readers. Project-wide documents are maintained in this repository. Component technical documentation remains in its owning repository and is linked here.

## Project-wide Policy

- Protocol And Policy
  - [Tokamak Private App Channels White Paper](publication/project-wide-policy/whitepaper.md) — architecture, custody, channel policy, privacy model, and security posture.
  - Legal
    - [Terms of Service](publication/project-wide-policy/legal/terms.md) — terms governing access to and use of Tonigma.
    - [Privacy Notice](publication/project-wide-policy/legal/privacy-notice.md) — Service data processing and public blockchain-data boundaries.
- Transparency
  - [Monitoring Packet](publication/project-wide-policy/monitoring/Monitoring-Packet.md) — public monitoring scope, evidence sources, and data-backed packet files.

## Bridge And Channels

- Bridge Reference
  - [Bridge Documentation](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/publication/bridge/index.md) — public bridge documentation hub.
  - [Bridge Gas Assessment](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/publication/bridge/gas-assessment.md) — gas-cost reference for bridge calls.
- Channel Interoperability
  - [Channel Workspace Mirror Protocol](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/publication/private-state/channel-workspace-mirror-protocol.md) — channel-mirroring protocol reference.
- Assurance And Performance
  - [Mainnet Deployment Security Audit](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/publication/audit/mainnet-deploy/audit-for-mainnet-deploy.md) — consolidated deployment audit and current review status.
  - [Bridge Optimization Report](https://github.com/JehyukJang/Tonigma-contracts/blob/main/bridge/docs/publication/optimization-report.md) — bridge gas-optimization report with links to its dated mini-reports.

## Channel Dapps

- Private-State DApp
  - Protocol And Security
    - [Private-State DApp Documentation](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/publication/private-state/index.md) — reading order for the complete DApp documentation set.
    - [Background Theory](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/publication/private-state/background-theory.md)
    - [Contract Specification](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/publication/private-state/contract-spec.md)
    - [Function Constraints](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/publication/private-state/function-constraints.md)
    - [Security Model](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/publication/private-state/security-model.md)

## Tokamak zk-EVM

- QAP Compiler
  - Integration And Release
    - [Consumer Integration](https://github.com/JehyukJang/Tokamak-zk-EVM/blob/main/packages/frontend/qap-compiler/docs/publication/consumer-integration.md)
    - [Generation And Release](https://github.com/JehyukJang/Tokamak-zk-EVM/blob/main/packages/frontend/qap-compiler/docs/publication/subcircuit-library-generation-and-release.md)
  - Security
    - [Merged ALU Security Audit](https://github.com/JehyukJang/Tokamak-zk-EVM/blob/main/packages/frontend/qap-compiler/docs/publication/merged-alu-security-audit.md) — current circuit security audit and historical findings.
- Backend Packages
  - Tokamak zk-SNARK Protocol Design And Security Analysis
    - [An Efficient SNARK for Field-Programmable and RAM Circuits](https://eprint.iacr.org/2024/507) — external research publication describing the Tokamak zk-SNARK protocol shared by backend setup, proving, and verification.
  - Prove
    - Performance
      - [Proving Performance History](https://github.com/JehyukJang/Tokamak-zk-EVM/blob/main/packages/backend/prove/optimization/publication/optimization-report.md) — continuously updated accepted, provisional, and rejected performance history.

## Scope Notes

This index excludes usage guides, command walkthroughs, repository README files, internal development references, implementation notes, planning documents, and dated review snapshots that are superseded by a current public report. Usage guidance belongs in the README of the component that provides the interface.
