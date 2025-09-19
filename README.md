<!-- ================= HEADER ================= -->
# 주문형 API 개발 기술지원

![GitHub stars](https://img.shields.io/github/stars/npay-mall-order-api/merchant-order-api?style=social)
![GitHub Discussions](https://img.shields.io/github/discussions/npay-mall-order-api/merchant-order-api?style=social)
![GitHub issues](https://img.shields.io/github/issues/npay-mall-order-api/merchant-order-api)

**Tech stack:** `Restful` `OAuth 2.0` | `HTTPS`

---

## Github 소개
Npay 주문형 연동 개발을 위한 기술지원 Github 공간입니다. <br/>
Repository 알림 (Watch) 을 활성화 해주시면 원활한 문의&답변이 가능합니다. (※ Repository 상단 → Watch → Participating and @mentions) 

| 공간         | 내용                                                         | 링크 |
|--------------|-------------------------------------------------------------|------------|
| 📣 공지사항 | 공지사항을 확인하실 수 있습니다. | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/discussions/categories/announcements) |
| 📝 릴리즈 노트 | API 에 업데이트 되는 내용들을 확인하실 수 있습니다. | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/discussions/categories/release-note) |
| 🙏 묻고 답하기 | API 연동 중 기술 문의사항을 직접 문의하실 수 있습니다. | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/discussions/categories/q-a) |
| 💡 자주 묻는 질문 | API 연동 중 자주 묻는 질문 (FAQ) 을 확인하실 수 있습니다. | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/discussions/categories/faq) |
| 📖 Wiki | API 연동 가이드 및 참고 정보를 확인하실 수 있습니다.  | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/wiki) |



---

## 주문형 API 소개
네이버페이 주문형 가맹점이 네이버페이 이용 중 주문 관련 내역 또는 그 밖의 필요한 정보를 조회 혹은 처리할 수 있는 API 입니다. <br />

## 주문형 API 문서 가이드 ➡ [바로가기](https://api.pay.naver.com/npay/partner)
API 호출에 대한 가이드를 확인하실 수 있습니다.  

