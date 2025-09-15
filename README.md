<!-- ================= HEADER ================= -->
<img src="https://github.com/user-attachments/assets/250d0aae-9fd7-40ec-80b1-d2e7d54ac41a" alt="Npay logo"/>

# 주문형 API 개발 기술지원 (Order API Development Technical Support)

![GitHub stars](https://img.shields.io/github/stars/npay-mall-order-api/merchant-order-api?style=social)
![GitHub Discussions](https://img.shields.io/github/discussions/npay-mall-order-api/merchant-order-api?style=social)
![GitHub issues](https://img.shields.io/github/issues/npay-mall-order-api/merchant-order-api)

**Tech stack:** `Restful` | `FastAPI` |
**Status:** 🟢 Active Development

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

## 주문형 API 종류

| 구분           |                         | API                           | Endpoint      | 설명                                               |
|----------------|-------------------------|-------------------------------|---------------|----------------------------------------------------|
| **주문관리**   | 주문조회                 | 변경 상품 주문 내역 조회       | No Content    | 조회 범위 내에서 변경 이력이 있는 상품 주문 내역을 조회 |
|                |                         | 상품 주문 상세 내역 조회       | No Content    |  상품 주문에 대한 상세 상품 주문 내역을 조회         |
|                |                         | 상품 주문 목록 조회            | No Content    |  주문에 대한 상품 주문 번호 목록을 조회             |
|                |                         | 조건형 상품 주문 상세 내역 조회 | No Content    |  조건에 맞는 상품 주문에 대한 상세 내역을 조회       |
|                | 발주발송                | 발주 확인 처리                  | No Content    |  상품 주문을 발주 확인 처리                        |
|                |                         | 발송 지연 처리                 | No Content    |  상품 주문을 발송 지연 요청                        |
|                |                         | 발송 처리                      | No Content    |  상품 주문을 발송 처리                              |
|                | 취소                    | 취소 요청                      | No Content    |  상품 주문을 취소 요청                              |
|                |                         | 취소 요청 승인                 | No Content    |  상품 주문에 대한 취소 요청을 승인                  |
|                | 반품                    | 반품 접수                      | No Content    |  상품 주문에 대해 반품 요청                         |
|                |                         | 반품 승인                      | No Content    |  상품 주문에 대한 반품을 승인                       |
|                |                         | 반품 거부(철회)                | No Content    |  상품 주문에 대한 반품 요청을 거부(철회)            |
|                |                         | 반품 보류                      | No Content    |  상품 주문에 대한 반품을 보류                       |
|                |                         | 반품 보류 해제                 | No Content    |  상품 주문에 대한 반품 보류를 해제                  |
|                | 교환                    | 교환 수거 완료                 | No Content    |  상품 주문에 대한 교환을 수거 완료 처리             |
|                |                         | 교환 재배송 처리               | No Content    |  상품 주문 교환 승인 건을 재배송 처리               |
|                |                         | 교환 거부(철회)                | No Content    |  상품 주문에 대한 교환 요청을 거부(철회)            |
|                |                         | 교환 보류                      | No Content    |  상품 주문에 대한 교환을 보류                       |
|                |                         | 교환 보류 해제                 | No Content    |  상품 주문에 대한 교환 보류를 해제                  |
|                | 리뷰조회                | 리뷰 조회                      | No Content    |  상품 주문에 대한 리뷰를 조회                       |
| **정산**       |                         | No content                    | No Content    |  No content                                        |
| **문의**       | 문의조회                | 문의 조회                      | No Content    |  구매자가 등록한 문의를 조회                        |
|                | 문의처리                |문의 처리                       | No Content    |  구매자가 등록한 문의에 답변 처리 혹은 답변 수정     |

## 주문형 API 인증 정보 확인
내 API 호출 인증 정보 (애플리케이션) 조회 ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/discussions/categories/announcements)

## API 문서 가이드 바로가기
API 문서 가이드 ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/discussions/categories/announcements)

---

