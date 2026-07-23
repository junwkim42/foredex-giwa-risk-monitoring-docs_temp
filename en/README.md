# GIWA Ecosystem On-Chain Anomaly Detection System

> A monitoring system designed to support a more trustworthy GIWA ecosystem through the early detection of on-chain anomalies associated with ecosystem projects

This documentation describes an **independent GIWA Sepolia demo project** prepared by ForeDex for submission to the GASOK program. Using a test token and purpose-built demo scenarios, the project presents a workflow for collecting on-chain state, quantifying risk signals, displaying the results on a dashboard, and independently reviewing the underlying evidence in an Explorer.

{% embed url="https://www.youtube.com/watch?v=oz82q8OisM0&autoplay=1&mute=1&loop=1" %}

## Quick Links

- [ForeDex Test Dashboard](https://test.foredex.io/charts/altcoin/giwa-risk-monitoring)
- [RISK Contract — GIWA Sepolia Explorer](https://sepolia-explorer.giwa.io/address/0xa1836f8251eab5704A8Fedc6b64278A70132f578?tab=contract)
- [Official GASOK Program Page](https://giwa.io/gasok)

## What the Demo Presents

- Detection of a discrepancy between the demo-disclosed supply and the on-chain token supply
- Detection of anomalous minting activity by an authorized address
- Detection of a large net outflow from a project-controlled wallet
- Detection of a concentrated sell-off in the `RISK/DWETH` liquidity pool

## Recommended Reading Order

The following sequence is recommended:

1. [Executive Summary](reviewer-summary.md)
2. [System and Data Flow](system-overview.md)
3. [Detection Scenarios](detection-scenarios.md)
4. [Explorer-Based On-Chain Verification](onchain-verification.md)
5. [Limitations and Disclaimer](limitations.md)

> **Demo Notice**
>
> The displayed states and illustrative thresholds are examples created for demonstration on the GIWA Sepolia testnet. A detection signal does not establish illegal conduct, project distress, manipulation, or investment risk, and does not replace a security audit, legal advice, or investment advice.

Prepared by: ForeDex Team

Contact: [support@foredex.io](mailto:support@foredex.io) · [foredex.io](https://foredex.io)

© 2026 ForeDex
