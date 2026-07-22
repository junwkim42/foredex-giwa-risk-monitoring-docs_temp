# Claims and Evidence Register

This register is excluded from GitBook navigation. `verified_at` uses an ISO 8601 date. Dynamic on-chain claims additionally require a block number.

| ID | Claim | Status | Evidence or required action |
|---|---|---|---|
| C01 | ForeDex prepared an independent GIWA Sepolia-based demo for submission to GASOK | approved pre-submission wording | Project context supplied by ForeDex; switch to `submitted` only after submission is confirmed |
| C02 | The RISK demo contract is deployed on GIWA Sepolia | verified 2026-07-22 | Verified non-proxy contract, deployment block `30,911,313`, deployment transaction recorded in Korean and English verification pages |
| C03 | Demo-disclosed supply is 100,000,000 RISK and initial minted supply is 150,000,000 RISK | verified in source 2026-07-22 | `DISCLOSED_SUPPLY`, `ACTUAL_INITIAL_SUPPLY`, and constructor mint; current snapshot supply `253,000,000 RISK` kept separate |
| C04 | The Owner at Block `31,403,117` could perform additional minting | verified 2026-07-22 | `mint(address,uint256) external onlyOwner`, no cap check; `owner()` read at a fixed block because ownership can change |
| C05 | Four anomaly scenarios are represented by the dashboard | verified 2026-07-22 | Dashboard and public API expose outflow, supply, mint, and DEX rules with severity data |
| C06 | A dashboard signal can be traced to on-chain evidence | verified examples 2026-07-22 | WARNING and CRITICAL outflow transactions, a CRITICAL mint transaction, WARNING and CRITICAL DEX transactions, and a state-based CRITICAL supply block are linked |
| C07 | Dashboard base queries poll every 60 seconds and risk events use an event stream | verified in product behavior 2026-07-22 | Publish as refresh mechanism only; not an end-to-end latency guarantee |
| C08 | ForeDex operates an on-chain data platform | company/public claim | ForeDex website and company-provided GASOK material |
| C09 | ForeDex holds Korean Patent No. 10-2987801 | company-provided; external citation pending | Restrict wording to `Stablecoin Depegging Early Detection System` and verify through a public patent source if available |
| C10 | The system may expand to additional GIWA asset types and Wallet-facing risk information | planned | Describe only as future direction or integration potential |
| C11 | The design may support exchange-side project oversight | intended application | Do not imply adoption, approval, or validation by an exchange |
| C12 | No false positives or false negatives | prohibited | Acknowledge both possibilities and document evaluation scope |
| C13 | Production-grade, real-time, or official GIWA service | prohibited until evidenced | Requires measured latency, production scope, and written official authorization |
| C14 | Dashboard figures 27 / 12 / 128 / 142 are operational performance | excluded | Reintroduce only with definitions, time range, and reproducible source |
| C15 | Current demo rule windows, thresholds, exclusions, and project-wallet-only DEX evaluation | verified configuration 2026-07-22 | Public Registry API plus representative Risk Events API payloads; describe as current demo configuration, not a universal policy |

## Verification fields for dynamic evidence

```text
claim_id:
status:
source_url:
verified_at:
chain:
block_number:
contract_or_wallet:
transaction_hashes:
approved_wording_ko:
approved_wording_en:
reviewer:
```
