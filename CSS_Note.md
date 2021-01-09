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

    * 속성 선택자
        * 단순 속성
        ```css
        p[class] { 
            color: silver; 
        }
        ```
        ```css
        p[class][id] {
             text-decoration: underline; 
        }
        ```

        * 정확한 속성값
        ```css
        p[class="foo"] {
             color: silver; 
        }
        ```
        ```css
        p[id="title"] {
             text-decoration: underline; 
        }
        ```

        * 부분 속성값
        ```html
        <p class="color hot">red</p>
        <p class="cool color">blue</p>
        <p class="colorful nature">rainbow</p>
        ```
        ```css
        p[class~="color"] { font-style: italic; } /* 1, 2번째 요소 */
        p[class^="color"] { font-style: italic; } /* 1, 3번째 요소 */
        p[class$="color"] { font-style: italic; } /* 2번째 요소 */
        p[class*="color"] { font-style: italic; } /* 1, 2, 3번째 요소 */
        ```

    * 문서 구조 관련 선택자
        ```html
        <html>
        <body>
            <div>
                <h1><span>HTML</span>: Hyper Text Markup Language</h1>
            </div>
            <p>HTML과 CSS와 JAVASCRIPT를 이용해서 멋진 웹 사이트를 제작할 수 있습니다.</p>
        </body>
        </html>
        ```
        * 부모와 자식

            ```<body>```의 부모 요소: ```<html>``` ↔ ```<html>```의 자식 요소: ```<body>```
            
            ```<div>```의 부모 요소: ```<body>``` ↔ ```<body>```의 자식 요소: ```<div>```, ```<p>```
            
            ```<h1>```의 부모 요소: ```<div>``` ↔ ```<div>```의 자식 요소: ```<h1>```
            
            ```<span>```의 부모 요소: ```<h1>``` ↔ ```<h1>```의 자식 요소: ```<span>``` 
            
            ```<p>```의 부모 요소: ```<body>``` ↔ ```<body>```의 자식 요소: ```<div>```, ```<p>```

        * 조상과 자손

            ```<body>```의 조상 요소: ```<html>``` ↔ ```<html>```의 자손 요소: ```<body>```, ```<div>```, ```<h1>```, ```<span>```, ```<p>```

            ```<div>```의 조상 요소: ```<html>```, ```<body>``` ↔ ```<body>```의 자손 요소: ```<div>```, ```<h1>```, ```<span>```, ```<p>```

            ```<h1>```의 조상 요소: ```<html>```, ```<body>```, ```<div>``` ↔ ```<div>```의 자손 요소: ```<h1>```, ```<span>```

            ```<span>```의 조상 요소: ```<html>```, ```<body>```, ```<div>```, ```<h1>``` ↔ ```<h1>```의 자손 요소: ```<span>```

            ```<p>```의 조상 요소: ```<html>```, ```<body>``` ↔ ```<body>```의 자손 요소: ```<div>```, ```<h1>```, ```<span>```, ```<p>```

        * 형제

            ```<div>```, ```<p>```

    * 문서 구조 선택자
        * 자손 선택자
            ```css
            div span {
                 color: red; 
            }
            ```

        * 자식 선택자
            ```css
            div > h1 {
                color: red; 
            }
            ```

        * 인접 형제 선택자
            ```css
            div + p {
                 color: red; 
            }
            ```
            ```css
            /* body 요소의 자식인 div 요소의 자손인 table 요소 바로 뒤에 인접한 ul 요소 선택! */

            body > div table + ul { ... }
            ```

    * 가상 선택자
        * 가상 클래스(pseudo class)
            ```css
            :pseudo-class {
                property: value;
            }
            ```

        * 문서 구조와 관련된 가상 클래스
            ```html
            <ul>
                <li>HTML</li>
                <li>CSS</li>
                <li>JS</li>
            </ul>
            ```
            ```css
            li:first-child { 
                color: red; 
            }
            li:last-child { 
                color: blue; 
            }
            ```

        * 앵커 요소와 관련된 가상 클래스
            ```css
            a:link {
                 color: blue; 
            }
            a:visited {
                 color: gray; 
            }
            ```

        * 사용자 동작과 관련된 가상 클래스
            ```css
            a:focus { 
                background-color: yellow; 
            }
            a:hover { 
                font-weight: bold; 
            }
            a:active { 
                color: red; 
            }
            ```

        * 가상 요소(pseudo element)
            ```css
            ::pseudo-element {
                property: value;
            }
            ```
            :before : 가장 앞에 요소를 삽입
            ```css
            p::before {
                content: "###" 
            }
            ```
            :after : 가장 뒤에 요소를 삽입
            ```css
            p::after { 
                content: "!!!" 
            }
            ```
            :first-line : 요소의 첫 번째 줄에 있는 텍스트
            ```css
            p::first-line { ... }
            ```            
            :first-letter : 블록 레벨 요소의 첫 번째 문자
            ```css
            p::first-letter { ... }
            ```

    * 구체성
         ```css
         h1 { 
             color: red; 
         }
         body h1 { 
             color: green; 
         }
         ```

    * 인라인 스타일
        ```html
        <p id="page" style="color:blue">Lorem impusm dolor sit.</p>
        ```
    * important
        ```css
        p#page { 
            color: red !important; 
        }
        ```
        ```html
        <p id="page" style="color:blue">Lorem impusm dolor sit.</p>
        ```
    * 상속되는 속성
        ```css
        h1 {
             color: gray; 
        }
        ```
        ```html
        <h1>Hello, <em>CSS</em></h1>
        ```
    * 상속되는 속성의 구체성
        ```css
        * { 
            color: red; 
        }
        h1#page {
            color: gray; 
        }
        ```
        ```html
        <h1 id="page">Hello, <em>CSS</em></h1>
        ```

    * cascading 규칙 
        * 중요도(!important)와 출처
        * 구체성
        * 선언 순서

* 속성 - 단위
    * 절대 길이
        * px ( 1px = 1/96th of 1 inch )
        * pt ( 1pt - 1/72 of 1 inch )

    * 상대 길이
        * % : 부모의 값에 대해서 백분율로 환산한 크기를 갖게 됩니다.
        * em : font-size를 기준으로 값을 환산합니다. 소수점 3자리까지 표현 가능합니다.
        * rem : root의 font-size를 기준으로 값을 환산합니다.
        * vw : viewport의 width값을 기준으로 1%의 값으로 계산됩니다.