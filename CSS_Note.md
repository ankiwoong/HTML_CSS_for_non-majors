* CSS(Cascading Style Sheets)
    * HTML 꾸며주는 언어
    * 디자인
    * http://www.csszengarden.com/

* CSS 문법과 적용
    * CSS 구문
        ```css
        h1 { 
            color: yellow;
            font-size:2em; 
        }
        ```
        * 선택자(selector) - "h1"
        * 속성(property) - "color"
        * 값(value) - "yellow"
        * 선언(declaration) - "color: yellow", "font-size: 2em"
        * 선언부(declaration block) - "{ color: yellow; font-size:2em; }"
        * 규칙(rule set) - "h1 { color: yellow; font-size:2em; }"

* CSS 주석(Comment Tags)
    * Inline
    ```css
    /* 주석 내용 */
    /*
        주석은 여러 줄로도
        선언 할 수 있습니다.
    */
    ```

* CSS의 적용
    * Inline
    ```html
    <div style="color:red;"> 내용 </div>
    ```

    * Internal
    ```html
    <style>
    div {
        color: red;
    }
    </style>
    ```

    * External
    ```css
    div {
        color: red;
    }
    ```
    ```html
    <link rel="stylesheet" href="css/style.css">
    ```

    * Import
    ```html
    <style>
    @import url("css/style.css"); 
    </style>
    ```