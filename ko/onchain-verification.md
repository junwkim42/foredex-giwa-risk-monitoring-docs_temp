# Explorer 기반 온체인 검증


## 기준 컨트랙트

- 주소: [`0xa1836f8251eab5704A8Fedc6b64278A70132f578`](https://sepolia-explorer.giwa.io/address/0xa1836f8251eab5704A8Fedc6b64278A70132f578?tab=contract)
- 네트워크: GIWA Sepolia
- 토큰: `Unified Risk Example` (`RISK`), 소수점 18자리(decimals)
- 컨트랙트: 검증됨, 프록시 비사용(non-proxy), Solidity `0.8.28`
- 배포: Block `30,911,313` · [배포 트랜잭션](https://sepolia-explorer.giwa.io/tx/0x3bd540b53ff1efa21b01539607b18e9f0b19a5484a0149288ca1603b48bf7a60) · `2026-07-17 02:47:09 UTC`
- Owner·Treasury 스냅샷: Block `31,403,117`의 [`0x8Bc3dF18Bf41aB83eda4919e9BD92905a79BB443`](https://sepolia-explorer.giwa.io/address/0x8Bc3dF18Bf41aB83eda4919e9BD92905a79BB443)


![](assets/08.png)

> [[GIWA Sepholia Contract Link](https://sepolia-explorer.giwa.io/address/0xa1836f8251eab5704A8Fedc6b64278A70132f578?tab=contract)]

## 등록된 데모 프로젝트 지갑

| 역할 | 주소 | 2026-07-22 검증 상태 |
|---|---|---|
| Main Treasury · Owner · Minter · Seller · Liquidity Provider | [`0x8Bc3dF18Bf41aB83eda4919e9BD92905a79BB443`](https://sepolia-explorer.giwa.io/address/0x8Bc3dF18Bf41aB83eda4919e9BD92905a79BB443) | `ACTIVE_ONCHAIN` |
| Operations | [`0x6c53ceada39479cedd809dee33ccd8ba8ecfb500`](https://sepolia-explorer.giwa.io/address/0x6c53ceada39479cedd809dee33ccd8ba8ecfb500) | `CREATED_UNFUNDED` |
| Vesting | [`0x9e9be4e495784fd2a78ff9e50a80eca798b9f853`](https://sepolia-explorer.giwa.io/address/0x9e9be4e495784fd2a78ff9e50a80eca798b9f853) | `CREATED_UNFUNDED` |
| Liquidity | [`0xea84b0fa67e56289702debd942245f9c215e200b`](https://sepolia-explorer.giwa.io/address/0xea84b0fa67e56289702debd942245f9c215e200b) | `CREATED_UNFUNDED` |
| Marketing | [`0x39574ea1483e6a057bf2febc9b94b256da6b037`](https://sepolia-explorer.giwa.io/address/0x39574ea1483e6a057bf2febc9b94b256da6b037) | `CREATED_UNFUNDED` |

5개 주소는 탐지 범위를 설명하는 데모 Registry입니다. 검증 시점에 실제 온체인 활동이 확인된 주소는 Main Treasury 1개이며, 다른 네 주소를 활성 운영 지갑으로 표현하지 않습니다.

## 대표 거래와 상태 근거

아래 거래는 공개 API의 위험 이벤트와 GIWA Sepolia Explorer의 성공 거래를 대조한 데모 예시입니다.

| 규칙 | 등급 | 검증 가능한 예시 |
|---|---|---|
| 프로젝트 지갑 순유출 | WARNING | Block `31,358,156` · [`0xce0b00e39b060770647b0a609080c678e3329e0b49dbbcfce63f23027c97eb53`](https://sepolia-explorer.giwa.io/tx/0xce0b00e39b060770647b0a609080c678e3329e0b49dbbcfce63f23027c97eb53) — `4,000,000 RISK`, 시작 잔액 대비 약 `10.08%` |
| 프로젝트 지갑 순유출 | CRITICAL | Block `31,355,127` · [`0xb5b5205e97fb4f8bbbb572990aa814dd59ceea5554cc3b199200e93041ffd38e`](https://sepolia-explorer.giwa.io/tx/0xb5b5205e97fb4f8bbbb572990aa814dd59ceea5554cc3b199200e93041ffd38e) — `20,000,000 RISK`, 시작 잔액 대비 약 `33.50%` |
| 비정상 민팅 | CRITICAL | Block `31,355,139` · [`0x0a4fb68a0c110c103a7827991c51c93b9067626660e414af07688fa8316abdb6`](https://sepolia-explorer.giwa.io/tx/0x0a4fb68a0c110c103a7827991c51c93b9067626660e414af07688fa8316abdb6) — `50,000,000 RISK` 추가 민팅, 공시량의 `50%`·민팅 직전 총공급량 대비 `25%` |
| DEX 집중 매도 | WARNING | Block `31,358,222` · [`0x1ec593d2c8585a5c381b998384be32c5c602509ded888915e26f13a9f4c942a7`](https://sepolia-explorer.giwa.io/tx/0x1ec593d2c8585a5c381b998384be32c5c602509ded888915e26f13a9f4c942a7) — `12,000 RISK`, 가격 하락 약 `10.98%`, 관측 시작 RISK 준비금 대비 매도 비율 `6%` |
| DEX 집중 매도 | CRITICAL | Block `31,355,168` · [`0xb8578423633cc4df4149e9d46a367f3aa04557f65336f7e36b68cf71bd0ca536`](https://sepolia-explorer.giwa.io/tx/0xb8578423633cc4df4149e9d46a367f3aa04557f65336f7e36b68cf71bd0ca536) — `50,000 RISK`, 가격 하락 약 `43.70%`, 관측 시작 RISK 준비금 대비 매도 비율 약 `33.33%` |
| 공급량 불일치 | CRITICAL | 상태 기반 이벤트이므로 단일 거래가 아닌 [Block `31,358,185`](https://sepolia-explorer.giwa.io/block/31358185)의 공급량 상태를 기준으로 확인 |

각 비율은 당시 이벤트 평가 데이터입니다. 현재 잔액·reserve·가격 또는 총공급량으로 재계산한 값과 다를 수 있습니다.
