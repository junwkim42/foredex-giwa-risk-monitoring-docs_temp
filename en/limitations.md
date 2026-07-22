# Limitations and Disclaimer

## Demo Scope

This documentation describes a ForeDex demo conducted on the GIWA Sepolia testnet. The test token, project-controlled wallet, DEX pool, supply baseline, and illustrative thresholds are configured examples for presenting the detection workflow. They are not an assessment of a real project or a production operating result.

## Principal Limitations

- **Testnet:** Service delays, errors, interruptions, chain reorganizations, rollbacks, and data resets may occur.
- **Rule coverage:** Activity outside the configured addresses, tokens, DEX pools, time windows, and illustrative thresholds may not be detected.
- **Address attribution:** Project-related address and entity labels may be incomplete or may change.
- **Data latency:** Node, indexer, API, and dashboard refresh times may differ.
- **DEX routes:** Unregistered pools, Routers, aggregators, or bridge routes may fall outside the analysis scope.
- **Disclosure baseline:** Legitimate activity may appear as a discrepancy if the supply definition or reference date is unclear.
- **False positives and false negatives:** Even if none have been identified during the documented demo review, the limited scenarios do not support a conclusion that false positives or false negatives cannot occur.
- **Thresholds:** Thresholds presented in the documentation are illustrative and must be calibrated for each project's token structure, liquidity, and operating policy.

## Decision Boundary

A detection signal identifies a data condition requiring further review. It does not determine any of the following:

- Illegal conduct or breach of contract
- Insider trading, market manipulation, or a rug pull
- Project solvency or operational soundness
- Digital-asset value or the likelihood of investment loss
- A decision concerning trading support, listing, or delisting

## Disclaimer

Displayed states and illustrative thresholds are examples created for demonstration. They do not establish illegal conduct, project distress, or investment risk involving a particular project. The system does not replace a security audit, legal advice, or investment advice. Independent technical, legal, and operational review, including inspection of raw on-chain data, is required.

Reference: [GIWA Testnet Terms of Use](https://docs.giwa.io/terms-and-policies/testnet-terms-of-use)
