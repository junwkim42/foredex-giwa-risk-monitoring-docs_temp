# GIWA Sepolia 데모 환경

## 데모 목적

실제 프로젝트에 대한 위험 판정을 주장하는 대신, 통제된 테스트 환경에서 온체인 이상 조건을 의도적으로 만들고 데이터 수집·규칙 평가·화면 표시·Explorer 검증이 연결되는지를 설명합니다.

## 기본 구성

- **네트워크:** GIWA Sepolia 테스트넷, Chain ID `91342`
- **테스트 토큰:** `Unified Risk Example` (`RISK`), 소수점 18자리(decimals)
- **토큰 컨트랙트:** [`0xa1836f8251eab5704A8Fedc6b64278A70132f578`](https://sepolia-explorer.giwa.io/address/0xa1836f8251eab5704A8Fedc6b64278A70132f578?tab=contract), 검증된 프록시 비사용(non-proxy) 컨트랙트
- **공시 공급량 기준:** `100,000,000 RISK` — 데모 비교 기준
- **최초 민팅 시나리오:** `150,000,000 RISK` — 공급량 불일치를 만들기 위한 설정
- **추가 민팅:** `mint(address,uint256)`가 `onlyOwner`로 제한되며 온체인 발행 상한(cap)은 없음
- **Owner·Treasury 스냅샷:** Block `31,403,117`의 `owner()`·`treasury()`: [`0x8Bc3dF18Bf41aB83eda4919e9BD92905a79BB443`](https://sepolia-explorer.giwa.io/address/0x8Bc3dF18Bf41aB83eda4919e9BD92905a79BB443)
- **DEX 환경:** 의도적으로 저유동성으로 구성한 Demo V2 `RISK/DWETH` 풀

![GIWA Risk Monitoring 대시보드 데모](assets/03.png)

## 공급량 수치의 해석

`100,000,000 RISK`는 데모에서 공시값 역할을 하는 비교 기준이고, `150,000,000 RISK`는 의도적으로 불일치를 만들기 위한 최초 민팅 설정입니다. 검증된 소스 코드에는 두 값이 각각 `DISCLOSED_SUPPLY`, `ACTUAL_INITIAL_SUPPLY` 상수로 선언되어 있고, 생성자(constructor)가 최초 `150,000,000 RISK`를 민팅합니다.

`2026-07-22 19:25:15 UTC`(Block `31,403,199`) 검증 스냅샷의 온체인 총공급량은 추가 민팅을 포함해 `253,000,000 RISK`였습니다. 따라서 아래 세 값을 구분해야 합니다.

- **`100,000,000 RISK`:** 모니터링에 등록한 데모 공시 공급량·설정상 최대 공급량(max supply)
- **`150,000,000 RISK`:** 배포 시점의 최초 민팅량
- **`253,000,000 RISK`:** 2026-07-22 19:25:15 UTC, Block `31,403,199` 스냅샷의 총공급량

대시보드의 `100,000,000 RISK` 최대 공급량(max supply)은 모니터링 설정값이며 컨트랙트가 강제하는 발행 상한이 아닙니다. `2026-07-22 19:23:53 UTC`, Block `31,403,117`에서 확인한 Owner는 `onlyOwner` 민팅 함수를 실행할 수 있었습니다. Owner 상태는 이후 변경될 수 있습니다.

## 공개 Demo DEX 구성

- **Demo V2 Pool:** [`0x1c75c9984b2e43a8606FdD6d7946c02532a80CB1`](https://sepolia-explorer.giwa.io/address/0x1c75c9984b2e43a8606FdD6d7946c02532a80CB1)
- **Demo V2 Router:** [`0x0f6c248912D555878f6ea9F1272D4a9b28549349`](https://sepolia-explorer.giwa.io/address/0x0f6c248912D555878f6ea9F1272D4a9b28549349)
- **Demo V2 Factory:** [`0xA7b4E8A3eC9CeeEAaF1F03e19C2c85D31a082565`](https://sepolia-explorer.giwa.io/address/0xA7b4E8A3eC9CeeEAaF1F03e19C2c85D31a082565)
- **Demo Wrapped Ether (`DWETH`):** [`0x4A954C249a462c028247F292652daf94db1bab9f`](https://sepolia-explorer.giwa.io/address/0x4A954C249a462c028247F292652daf94db1bab9f)


## 테스트 토큰

GIWA Sepolia의 테스트 토큰은 경제적 가치가 없는 개발·검증용 자산입니다. 테스트넷에는 지연, 오류, 체인 재구성(chain reorganization, reorg), 롤백 또는 데이터 초기화가 발생할 수 있습니다.

출처: [GIWA 네트워크 연결 정보](https://docs.giwa.io/get-started/connect-to-giwa) · [GIWA 테스트넷 이용약관](https://docs.giwa.io/terms-and-policies/testnet-terms-of-use) · [RISK 컨트랙트](https://sepolia-explorer.giwa.io/address/0xa1836f8251eab5704A8Fedc6b64278A70132f578?tab=contract)
