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

    * 요소 선택자
    ```css
    h1 { 
        color: yellow; 
    }
    h2 { 
        color: yellow; 
    }
    h3 { 
        color: yellow; 
    }
    h4 { 
        color: yellow; 
    }
    h5 { 
        color: yellow; 
    }
    h6 { 
        color: yellow; 
    }
    ```

    * 그룹화
    ```css
    h1, h2, h3, h4, h5, h6 {
        color: yellow; 
    }
    ```

    ```css
    * {
        color: yellow; 
    }
    ```

    ```css
    h1 { 
        color: yellow; 
        font-size: 2em; background-color: gray; 
    }
    ```

    ```css
    h1, h2, h3, h4, h5, h6 { 
        color: yellow; 
        font-size: 2em; background-color: gray; 
    }
    ```

    * class 선택자
    ```css
    .foo { 
        font-size: 30px; 
    }
    ```

    ```css
    .html { 
        color: purple; 
    }
    .css {
         text-decoration: underline; 
    }
    ```

    * 다중 class
    ```css
    .foo { 
        font-size: 30px; 
    }
    .bar {
        color: blue; 
    }
    ```

    * id 선택자
    ```css
    #bar {
        background-color: yellow; 
    }
    ```

    * 선택자의 조합
    ```html
    <style>
        /* 요소와 class의 조합 */
        p.bar { ... }

        /* 다중 class */
        .foo.bar { ... }

        /* id와 class의 조합 */
        #foo.bar { ... }
    </style>
    ```