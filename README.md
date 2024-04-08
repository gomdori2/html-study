# 2. 스타일(style)

align-self : strech > 부모가 줄어들면 자식도 줄어들어라 의미

## 6.1 스타일 시트

- 브라우저 기본스타일

  - 웹 브라우저에서 기본으로 사용하는 스타일

```- 인라인 스타일(태그안에 사용)
- 내부 스타일 시트(<style></style>)
- 외부 스타일 시트(css,scss 등등의 파일을 해당 js에 import해서 사용하는거)
```

```html
<head>
  <meta />
  <title></title>
  <!-- 헤드 안 맨밑에 넣어야함. -->
  <link rel="stylesheet" href="외부 파일시트 파일 경로" />
</head>
```

## 6.2. css 기본 선택자(selector)

1. 전체 선택자

- 문서 모든 요소에 스타일을 적용

```css
* {
}
```

2. 타입 선택자

- 특정 태그를 사용한 모든 요소에서 스타일 적용
-

```css
p {
  font-style: ~~~;
}
```

3. 클래스 선택자

- 특정 부분만 선택해서 문서 안에 여러번 적용
- 재활용 용의

```css
.bg {
  backgound-color: #ddd;
}
```

4. 그룹 선택자

- 여러 요소에 같은 스타일을 적용
- ,표로 구분해서 주기

```css
h1,
h2 {
}
```

5. id 선택자

- #으로 구분해서 줌

```css
# id {
}
```

-

## 2.3 스타일 우선순위

1. 얼마나 중요한가?

- 사용자 스타일(제일 중요) -> 제작자 스타일 -> 브라우저 기본스타일

2. 적용 범위 어디까지인가?

- 적용 서열
  - !important > inline > id # 스타일 > class 스타일 > 타입 스타일

```css
div {
  background-color: #ffffff !important;
}

<div style="background-color: #ffffff;" > #ssdf {
}

.ssdf {
}

div {
}
```

3. 소스 작성 순서

- 나중에 작성한 스타일이 먼저 작성한 스타일을 덮어쓴다.

# 3. 텍스트 스타일()

## 3.1 글자와 관련된 속성

- font-family : "pretendard" (글꼴 종류 지정)
- font-size : 글자 크기 지정
- font-style : 글자 이탤릭체로 표시할지 지정
- font-weight : 글자의 굵기 지정

## 3.2 텍스트 스타일 속성

- color : 글자색 지정
- text-decoration : none;

  - 텍스트에 밑줄, 취소선 등등(a태그의 하이퍼링크 표시나 등등) 표시할지 여부

- text-transform :
  - 텍스트 전체, 또는 첫 글자를 대문자로 표시
- text-shadow: 텍스트에 그림자 추가
- letter-spacing : 글자사이에 간격(자간)
- text :
- word-spascing : 단어사이 간격
- text-align : 텍스트 정렬 방법
- line-height : 줄 간격 조정(행간)
- tip
  - mac : otf / window : ttf
  - 삐침 > serif
  - 삐침이 없음 > san

## 3.3 웹에서 색상을 지정하는 방법

- \# 16진수 hex 코드 : #/00/00/00
  - 00 00 00 > 같이 숫자가 같으면 #000해도 됨
- rgb(빛의 삼원색, 모니터용[화면용]{rgb다 섞으면 하얀색}), rgba :
  - alpha : 투명도
  - rgb :rgba(255,255,255, 0.7) red / green / blue
- hsl, hsla
- 색상 이름(white, black)
- cmyk(색상 이니셜)

## 3.4 텍스트를 정렬하는 text-align 속성

- start : 현재 텍스트 줄의 시작 위치에 맞추어 문단을 정렬
- end : 현재 텍스트 줄의 끝 위치에 맞추어 문단을 정렬
- left : 왼쪽 맞춤
- right 오른쪽 맞춤
- center : 가운데 맞춤
- justify : 양쪽 맞춤
- match-parent : 부모 요소를 따라 문단 정렬

## 3.5 줄 간격을 조절하는 line-height 속성

- 보통 1.25 ~ 1.75배 정도 추천
- 박스 높이랑 같이 주면 위 / 아래 정렬 한거 같은 효과 있음

## 3.6 텍스트의 줄을 표시하거나 없애 주는 text-decoration 속성

- 텍스트에 밑줄을 긋거나 취소선을 표시
- 하이퍼링크 밑줄 없애기 등에 사용
- none
- underline
- overline
- line-through

## 3.7 텍스트에 그림자 효과 text-shadow 속성

- default : none으로 적용되어있다.
- text-shadow : 가로거리 세로거리 번짐정도 색상
  - text-shadow : 50px 50px
- 양수면 오른쪽 아래 / 음수면 왼쪽 위로

## 3.8 텍스트의 대소문자를 변환하는 text-transform 속성

- 영문자
- capialize : 첫 번째 글자를 대문자로
- uppercase : 모든 글자를 대문자
- lowercase : 모든 글자를 소문자
- full-width : 가능한 모든 문자를 전각 문자로 변환

## 3.9 글자 간격을 조절하는 letter-spacing, word-spacing

- leter-spacing : 자간
- word-spacing : 단어와 단어 사기 간격을 조절
