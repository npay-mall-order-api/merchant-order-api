<!-- ================= HEADER ================= -->
<img src="https://github.com/user-attachments/assets/250d0aae-9fd7-40ec-80b1-d2e7d54ac41a" alt="Npay logo"/> 

# 주문형 API 개발 기술지원 (Order API Development Technical Support)


![GitHub stars](https://img.shields.io/github/stars/username/repo?style=social)
![GitHub forks](https://img.shields.io/github/forks/username/repo?style=social)
![GitHub issues](https://img.shields.io/github/issues/username/repo)
![License](https://img.shields.io/github/license/username/repo)

**Tech stack:** `Restful` | `FastAPI` |
**Status:** 🟢 Active Development

---

## 📖 목차
- 소개(Introduction)
- 사용 예제 (Example of use)

---

## 소개 (Introduction)
제휴 파트너사를 이용하지 않고 Npay 주문형을 자체적으로 개발하는 연동사를 위한 기술지원 공간입니다. <br />
It is a technical support space for linked companies that develop their own Npay on-demand without using affiliated partners.

---

## 사용 예제 (Example of use)
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