## 주문형 API 연동 시작하기
#### Step 0️⃣. 애플리케이션 인증 정보 (ID/Secret) 발급하기
<details>
  <summary>more</summary>

  <br />
  인증 정보 발급하기 ➡ [바로가기](https://github.com/npay-mall-order-api/partner-cafe24/wiki/%EC%95%A0%ED%94%8C%EB%A6%AC%EC%BC%80%EC%9D%B4%EC%85%98-%EB%B0%9C%EA%B8%89-%EB%B0%A9%EB%B2%95) <br/>
  인증 정보 조회하기 ➡ [바로가기](https://admin.pay.naver.com/)

</details>

#### Step 1️⃣. OAuth 토큰 발급하기
<details>
  <summary>more</summary>
  
<br />
  API 를 호출하기 위한 인증 토큰을 발급/갱신 요청합니다. ➡ 📖 API 문서 가이드 [바로가기](https://api.pay.naver.com/npay/partner#tag/OAuth-2.0)
  
> ❓ 인증 토큰 Request Body 중 전자서명 생성하는 방법 ➡ 📖 API 문서 가이드 [바로가기](https://api.pay.naver.com/npay/partner#section/%EC%9D%B8%EC%A6%9D/%EC%A0%84%EC%9E%90%EC%84%9C%EB%AA%85) <br/>
>주문형 API 에서는 인증 토큰 발급을 요청할 때 client_secret 값을 직접 전달하지 않고 전자서명 (signature) 을 생성하여 전달하는 방법으로 client_secret 탈취에 대해 강화된 보안을 제공합니다.

</details>

#### Step 2️⃣. 발급받은 토큰을 이용한 API 호출
<details>
  <summary>more</summary>
  
  <br />
발급받은 인증 토큰을 HTTP Authorization Header 에 포함하여 API 를 호출합니다. ➡ 📖 API 문서 가이드 [바로가기](https://api.pay.naver.com/npay/partner#tag/%EC%A3%BC%EB%AC%B8-%EC%A1%B0%ED%9A%8C) <br/>
  `Authorization: Bearer {access_token}`

</details>

#### Step 3️⃣. 인증 토큰 만료 여부에 따라 갱신 요청
<details>
  <summary>more</summary>
  
  <br />
  인증 토큰의 유효 시간은 3시간(10,800초)입니다. ➡ 📖 API 문서 가이드 [바로가기](https://api.pay.naver.com/npay/partner#tag/OAuth-2.0/operation/issueToken.commerce-id)<br />
  발급된 인증 토큰이 존재하는 경우 남은 유효 시간이 30분 이상이면 기존 인증 토큰이 반환되고 30분 미만이면 새로운 인증 토큰이 발급됩니다. <br/>
  새로운 인증 토큰이 발급된 경우에도 유효 시간이 만료되기 전까지는 기존 인증 토큰을 사용할 수 있습니다.<br/>

</details>

## 주문형 API 내용
### 호스트
- 운영 환경 : `https://api.pay.naver.com/npay/partner`
- 개발 환경 : `https://sandbox-api.pay.naver.com/npay/partner`

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


### 주문 상태 변경 다이어그램
정상 주문, 취소, 반품, 교환에 따른 주문의 상태 변경을 다이어그램으로 설명합니다. 

| 구분         | 링크                                                         | 
|--------------|-------------------------------------------------------------|
| 정상 주문 상태 | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/wiki/%EC%A3%BC%EB%AC%B8-%EC%83%81%ED%83%9C-%EC%9D%B4%EB%8F%99-%EB%8B%A4%EC%9D%B4%EC%96%B4%EA%B7%B8%EB%9E%A8#%EC%A0%95%EC%83%81-%EC%A3%BC%EB%AC%B8-%EC%83%81%ED%83%9C-%EC%9D%B4%EB%8F%99-%EB%8B%A4%EC%9D%B4%EC%96%B4%EA%B7%B8%EB%9E%A8) |
| 취소 주문 상태 | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/wiki/%EC%A3%BC%EB%AC%B8-%EC%83%81%ED%83%9C-%EC%9D%B4%EB%8F%99-%EB%8B%A4%EC%9D%B4%EC%96%B4%EA%B7%B8%EB%9E%A8#%EC%B7%A8%EC%86%8C-%EC%A3%BC%EB%AC%B8-%EC%83%81%ED%83%9C-%EC%9D%B4%EB%8F%99-%EB%8B%A4%EC%9D%B4%EC%96%B4%EA%B7%B8%EB%9E%A8) |
| 반품 주문 상태 | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/wiki/%EC%A3%BC%EB%AC%B8-%EC%83%81%ED%83%9C-%EC%9D%B4%EB%8F%99-%EB%8B%A4%EC%9D%B4%EC%96%B4%EA%B7%B8%EB%9E%A8#%EB%B0%98%ED%92%88-%EC%A3%BC%EB%AC%B8-%EC%83%81%ED%83%9C-%EC%9D%B4%EB%8F%99-%EB%8B%A4%EC%9D%B4%EC%96%B4%EA%B7%B8%EB%9E%A8) |
| 교환 주문 상태 | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/wiki/%EC%A3%BC%EB%AC%B8-%EC%83%81%ED%83%9C-%EC%9D%B4%EB%8F%99-%EB%8B%A4%EC%9D%B4%EC%96%B4%EA%B7%B8%EB%9E%A8#%EA%B5%90%ED%99%98-%EC%A3%BC%EB%AC%B8-%EC%83%81%ED%83%9C-%EC%9D%B4%EB%8F%99-%EB%8B%A4%EC%9D%B4%EC%96%B4%EA%B7%B8%EB%9E%A8) |

---

## SOAP → REST API 전환 
기존의 SOAP 방식에서 REST API 로 전환하면서 궁금해하실만한 내용들을 정리해놓았습니다. ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/wiki/SOAP-%E2%86%92-REST-API-%EC%A0%84%ED%99%98-%EC%B0%B8%EA%B3%A0%EC%82%AC%ED%95%AD)





