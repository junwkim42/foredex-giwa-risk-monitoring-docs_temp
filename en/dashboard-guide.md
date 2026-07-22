# Dashboard Guide

[Open the ForeDex GIWA Risk Monitoring Test Dashboard](https://test.foredex.io/charts/altcoin/giwa-risk-monitoring)

## Role of the Dashboard

The dashboard connects multiple types of on-chain data at the project level and summarizes changes that meet configured rules in a reviewable form. It provides a starting point for investigation and does not replace raw records in the Explorer.

<!-- IMAGE_PLACEHOLDER:IMG-08 -->
> **Image placeholder IMG-08 — Reading dashboard results**
>
> In the caption, identify each card's input data, the meaning of its status, and the observation time.

## Recommended Review Sequence

1. **Confirm the environment:** Verify the GIWA Sepolia and demo-only labels.
2. **Confirm the targets:** Review the token contract, project-controlled wallet, and DEX pool.
3. **Confirm the criteria:** Review the demo-disclosed supply, illustrative threshold, and time window.
4. **Review observed values:** Examine supply, minting, large net outflow, and swap values.
5. **Review the reason for the status:** Determine which data satisfied the rule condition.
6. **Open the Explorer:** Recheck the evidence through contract, event, and transaction links.

## Meaning of Status Labels

| Label | Meaning |
|---|---|
| NORMAL | The current observation does not meet the configured WARNING or CRITICAL condition |
| WARNING | An illustrative warning threshold has been met, requiring prioritized review |
| CRITICAL | An illustrative upper threshold or max supply condition has been met, requiring high-priority review |
| CONFIRMED | A risk-event record has been finalized against the relevant block and log |

`CONFIRMED` is a system event status. It does not indicate that project misconduct, intent, or actual loss has been confirmed.

## Caution Regarding Dynamic Values

Repeated demo execution can change the supply, wallet balances, swaps, and alert count. Any dashboard value cited in documentation or review materials must include the capture time and reference block. Initial demo configuration values and current on-chain observations must not be treated as identical values.

## What a Status Does Not Establish

- The absence of an alert does not guarantee the absence of risk.
- An alert does not prove intent, criminal conduct, project distress, or investment loss.
- Dashboard priority is valid only within the configured addresses, pools, rules, and illustrative thresholds.
- Indexing and network conditions can cause a delay between the dashboard and the latest block.

## Refresh Method

The dashboard's default data requests use a 60-second refresh interval, while new risk events are configured for delivery through a separate event stream. The 60-second interval is the default dashboard polling interval, not a guaranteed end-to-end detection latency from collection through evaluation and display. Accordingly, this documentation uses `periodic monitoring` and `event stream` rather than `real-time`.

## Verification Snapshot

Reference: `2026-07-22 19:25:15 UTC`, Block `31,403,199`

| Documentation scenario | Dashboard panel | Status |
|---|---|---|
| Large net outflow from a project-controlled wallet | `프로젝트 주요 지갑 순유출` (Project Wallet Net Outflow) | WARNING · CONFIRMED |
| Supply discrepancy | `공급량 비교` (Supply Comparison) | CRITICAL · CONFIRMED |
| Anomalous minting | `전체 민팅량` (Total Minted Supply) | CRITICAL · CONFIRMED |
| Concentrated DEX sell-off in a low-liquidity pool | `DEX SWAP` | WARNING · CONFIRMED |

The table is a snapshot at the time of verification. The latest state must be reviewed on the [test dashboard](https://test.foredex.io/charts/altcoin/giwa-risk-monitoring). A status change does not represent a product-performance trend or actual project risk.

In the project-controlled wallets API from the same verification period (`2026-07-22 19:25:31 UTC`), five wallets were registered, but only one—the Main Treasury—had on-chain activity. The other four were unfunded addresses manually entered in the demo Registry. The Main Treasury held `35,638,000 RISK`, its cumulative external net outflow was `114,362,000 RISK`, and cumulative DEX sales by project-controlled wallets were `112,000 RISK`. These values can change as the demo runs and are not operating-performance metrics.
