# Executive Summary

## Problem

Potentially anomalous on-chain activity associated with project operators can add operational burden to exchange-side project oversight and efforts to build confidence in a blockchain ecosystem. Changes in token supply, minting by privileged addresses, movements from core wallets, and DEX sales are individually recorded on a public ledger. Converting those records into operationally useful signals, however, requires multiple data sources to be connected and interpreted in context.

## Proposal

ForeDex connects project-associated addresses with token and DEX data, evaluates configured conditions, and quantifies potential anomalies as reviewable signals. Reviewers are not limited to dashboard output: they can follow each result to the GIWA Sepolia Explorer and inspect contract state, event logs, wallet activity, and individual transactions as supporting evidence.

## Core Messages

1. **Early identification:** Supply, minting, wallet, and DEX changes observed on-chain are converted into signals that an operator can review.
2. **Verifiability:** Each signal is designed to link to publicly available on-chain records.
3. **Scalability:** The project aims to extend the workflow validated with the current RISK demo to GIWA ecosystem projects, tokens, RWAs, stablecoins, and DeFi data.

## Alignment with GASOK Evaluation Criteria

- **Fit with the GIWA chain:** Chain-specific validation using a test token deployed on GIWA Sepolia and the public Explorer
- **Originality:** Quantification of composite risk signals from a project-operations perspective, beyond isolated transaction lookups
- **Feasibility:** An operating test dashboard and four purpose-built demo scenarios
- **Marketability:** A proposed monitoring workflow for exchanges, foundations, and project operators
- **Team capability:** Experience operating an on-chain data platform and, based on ForeDex-provided materials, ownership of a related risk-detection patent
- **Potential for GIWA Wallet integration:** A prospective integration path for alert and project-risk information modules, not a currently implemented function
- **Implementation and technical completeness:** A reproducible review procedure that presents dashboard results together with public on-chain evidence

## Current Scope and Target Scope

The **current scope** consists of a test token and preconfigured demo scenarios on GIWA Sepolia. The **target scope** is periodic monitoring across multiple projects and asset types. The target scope is not presented as a current operating result.

## Results Available for Reviewer Inspection

- The data and conditions evaluated by each rule
- The distinction among the demo-disclosed supply, a configured value, and an on-chain observation
- The procedure for reviewing why a signal was generated
- The boundary between the current implementation and planned expansion
- Interpretation limits, including false positives, false negatives, and testnet constraints

Source: [GASOK Program and Evaluation Criteria](https://giwa.io/gasok)
