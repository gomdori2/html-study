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

## 3.10 목록 스타일

- list-style > type, image 안주고 한번에 정리할수있음 1개만 필요할 때 사용

### 3.10.1 불릿 모양과 번호 스타일을 지정하는 list-style-type 속성

- disc : 채운 원모양
- circle : 빈 원 모양
- square : 채운 사각형
- decimal : 1~10(10진수)
- decimal-leading-zero : 앞에 0이 붙는 10진수 0~9
- lower-roman : 로마 숫자 소문자.
- upper-roman : 로마 숫자 대문자
- lower-alpha && lower-latin : 알파벳 소문자
- upper-alpha 또는 upper-latin : 알파벳 대문자
- none : 불릿이나 숫자를 없앤다.

### 3.10.2 불릿 대신 이미지를 사용하는 list-style-image 속성

```css
ul {
  list-style-image: url(../image/cat.png);
}
```

### 3.10.3 목록을 들여 쓰는 list-style-position 속성

- inside
- outside

### 3.10.4 목록 속성을 한꺼번에 표시하는 list-style 속성

```css
ul {
  list-style: url() none inside;
}
```

### 3.10.5 표 스타일\_일단 안하고 넘어감.

# 4. 레이아웃을 구성하는 CSS 박스모델

- 웹 문서에서 내용을 배치할 때는 각 요소를 박스 형태로 구성

- 박스 모델은 실제 내용이 들어가는 콘텐츠영역, 테두리, 여백으로 구성

## 4.1. CSS와 박스모델

- 웹 문서의 내용을 박스 형태로 정의하는 방법
- 박스 모델이 모여서 웹 문서를 이룬다.
- 박스 모델에는 마진, 패딩, 테두리 등 박스가 **여러 겹** 들어 있다.
  - 클론코딩 할때 피그마로 컴포넌트만이라도 짜보자

### 4.1.1. 블록 레벨 요소와 인라인 레벨 요소

- block-level 요소 : 태그를 사용해서 요소를 삽입했을 때 혼자 **한 줄을** 차지하는 것, 해당 요소의 너비는 100%

  - 대표 태그 : h1, div, p ...

- inline-level 요소 : 한 줄을 차지하지 않고, **콘텐츠 만큼만** 영역을 차지
- 따라서 한 줄에 인라인 레벨 요소를 여러 개 표시할 수 있다.
- 너비/높이값 못준다.
  - 대표 태그 : span, img, strong, a ...

### 4.1.2. 박스 모델의 기본 구성

- 박스 모델은 콘텐츠 영역
- 박스와 콘텐츠 영역 사이의 여백(패딩)
- 박스의 테두리 그리고 여러 박스 모델 사이의 여백(margin)

### 4.1.3. 콘텐츠 영역의 크기를 지정하는 width, height 속성

- 단위 : px이나 em단위로 지정
  - px, rem 단위를 많이 쓴다.
  - font-size : 10px 보통 계산하기 쉬우라고 해놓는다함.
  - em : 자기부모(부모 자식 태그 기준)에 몇배
    - 부모 요소의 글꼴 크기에 상대적이다.
    - 컨텐츠를 기준으로 할 시 사용
    - 부모를 따라감.
    - 반응형 디자인 때문에 사용
    - ex) 부모태그 10px > 1.2em > 12px로 잡힘.
  - root em 인 rem 단위를 쓰는 것이 일관된 크기 조정에 용이하다.
  - 백분율 : 박스 모델을 포함하는 `부모 요소를 기준`으로 너비, 높이 값을 백분율(%)로 지정
  - auto : 박스 모델의 너비, 높이 값이 콘텐츠 양에 따라 자동으로 결정(기본값)
    - default값으로 auto 들어감.

### 4.1.2. 박스 모델의 크기를 계한하는 box-sizing 속성

- border-box : 테두리까지 포함해서 width 값을 지정

  - 웹 문서 레이아웃을 만들 때 요소의 크기를 쉽게 계산할려면 이것을 주자.
  - 회사의 컨벤션으로 사용 x 일 시 그것을 따라갈 것

- content-box : 콘텐츠 영역만 width 값을 지정(기본값)

### 4.1.3. 박스 모델에 그림자 효과를 주는 box-shadow 속성

- box-shadow : 수평거리 수직거리 흐림정도 번짐정도 색상 inset
  - 로 구분
- 수평거리
- 수직거리
- 흐림정도
- 번짐정도
- 색상 : 한가지 또는 공백으로 구분 / 여러색상 가능
- inset: 그림자 안쪽으로

## 4.2. 테두리 스타일 지정하기

### 4.2.1. 박스 모델의 방향 살펴보기

- top > right > bottom > left 방향으로 움직임(시계 방향)
  - margin : 4px 4px 4px 4px; 이런거

### 4.2.3. 테두리 스타일을 지정하는 border-style 속성

- border : 1px solid red;
  - none : 테두리 없음
  - hidden : 테두리 감춤
  - solid : 실선
  - dotted : 점선
  - dashed : 하이푼으로 선이 되어있는것(짧은 직선)
  - double : 이중선
    - 두선 사이에 간격은 border-width 값으로 줌.
  - groove : 홈이 파인 듯 입체 느낌
  - inset : 표에서 사용
  - outset : 표에서 사용
  - ridge : 튀어 나온 듯한 입체느낌
