<!-- ================= HEADER ================= -->
<img src="https://github.com/user-attachments/assets/250d0aae-9fd7-40ec-80b1-d2e7d54ac41a" alt="Npay logo"/>

# 주문형 API 개발 기술지원 (Order API Development Technical Support)

![GitHub stars](https://img.shields.io/github/stars/npay-mall-order-api/merchant-order-api?style=social)
![GitHub Discussions](https://img.shields.io/github/discussions/npay-mall-order-api/merchant-order-api?style=social)
![GitHub issues](https://img.shields.io/github/issues/npay-mall-order-api/merchant-order-api)

**Tech stack:** `Restful` | `FastAPI` |
**Status:** 🟢 Active Development

---

### 공간 소개
Npay 주문형을 자체적으로 개발하는 연동사를 위한 기술지원 공간입니다. <br />
It is a technical support space for the development Npay order.

### 공간 바로가기

| 공간         | 내용                                                         | 링크 |
|--------------|-------------------------------------------------------------|------------|
| 📣 공지사항 | 공지사항을 확인하실 수 있습니다. | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/discussions/categories/announcements) |
| 📝 릴리즈 노트 | API 에 업데이트 되는 내용들을 확인하실 수 있습니다. | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/discussions/categories/release-note) |
| 🙏 묻고 답하기 | API 연동 중 기술 문의사항을 직접 문의하실 수 있습니다. | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/discussions/categories/q-a) |
| 💡 자주 묻는 질문 | API 연동 중 자주 묻는 질문 (FAQ) 을 확인하실 수 있습니다. | ➡ [바로가기](https://github.com/npay-mall-order-api/merchant-order-api/discussions/categories/faq) |

---

### API 연동 시작하기

#### + API 문서 가이드 바로가기 추가 +

---




### Npay 주문형 버튼 적용 예제
```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>
<head>
    <meta http-equiv="Content-Type" content="text/html; charset=euc-kr">
    <title>네이버페이 버튼 사용법</title>
    <script type="text/javascript" src="http://pay.naver.com/customer/js/naverPayButton.js" charset="UTF-8"></script>
</head>
<body>
    <script type="text/javascript">
        //<![CDATA[ // 
        naver.NaverPayButton.apply({
            BUTTON_KEY: "버튼 인증 키", // 네이버페이에서 제공받은 버튼 인증 키 입력
            TYPE: "E", // 버튼 모음 종류 설정
            COLOR: 1, // 버튼 모음의 색 설정
            COUNT: 2, // 버튼 개수 설정. 구매하기 버튼만 있으면(장바구니 페이지) 1, 찜하기 버튼도 있으면(상품 상세 페이지) 2를 입력.
            ENABLE: "Y", // 품절 등의 이유로 버튼 모음을 비활성화할 때에는 "N" 입력
            "": ""
        }); //]]>
    </script>
</body>
</html>
```
