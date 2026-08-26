# Tonigma Publication Index

This index is the public entry point for Tonigma users, integrators, auditors, and report readers. Project-wide documents are maintained in this repository. Component documentation remains in its owning repository and is linked here.

## Project-Wide Documentation

- [Tokamak Private App Channels White Paper](whitepaper.md) — architecture, custody, channel policy, privacy model, and security posture.
- [Terms of Service](legal/terms.md) — terms governing access to and use of Tonigma.
- [Privacy Notice](legal/privacy-notice.md) — Service data processing and public blockchain-data boundaries.
- [Monitoring Packet](monitoring/Monitoring-Packet.md) — public monitoring scope, evidence sources, and data-backed packet files.

## Bridge And Private-State DApp

- [Bridge Documentation](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/bridge/index.md) — public bridge documentation hub.
- [Bridge Gas Assessment](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/bridge/gas-assessment.md) — gas-cost reference for bridge calls.
- [Private-State DApp Documentation](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/dapps/private-state/index.md) — public reading order for the protocol, contract specification, function constraints, security model, workflow, and channel workspace mirror protocol.
- [Private-State Background Theory](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/dapps/private-state/background-theory.md)
- [Private-State Contract Specification](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/dapps/private-state/contract-spec.md)
- [Private-State Function Constraints](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/dapps/private-state/function-constraints.md)
- [Private-State Security Model](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/dapps/private-state/security-model.md)
- [Private-State Workflow](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/dapps/private-state/workflow.md)
- [Channel Workspace Mirror Protocol](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/dapps/private-state/channel-workspace-mirror-protocol.md)

## Security, Monitoring, And Audit Reports

- [Mainnet Deployment Security Audit](https://github.com/JehyukJang/Tonigma-contracts/blob/main/docs/audit/mainnet-deploy/audit-for-mainnet-deploy.md) — consolidated deployment audit and current review status.
- [Merged ALU Security Audit](https://github.com/JehyukJang/Tokamak-zk-EVM/blob/main/packages/frontend/qap-compiler/docs/merged-alu-security-audit.md) — current circuit security audit and historical findings.

## Tokamak zk-EVM Technical Documentation

- [Version Rules](https://github.com/JehyukJang/Tokamak-zk-EVM/blob/main/docs/version-rules.md) — public package and compatibility versioning rules.
- [Subcircuit Library Consumer Integration](https://github.com/JehyukJang/Tokamak-zk-EVM/blob/main/packages/frontend/qap-compiler/docs/consumer-integration.md) — how supported consumers use the generated subcircuit library.
- [Subcircuit Library Generation and Release](https://github.com/JehyukJang/Tokamak-zk-EVM/blob/main/packages/frontend/qap-compiler/docs/subcircuit-library-generation-and-release.md) — relationship between the generation workflow and the published library package.
- [Verify-WASM NPM Usage](https://github.com/JehyukJang/Tokamak-zk-EVM/blob/main/packages/backend/verify/verify-wasm/NPM_USAGE.md) — historical reference for deprecated WASM verifier packages.
- [Verify-WASM Quick Start](https://github.com/JehyukJang/Tokamak-zk-EVM/blob/main/packages/backend/verify/verify-wasm/QUICK_START.md) — historical quick-start reference for deprecated WASM verifier packages.

## Optimization And Performance Reports

- [Bridge Optimization Report](https://github.com/JehyukJang/Tonigma-contracts/blob/main/bridge/docs/optimization/optimization_report.md) — bridge gas-optimization report with links to its dated mini-reports.
- [GPU Prove Optimization Summary](https://github.com/JehyukJang/Tokamak-zk-EVM/blob/main/packages/backend/prove/optimization/mini-reports/2026-04-30_gpu-prove-optimization-summary.md) — CUDA proving optimization measurements and conclusions.
- [Prove Optimization Mini-Reports](https://github.com/JehyukJang/Tokamak-zk-EVM/tree/main/packages/backend/prove/optimization/mini-reports) — dated proving optimization reports.
- [Current CPU Prove Timing Report](https://github.com/JehyukJang/Tokamak-zk-EVM/blob/main/packages/backend/prove/optimization/timing.local.cpu.current.md)
- [Remote CUDA Prove Timing Report](https://github.com/JehyukJang/Tokamak-zk-EVM/blob/main/packages/backend/prove/optimization/timing.remote.no-output-optimize-size.repeat.cuda.md)
- [TokamakL2JS Optimization Report](https://github.com/JehyukJang/TokamakL2JS/blob/main/docs/optimization_report.md) — optimization results for Tokamak L2 state-manager initialization.

## Scope Notes

This index excludes documents explicitly maintained as internal development references, implementation notes, planning documents, and dated review snapshots that are superseded by a current public report. It also excludes repository README files from the technical-documentation list.
