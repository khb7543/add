# HTML

## HTML Introduction

https://www.w3schools.com/html/html_intro.asp

> HTML : Hyper Text Markup Language
>
> - 버전 : HTML5(HTML 5.2) - 표준화 2014
> - 웹페이지의 콘텐츠 표시
> - 웹페이지 구조 표시

## HTML Element

https://www.w3schools.com/html/html_elements.asp

- 콘텐츠를 표시하는 언어 : 태그
- 시작태그 + 콘텐츠 + 종료태그 : Element(요소)

```
문법
<tagname>Contents</tagname>

콘텐츠, 종료태그 없는 요소 : 빈요소(Empty Element)
<br>
```

> Nested Element(중첩, 포함관계)

```
<section>
  <div>
    <p>텍스트</p>
  </div>
</section>

1. p 태그 기준
- 포함하는 요소
    - div : 부모요소(parent)
    - section : 조상요소(ancestor)

2. div 태그 기준
- 포함하는 요소 : section - 부모요소
- 포함되는 요소 : p - 자식요소(children)

3. section 태그 기준
- 포함되는 요소
  - div : 자식요소
  - p : 자손요소(descendant)
```

## HTML 기본 구조

```
<!DOCTYPE html> : 웹 문서 종류 표시
<html> : html 문서 영역을 표시
  <head>  : 웹 페이지 관련 정보, 파일 정보등의 내용이 표시되는 영역
  </head>
  <body> : 웹 페이지 콘텐츠, 구조가 표시되는 영역
  </body>
</html>
```

## HTML Attribute(속성)

https://www.w3schools.com/html/html_attributes.asp

- HTML Elment에 추가 정보를 제공
- 시작태그에 작성
- name="value" 형식으로 구성

## HTML Contents 표시 Element

> - Text Contents
>   - 제목, 단락, 목록, 링크, 테이블(표)
> - Multimedia Contents / Embeded Contents
>   - 이미지, 비디오, 오디오

### HTML Heading

https://www.w3schools.com/html/html_headings.asp

- h : (h)eading : 제목 표시 태그
- h1 ~ h6 : h1 - 가장 큰 제목

### HTML Paragraph

https://www.w3schools.com/html/html_paragraphs.asp

- p : (p)aragraph - 단락 표시 태그
- br : line (br)eak - 강제 줄바꿈 태그 / 빈 요소(Empty Element)
- &nbsp; : (N)on-(B)reak (Sp)ace - Entity code
- hr : (H)orozontal (R)ule - 수평선 / 빈 요소(Empty Element)

### HTML link

https://www.w3schools.com/html/html_links.asp

- 다른 페이지로 연결
- a : (a)nchor
- href : Hypertext Reference : 웹페이지 참조주소

```
<a href="이동할웹페이지의url" target="_blank">링크이름</a>

target="_blank" : 새 창(탭) 열기
```

### HTML list

https://www.w3schools.com/html/html_lists.asp

- 순서없는 목록 : ul - (U)nordered (L)ist
- 순서있는 목록 : ol - (O)rdered (L)ist
- 목록 항목 : li - (L)ist (I)tem
- 설명 목록
  - dl : (D)escription (L)ist
  - dt : (D)escription (T)itle
  - dd : (D)escription (D)ata
- 원하는 목록의 형태 : 직접 입력해서 사용

```
<ul>
  <li>항목 내용</li>
</ul>

<ol>
  <li>항목 내용</li>
</ol>

<dl>
  <dt>목록 주제(제목)</dt>
  <dd>주제에 대한 설명</dd>
</dl>
```

### HTML Table

- HTML table generator

https://www.tablesgenerator.com/html_tables

### HTML Image

- img : 이미지 첨부
- src : (s)ou(rc)e - 이미지 경로/이름
- alt : (alt)ernative - 대체 텍스트


### HTML Video

- video
- controls, autoplay, loop, muted
  - HTML5에서 추가된 속성 : 속성 이름만 사용
  - 사용 여부에 대한 표시
- autoplay 적용시 muted를 같이 적용해야 하는 경우를 고려해야함


```
controls="true" => controls
```

### Youtube Video

## HTML Structure

- 웹페이지의 영역구분 / 배치

> 웹페이지의 HTML Contents별 영역 구분 : HTML
>
> 구분된 영역의 배치 : CSS

- 영역 배치의 흐름
  - 세로, 가로 방향 모두 한 가지로 연결되는 흐름 구성
  - 세로 흐름이 가로 흐름보다 우선되어야 함

### HTML Semantic Element
https://www.w3schools.com/html/html5_semantic_elements.asp

- Semantic Element
  - 영역 구분하는 Element를 의미를 부여해서 사용

```
<header></header> : 로고, 로그인, 메뉴 상단 내용
<nav></nav> : (nav)igation - 메뉴
<section></section> : Contents
<article></article> : Contents
<aside></aside> : 부수적인 contents(광고)
<footer></footer> : 하단 페이지 contents(개인정보처리방침, 이용약관, 사이트맵)
<figure></figure> : 비주얼 Contents
```

### HTML Container Element(non-semantic)

- div : (div)ision
- span
  - 의미있게 사용하지 않고 단순히 Group화 할 때 사용

### HTML Block & Inline Element
https://www.w3schools.com/html/html_blocks.asp

- 화면에 표시되는 특성으로 구분하는 기준(디자인 기준)

> Block Element
>
> - 부모요소를 기준으로 좌우전체가 채워짐
> - 항상 줄바꿈되어 표시됨 => 세로방향으로 배치

> Inline Element
>
> - 자식요소의 크기 만큼 너비가 지정됨
> - 영역이 한 줄에 나란히 표시 => 가로방향으로 배치
> - 불필요한 여백이 존재
> - 박스모델이 적용되지 않음
> - HTML 페이지의 구조/레이아웃을 구성하는 데 사용하지 않음

```
(O)
<div>
  <span>Hello World</span>
</div>

(X)
<span>
  <div>Hello World</div>
</span>

(예외)
<a href="url">
  <div>Hello World</div>
</a>
```

### HTML File Path / URL
 
- URL : Uniform Resource Locator
 - File Identifier(파일 식별자)
 - 네트워크 상에서 자원(파일)의 위치를 표시하는 자세한 주소
 - 웹페이지를 찾기 위한 주소

 > 절대 경로 / URL 방식
```
Ex) 
택배주소 : 국가 - 시/도 - 시/군/구 - 동/읍/면 - 상세주소

- 출발위치에 상관없이 항상 최종 목적지에 도착할 수 있음
- 주소의 길이가 김
```
> 상대 경로 / URL 방식
```
Ex)
주소표시 : 필요에 따라 짧은 주소 표시

상세주소
동/읍/면 - 상세주소
시/군/구 - 동/읍/면 - 상세주소

- 출발위치에 따라서 최종 목적지 표시가 달라질 수 있음
- 주소 길이가 짧게 표시됨


photo.jpg
images/photo.jpg
../images/photo.jpg

- 기준 위치에 따라 필요한 경로/주소만 표시하는 것

- web - images - photo.jpg
      - html - page.html(photo.jpg 파일을 포함)

``` 

- 서버주소(도메인)부터 시작



