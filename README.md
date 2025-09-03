<!-- ================= HEADER ================= -->
<img src="https://github.com/user-attachments/assets/250d0aae-9fd7-40ec-80b1-d2e7d54ac41a" alt="Npay logo"/> 

# 주문형 API 기술지원



![GitHub stars](https://img.shields.io/github/stars/username/repo?style=social)
![GitHub forks](https://img.shields.io/github/forks/username/repo?style=social)
![GitHub issues](https://img.shields.io/github/issues/username/repo)
![License](https://img.shields.io/github/license/username/repo)

**Tech stack:** `Restful` | `FastAPI` |
**Status:** 🟢 Active Development

---

## 📖 목차
- [소개](##소개)
- [사용 예제](#사용-예제)
- [API 문서](#api-문서)
- [주의사항⚠️](#주의사항⚠️)

---

## 소개
제휴 파트너사를 이용하지 않고 Npay 주문형을 자체적으로 개발하는 연동사를 위한 기술지원 공간입니다. 

---

## 사용예제
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


---

## API 문서

---

## 주의사항⚠️

> **주의:** 공개가 부적합한 정보는 게시되어선 안됩니다.  
> 등록하신 문의 내용은 게시 즉시 다른 사용자들에게도 공개됩니다.  
> 내용의 본문, 첨부파일 등으로 아래에 해당하는 정보를 게시하지 않도록 주의해주시기 바랍니다.

### 금지 정보 예시
- 개인정보(주민등록번호, 연락처, 주소 등)  
- 계정 비밀번호, 어플리케이션 정보, 토큰 등 인증 정보  
- 회사 내부 기밀 문서 및 민감 자료

---

### 권장 사항
- 질문/예제 중심으로 작성  
- 테스트용 데이터나 더미 정보 활용  
- 민감한 내용은 개인 채널로 문의

