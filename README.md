<!-- ================= HEADER ================= -->
# 주문형 API 개발 기술지원

![GitHub stars](https://img.shields.io/github/stars/npay-mall-order-api/merchant-order-api?style=social)
![GitHub Discussions](https://img.shields.io/github/discussions/npay-mall-order-api/merchant-order-api?style=social)
![GitHub issues](https://img.shields.io/github/issues/npay-mall-order-api/merchant-order-api)

**Tech stack:** `Restful` `OAuth 2.0` | `HTTPS`

---

## Github 소개
네이버페이 주문형 API 연동 개발을 위한 기술지원 Github 공간입니다. <br/>
Repository 알림 (Watch) 을 활성화 해주시면 원활한 문의&답변이 가능합니다. <br />
(※ Repository 상단 → Watch → Participating and @mentions) 

| 공간         | 내용                                                         | 링크 |
|--------------|-------------------------------------------------------------|------------|
| 📣 공지사항 | 공지사항을 확인하실 수 있습니다. | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/discussions/categories/announcements) |
| 📝 릴리즈 노트 | API 에 업데이트 되는 내용들을 확인하실 수 있습니다. | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/discussions/categories/release-note) |
| 🙏 묻고 답하기 | API 연동 중 기술 문의사항을 직접 문의하실 수 있습니다. | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/discussions/categories/q-a) |
| 💡 자주 묻는 질문 | API 연동 중 자주 묻는 질문 (FAQ) 을 확인하실 수 있습니다. | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/discussions/categories/faq) |
| 📖 Wiki | API 연동 가이드 및 참고 정보를 확인하실 수 있습니다.  | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/wiki) |



---

## API 소개
### 주문관리 API
네이버페이 주문 정보를 조회 및 처리할 수 있는 API 입니다. <br/>
### 정산 API
네이버페이 정산 정보를 조회할 수 있는 API 입니다. <br/>

---

## API 문서 가이드 
### 주문관리 API
- 개발 환경 API 문서 : https://sandbox-api.pay.naver.com/npay/partner
- 운영 환경 API 문서 : https://api.pay.naver.com/npay/partner <br/><br/>
※ 위 문서는 발급받은 애플리케이션 `ID`/`시크릿` 으로 확인 가능합니다.

### 정산 API

---

## API 연동 프로세스

