# Editorial Decisions

This file records decisions that affect claims, evidence, language, and publication. It is intentionally excluded from the GitBook navigation.

## Baseline

- Audience: external GASOK reviewers and technical evaluators
- Publication: public GitBook site
- Language: complete Korean edition plus complete English edition
- Source of truth: Korean
- Tone: professional, concise, evidence-led
- Author: ForeDex Team
- Copyright: © 2026 ForeDex
- Final publication: only after ForeDex approves the GitBook preview

## Relationship wording

Approved wording:

> ForeDex가 GASOK 프로그램 제출을 위해 준비한 GIWA Sepolia 기반 독립 데모 프로젝트입니다.

English equivalent:

> An independent GIWA Sepolia-based demo project prepared by ForeDex for submission to the GASOK program.

Do not use `Powered by Upbit`, `ForeDex × GIWA`, official partner, endorsed, approved, deployed by GIWA, or language that could imply a listing relationship. Revert only if written brand-use or partnership authorization is supplied.

After GASOK submission is confirmed, `prepared for submission` may be changed to `submitted`. This wording change does not authorize partnership or endorsement language.

## Evidence levels

1. **On-chain verified:** reproducible through the GIWA Sepolia explorer or public API.
2. **Product observed:** visible on the ForeDex test dashboard with a capture timestamp.
3. **Demo configuration:** intentionally configured values or thresholds supplied by ForeDex.
4. **Company-provided:** ForeDex capability, roadmap, team, award, or patent context not independently reproduced in the demo.
5. **Planned:** future expansion; never described as currently implemented.

## Claim adjustments

| Supplied statement | Published treatment | Rationale | Revert condition |
|---|---|---|---|
| No known false positives or false negatives | No cases identified within the documented demo review; possibility remains | A limited demo cannot establish zero false positives or false negatives | Publish a defined validation set, method, and results |
| No known limitations | Publish explicit scope and testnet limitations | Testnet, indexing, address coverage, thresholds, and chain reorganization affect interpretation | Not reversible; limitations may be refined with evidence |
| Real-time monitoring | Use continuous or periodic monitoring unless latency is measured | End-to-end latency has not been established | Publish timestamped latency measurements and SLA |
| Exchange-use validation | Use exchange-operations-oriented design or applicability | No external exchange adoption evidence was supplied | Supply an attributable PoC or validation reference |
| Patented anomaly detection | Identify patent no. 10-2987801 and its exact subject; do not extend it to all four demo rules | The patent subject and the GIWA demo rules are not identical | Supply claim-level legal mapping |
| Dashboard counts 27 / 12 / 128 / 142 | Exclude | Calculation, period, and source are not documented | Supply metric definitions and reproducible source |

## Demo interpretation

- The disclosed supply of `100,000,000 RISK`, initial mint of `150,000,000 RISK`, owner-controlled additional mint, project-wallet outflow, supply mismatch, abnormal mint, and low-liquidity `RISK/DWETH` DEX dump are intentionally designed demo conditions.
- Dynamic supply, balances, and transaction counts may change as the demo is exercised. Any screenshot must include `captured_at`, chain, and block.
- Thresholds are examples for demonstration and are not universal security or listing standards.
- A detected signal does not prove intent, misconduct, insolvency, manipulation, or investment risk.

## Images

Only images provided or manually uploaded by ForeDex may be used. No autonomous capture, crop, or annotation of public pages is authorized. Visible placeholders must be replaced or removed before publication.

## Repository lifecycle

Draft work is performed in `junwkim42/foredex-giwa-risk-monitoring-docs_temp`. Transfer or copy to a ForeDex organization repository occurs only after GitBook completion and is outside the current publication step.
