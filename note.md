* Hyper Text Markup Language
    * 웹 페이지지를 만드는 언어
    * Hyper Text(링크)
    * Markup Language
    * 확장자가 html

* HTML 문법
    * 태그
    ```html
    <h1>Hello, HTML</h1>
    ```
    * 속성
    ```html
    <h1 id="title">Hello, HTML</h1>
    ```
    * 태그의 중첩
    ```html
    <h1>Hello, <i>HTML</i></h1>
    ```
    * 빈 태그
    ```html
    <br>
    <img src="">
    ```
    * 공백
    ```html
    <h1>Hello, HTML</h1>
    <h1>Hello   HTMML</h1>
    <h1>
        Hello,
        HTML
    </h1>
    ```
    * 주석
    ```html
    <!-- 여기에 작성되는 내용들은 모두 주석 처리가 됩니다. -->
    <!-- 주석은 여러 줄로 작성할 수도 있습니다.
        <h1>Hello, HTML</h1>
        위 <h1>태그는 브라우저가 해석하지 않습니다.
    -->
    ```

    * HTML 문서 구조(HTML DOcUMENTS)
    ```html
    <!DOCTYPE html>
    <html lang="ko">
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <h1>Hello, HTML</h1>
        </body>
    </html>
    ```

* HTML 태그
    * 제목 태그
    ```html
    <h1>역사</h1>
    <h2>개발</h2>
    1980년, 유럽 입자 물리 연구소(CERN)의 계약자였었던 물리학자 팀 버너스리가 HTML의 원형인 인콰이어를 제안하였다.
    ... 이하 생략
    <h2>최초 규격</h2>
    HTML 최초의 일반 공개 설명은 1991년 말에 버너스리가 처음으로 인터넷에서 문서를 "HTML 태그"(HTML tag)로 부르면서 시작되었다.
    ... 이하 생략
    ```

    * 단락 태그
    ```html
    <h1>역사</h1>
    <h2>개발</h2>
    <p>
        1980년, 유럽 입자 물리 연구소(CERN)의 계약자였었던 물리학자 팀 버너스리가 HTML의 원형인 인콰이어를 제안하였다.
        ... 이하 생략
    </p>
    <h2>최초 규격</h2>
    <p>
        HTML 최초의 일반 공개 설명은 1991년 말에 버너스리가 처음으로 인터넷에서 문서를 "HTML 태그"(HTML tag)로 부르면서 시작되었다.
        ... 이하 생략
    </p>
    ```

    * 개행 태그
    ```html
    <p></p>

    <br>
    ```

    * 텍스트 표현 태그
    ```html
    <p>
        <b>Lorem</b> <i>ipsum</i> dolor sit amet<br>
        <u>Lorem</u> <s>ipsum</s> dolor sit amet
    </p>
    ```

    * ```<a>```
    ```html
    <a href="http://www.naver.com/" target="_blank">네이버</a>
    ```

    * 내부링크
    ```html
    <a href="#some-element-id">회사 소개로 이동하기</a>

    ... 중략.

    <h1 id="some-element-id">회사 소개</h1>
    ```

    * 컨테이너 요소
    ```html
    <div>
        <span>Lorem</span> ipsum dolor sit.
    </div>
    ```

    * ```<ul>```
    ```html
    <ul> 
        <li> 콩나물</li> 
        <li> 파</li> 
        <li> 국  간장</li> 
        ... 
    </ul>
    ```