<details>
  <summary>Step 0️⃣. 개발 환경 애플리케이션 인증 정보 (ID/Secret) 발급하기</summary>

  <br/>
  [네이버페이센터](https://admin.pay.naver.com)에서 발급하실 수 있습니다. 

</details>

<details>
  <summary>Step 1️⃣. 개발 환경에서 API 연동하기</summary>

  #### 1. OAuth 토큰 발급하기
  &nbsp;&nbsp;&nbsp;&nbsp;
  API 를 호출하기 위한 인증 토큰을 발급/갱신 요청합니다. ➡ 📖 API 문서 가이드 [바로가기](https://api.pay.naver.com/npay/partner#tag/OAuth-2.0)
  
  >❓ 인증 토큰 Request Body 중 전자서명 생성하는 방법 ➡ 📖 API 문서 가이드 [바로가기](https://api.pay.naver.com/npay/partner#section/%EC%9D%B8%EC%A6%9D/%EC%A0%84%EC%9E%90%EC%84%9C%EB%AA%85) <br/>  <br />
  >주문형 API 에서는 인증 토큰 발급을 요청할 때 client_secret 값을 직접 전달하지 않고 전자서명 (signature) 을 생성하여 전달하는 방법으로 client_secret 탈취에 대해 강화된 보안을 제공합니다.

  #### 2. 발급받은 토큰을 이용한 API 호출 및 개발
  
  &nbsp;&nbsp;&nbsp;&nbsp;
  발급받은 인증 토큰을 HTTP Authorization Header 에 포함하여 API 를 호출합니다. ➡ 📖 API 문서 가이드 [바로가기](https://api.pay.naver.com/npay/partner#tag/%EC%A3%BC%EB%AC%B8-%EC%A1%B0%ED%9A%8C) <br/>  <br />
  &nbsp;&nbsp;&nbsp;&nbsp;
  `Authorization: Bearer {access_token}`

  #### 3. 필요한 API 들을 확인하여 개발합니다.

</details>


<details>
  <summary>Step 2️⃣. 개발 환경 검수 요청하기</summary>
  
  <br />
  
  개발 환경에서의 API 연동 개발이 완료되면 기술지원 부서로 검수 요청을 합니다. ➡ 검수 요청 [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/discussions/categories/inspection-request) <br/>
  검수 중 수정이 필요한 내용들은 수정 요청드릴 예정이며, 수정이 모두 확인되면 개발 환경에서의 검수가 완료됩니다.
  
  > **⚠️[주의](https://github.com/npay-mall-order-api/partner-cafe24?tab=security-ov-file#%EC%A3%BC%EC%9D%98%EC%82%AC%ED%95%AD%EF%B8%8F):** 공개가 부적합한 정보는 게시되어선 안됩니다.  
  > 등록하신 문의 내용은 게시 즉시 다른 사용자들에게도 공개됩니다.  
  > 내용의 본문, 첨부파일 등으로 아래에 해당하는 정보를 게시하지 않도록 주의해주시기 바랍니다.
  
</details>

<details>
  <summary>Step 3️⃣. 운영 환경 애플리케이션 인증 정보 (ID/Secret) 발급하기</summary>
  
  <br/>
  개발 환경에서의 검수가 완료되고 이슈가 없다고 판단되면 기술지원 부서에서 운영 환경 애플리케이션을 발급합니다. <br/> <br/>
  
  검수가 완료되었을 경우 ✉️dl_techsupport@navercorp.com 으로 아래 양식과 함께 메일 문의주시면 됩니다. (검수 완료 여부 확인 후 발급) <br/>
  발급된 애플리케이션은 별도 메일 발송됩니다. (파일 암호는 '휴대폰 번호' 로 발송됩니다.)

>- 가맹점 ID : np_xxxxxx  <br/>
>- 개발 담당자 이메일 :  <br/>
>- API 호출 IP  <br/>
 
  ※ 가맹점ID 는 [네이버페이센터 > 내정보 > 가입정보변경 > 페이센터ID] 경로에서 확인하실 수 있습니다.  <br/>
  ※ 위 가맹점 및 개인 정보는 이 공간에 게시되어선 안됩니다. 내용의 본문, 첨부파일 등으로 아래에 해당하는 정보를 게시하지 않도록 주의해주시기 바랍니다.

</details>

<details>
  <summary>Step 4️⃣. 운영 환경 API 적용</summary>
  
  <br/>
  발급된 애플리케이션을 운영 환경에 적용하고 사용자들이 해당 기능들을 이용할 수 있도록 서비스 오픈합니다. 
  
</details>

---

## API 내용
### 호스트
- 운영 환경 : `https://api.pay.naver.com/npay/partner`
- 개발 환경 : `https://sandbox-api.pay.naver.com/npay/partner`

### 주문관리 API
| 구분                    | API                           | Method | Path          | 설명                                               |
|-------------------------|-------------------------------|------|---------------|----------------------------------------------------|
| 주문조회   | 변경 상품 주문 내역 조회       | ![GET](https://img.shields.io/badge/GET-blue) | `/v1/pay-order/mall/product-orders/last-changed-statuses` | 조회 범위 내에 변경 이력이 있는 상품 주문 내역을 조회 |
|           | 상품 주문 상세 내역 조회        | ![POST](https://img.shields.io/badge/POST-green) | `/v1/pay-order/mall/product-orders/query` |  상품 주문에 대한 상세 상품 주문 내역을 조회 |
|           | 상품 주문 번호 목록 조회        | ![GET](https://img.shields.io/badge/GET-blue) | `/v1/pay-order/mall/orders/{orderId}/product-order-ids` |  주문에 대한 상품 주문 번호 목록을 조회 |
|           | 조건형 상품 주문 상세 내역 조회 | ![GET](https://img.shields.io/badge/GET-blue) | `/v1/pay-order/mall/product-orders` |  조건에 맞는 상품 주문에 대한 상세 내역을 조회 |
| 발주/발송  | 발주 확인 처리                 | ![POST](https://img.shields.io/badge/POST-green) | `/v1/pay-order/mall/product-orders/confirm` |  단수 또는 복수 개 상품 주문의 발주를 확인 처리 |
|           | 발송 지연 처리                 | ![POST](https://img.shields.io/badge/POST-green) | `/v1/pay-order/mall/product-orders/{productOrderId}/delay` |  1건의 상품 주문을 발송 지연 요청 |
|           | 발송 처리                      | ![POST](https://img.shields.io/badge/POST-green) | `/v1/pay-order/mall/product-orders/dispatch` |  단수 또는 복수 개 상품 주문을 발송 처리 |
| 취소      | 취소 요청                      | ![POST](https://img.shields.io/badge/POST-green) | `/v1/pay-order/mall/product-orders/{productOrderId}/claim/cancel/request` |  1건의 상품 주문을 취소 요청 |
|           | 취소 요청 승인                 | ![POST](https://img.shields.io/badge/POST-green) | `/v1/pay-order/mall/product-orders/{productOrderId}/claim/cancel/approve` |  1건의 상품 주문에 대한 취소 요청을 승인 |
| 반품      | 반품 요청                      | ![POST](https://img.shields.io/badge/POST-green) | `/v1/pay-order/mall/product-orders/{productOrderId}/claim/return/request` |  1건의 상품 주문에 대해 반품 요청 |
|           | 반품 승인                      | ![POST](https://img.shields.io/badge/POST-green) | `/v1/pay-order/mall/product-orders/{productOrderId}/claim/return/approve` |  1건의 상품 주문에 대한 반품을 승인 |
|           | 반품 거부(철회)                | ![POST](https://img.shields.io/badge/POST-green) | `/v1/pay-order/mall/product-orders/{productOrderId}/claim/return/reject` |  1건의 상품 주문에 대한 반품 요청을 거부(철회) |
|           | 반품 보류                      | ![POST](https://img.shields.io/badge/POST-green) | `/v1/pay-order/mall/product-orders/{productOrderId}/claim/return/holdback` |  1건의 상품 주문에 대한 반품을 보류 |
|           | 반품 보류 해제                 | ![POST](https://img.shields.io/badge/POST-green) | `/v1/pay-order/mall/product-orders/{productOrderId}/claim/return/holdback/release` |  1건의 상품 주문에 대한 반품 보류를 해제 |
| 교환      | 교환 수거 완료                 | ![POST](https://img.shields.io/badge/POST-green) | `/v1/pay-order/mall/product-orders/{productOrderId}/claim/exchange/collect/complete` |  1건의 상품 주문에 대한 교환을 수거 완료 처리 |
|           | 교환 재배송 처리               | ![POST](https://img.shields.io/badge/POST-green) | `/v1/pay-order/mall/product-orders/{productOrderId}/claim/exchange/dispatch` |  1건의 상품 주문 교환 승인 건을 재배송 처리 |
|           | 교환 거부(철회)                | ![POST](https://img.shields.io/badge/POST-green) | `/v1/pay-order/mall/product-orders/{productOrderId}/claim/exchange/reject` |  1건의 상품 주문에 대한 교환 요청을 거부(철회) |
|           | 교환 보류                      | ![POST](https://img.shields.io/badge/POST-green) | `/v1/pay-order/mall/product-orders/{productOrderId}/claim/exchange/holdback` |  1건의 상품 주문에 대한 교환을 보류 |
|           | 교환 보류 해제                 | ![POST](https://img.shields.io/badge/POST-green) | `/v1/pay-order/mall/product-orders/{productOrderId}/claim/exchange/holdback/release` |  1건의 상품 주문에 대한 교환 보류를 해제 |
| 리뷰      | 리뷰 조회                     | ![GET](https://img.shields.io/badge/GET-blue) | `/v1/pay-order/mall/reviews` |  상품 주문에 대한 리뷰를 조회 |

### 정산 API

---

## 주문 상태 변경 다이어그램
정상 주문, 취소, 반품, 교환에 따른 주문의 상태 변경을 다이어그램으로 설명합니다. 

| 구분         | 링크                                                         | 
|--------------|-------------------------------------------------------------|
| 정상 주문 상태 | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/wiki/%EC%A3%BC%EB%AC%B8-%EC%83%81%ED%83%9C-%EC%9D%B4%EB%8F%99-%EB%8B%A4%EC%9D%B4%EC%96%B4%EA%B7%B8%EB%9E%A8#%EC%A0%95%EC%83%81-%EC%A3%BC%EB%AC%B8-%EC%83%81%ED%83%9C-%EC%9D%B4%EB%8F%99-%EB%8B%A4%EC%9D%B4%EC%96%B4%EA%B7%B8%EB%9E%A8) |
| 취소 주문 상태 | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/wiki/%EC%A3%BC%EB%AC%B8-%EC%83%81%ED%83%9C-%EC%9D%B4%EB%8F%99-%EB%8B%A4%EC%9D%B4%EC%96%B4%EA%B7%B8%EB%9E%A8#%EC%B7%A8%EC%86%8C-%EC%A3%BC%EB%AC%B8-%EC%83%81%ED%83%9C-%EC%9D%B4%EB%8F%99-%EB%8B%A4%EC%9D%B4%EC%96%B4%EA%B7%B8%EB%9E%A8) |
| 반품 주문 상태 | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/wiki/%EC%A3%BC%EB%AC%B8-%EC%83%81%ED%83%9C-%EC%9D%B4%EB%8F%99-%EB%8B%A4%EC%9D%B4%EC%96%B4%EA%B7%B8%EB%9E%A8#%EB%B0%98%ED%92%88-%EC%A3%BC%EB%AC%B8-%EC%83%81%ED%83%9C-%EC%9D%B4%EB%8F%99-%EB%8B%A4%EC%9D%B4%EC%96%B4%EA%B7%B8%EB%9E%A8) |
| 교환 주문 상태 | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/wiki/%EC%A3%BC%EB%AC%B8-%EC%83%81%ED%83%9C-%EC%9D%B4%EB%8F%99-%EB%8B%A4%EC%9D%B4%EC%96%B4%EA%B7%B8%EB%9E%A8#%EA%B5%90%ED%99%98-%EC%A3%BC%EB%AC%B8-%EC%83%81%ED%83%9C-%EC%9D%B4%EB%8F%99-%EB%8B%A4%EC%9D%B4%EC%96%B4%EA%B7%B8%EB%9E%A8) |

---

## SOAP → REST API 전환 참고사항
기존의 SOAP 방식에서 REST API 로 전환하시는 경우에는 이 문서를 참고해주세요. ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/wiki/SOAP-%E2%86%92-REST-API-%EC%A0%84%ED%99%98-%EC%B0%B8%EA%B3%A0%EC%82%AC%ED%95%AD)





