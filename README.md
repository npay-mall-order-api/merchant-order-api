<!-- ================= HEADER ================= -->
# 주문형 API 개발 기술지원

![GitHub stars](https://img.shields.io/github/stars/npay-mall-order-api/merchant-order-api?style=social)
![GitHub Discussions](https://img.shields.io/github/discussions/npay-mall-order-api/merchant-order-api?style=social)
![GitHub issues](https://img.shields.io/github/issues/npay-mall-order-api/merchant-order-api)

**Tech stack:** `Restful` | `HTTPS`

---

## 공간 소개
Npay 주문형 연동 개발을 위한 기술지원 공간입니다. <br />
It is a technical support space for the development Npay order.

## 공간 바로가기

| 공간         | 내용                                                         | 링크 |
|--------------|-------------------------------------------------------------|------------|
| 📣 공지사항 | 공지사항을 확인하실 수 있습니다. | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/discussions/categories/announcements) |
| 📝 릴리즈 노트 | API 에 업데이트 되는 내용들을 확인하실 수 있습니다. | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/discussions/categories/release-note) |
| 🙏 묻고 답하기 | API 연동 중 기술 문의사항을 직접 문의하실 수 있습니다. | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/discussions/categories/q-a) |
| 💡 자주 묻는 질문 | API 연동 중 자주 묻는 질문 (FAQ) 을 확인하실 수 있습니다. | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/discussions/categories/faq) |

---

## 주문형 API 개요
네이버페이 주문형 가맹점이 네이버페이 이용 중 주문 관련 내역 또는 그 밖의 필요한 정보를 조회 혹은 처리할 수 있는 API 입니다.

## API 문서 가이드 바로가기
API 문서 가이드 ➡ [바로가기](https://admin.pay.naver.com/)

## 주문형 API 종류





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

## 주문형 API 인증 정보 확인
내 API 호출 인증 정보 (애플리케이션) 조회 ➡ [바로가기](https://admin.pay.naver.com/)

## 주문형 API 주문 상태 변경 다이어그램
정상 주문, 취소, 반품, 교환에 따른 주문의 상태 변경을 다이어그램으로 설명합니다. 

| 구분         | 링크                                                         | 
|--------------|-------------------------------------------------------------|
| 정상 주문 상태 | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/wiki/%EC%A3%BC%EB%AC%B8-%EC%83%81%ED%83%9C-%EC%9D%B4%EB%8F%99-%EB%8B%A4%EC%9D%B4%EC%96%B4%EA%B7%B8%EB%9E%A8#%EC%A0%95%EC%83%81-%EC%A3%BC%EB%AC%B8-%EC%83%81%ED%83%9C-%EC%9D%B4%EB%8F%99-%EB%8B%A4%EC%9D%B4%EC%96%B4%EA%B7%B8%EB%9E%A8) |
| 취소 주문 상태 | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/wiki/%EC%A3%BC%EB%AC%B8-%EC%83%81%ED%83%9C-%EC%9D%B4%EB%8F%99-%EB%8B%A4%EC%9D%B4%EC%96%B4%EA%B7%B8%EB%9E%A8#%EC%B7%A8%EC%86%8C-%EC%A3%BC%EB%AC%B8-%EC%83%81%ED%83%9C-%EC%9D%B4%EB%8F%99-%EB%8B%A4%EC%9D%B4%EC%96%B4%EA%B7%B8%EB%9E%A8) |
| 반품 주문 상태 | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/wiki/%EC%A3%BC%EB%AC%B8-%EC%83%81%ED%83%9C-%EC%9D%B4%EB%8F%99-%EB%8B%A4%EC%9D%B4%EC%96%B4%EA%B7%B8%EB%9E%A8#%EB%B0%98%ED%92%88-%EC%A3%BC%EB%AC%B8-%EC%83%81%ED%83%9C-%EC%9D%B4%EB%8F%99-%EB%8B%A4%EC%9D%B4%EC%96%B4%EA%B7%B8%EB%9E%A8) |
| 교환 주문 상태 | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/wiki/%EC%A3%BC%EB%AC%B8-%EC%83%81%ED%83%9C-%EC%9D%B4%EB%8F%99-%EB%8B%A4%EC%9D%B4%EC%96%B4%EA%B7%B8%EB%9E%A8#%EA%B5%90%ED%99%98-%EC%A3%BC%EB%AC%B8-%EC%83%81%ED%83%9C-%EC%9D%B4%EB%8F%99-%EB%8B%A4%EC%9D%B4%EC%96%B4%EA%B7%B8%EB%9E%A8) |

---

