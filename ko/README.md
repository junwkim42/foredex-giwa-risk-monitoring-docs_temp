# GIWA 생태계 온체인 이상 징후 탐지 시스템

> 프로젝트의 온체인 이상 징후를 조기에 탐지하여 신뢰할 수 있는 GIWA 생태계 조성에 기여하는 모니터링 시스템

이 문서는 ForeDex가 GASOK 프로그램 제출을 위해 준비한 **GIWA Sepolia 기반 독립 데모 프로젝트**를 설명합니다. 테스트 토큰과 의도적으로 설계한 데모 시나리오(purpose-built demo scenario)를 이용해 온체인 이상 징후 탐지(on-chain anomaly detection), 위험 신호 정량화와 Explorer 재검증이 연결되는 흐름을 제시합니다.

{% embed url="https://www.youtube.com/watch?v=oz82q8OisM0&autoplay=1&mute=1&loop=1" %}

## 바로 확인하기

- [ForeDex 테스트 대시보드](https://test.foredex.io/charts/altcoin/giwa-risk-monitoring)
- [RISK 컨트랙트 — GIWA Sepolia Explorer](https://sepolia-explorer.giwa.io/address/0xa1836f8251eab5704A8Fedc6b64278A70132f578?tab=contract)
- [GASOK 공식 안내](https://giwa.io/gasok)

## 데모가 보여주는 것

- 공시된 공급량과 온체인 공급량의 불일치 식별
- 권한 있는 주소의 추가 민팅 활동 식별
- 프로젝트 지갑(project-controlled wallet)의 대규모 순유출 신호 식별
- `RISK/DWETH` 유동성풀에서의 집중 매도 신호 식별

## 문서 읽는 순서

다음 순서를 권장합니다.

1. [핵심 요약](reviewer-summary.md)
2. [시스템 및 데이터 흐름](system-overview.md)
3. [탐지 시나리오](detection-scenarios.md)
4. [Explorer 기반 온체인 검증](onchain-verification.md)
5. [한계 및 면책](limitations.md)

> **데모 고지**
>
> 표시된 상태와 임계값은 GIWA Sepolia 테스트넷에서 시연하기 위한 예시입니다. 탐지 신호는 특정 프로젝트의 위법행위·부실·조작 또는 투자 위험을 확정하지 않으며, 보안 감사·법률 자문·투자 조언을 대체하지 않습니다.

작성: ForeDex Team

문의: [support@foredex.io](mailto:support@foredex.io) · [foredex.io](https://foredex.io)

© 2026 ForeDex
