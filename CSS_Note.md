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

* 속성
    * 단위
        * 절대 길이
            * px ( 1px = 1/96th of 1 inch )
            * pt ( 1pt - 1/72 of 1 inch )

        * 상대 길이
            * % : 부모의 값에 대해서 백분율로 환산한 크기를 갖게 됩니다.
            * em : font-size를 기준으로 값을 환산합니다. 소수점 3자리까지 표현 가능합니다.
            * rem : root의 font-size를 기준으로 값을 환산합니다.
            * vw : viewport의 width값을 기준으로 1%의 값으로 계산됩니다.

    * 속성
        * 색상 값 지정 방식
            * 컬러 키워드 : transparent는 투명을 나타내는 키워드 
            * 16진법 : #RRGGBB / #RGB
            * RGB( )
            * RGBA( )

    * 속성-background
        * background 관련 속성
            ```
            background: [-color] [-image] [-repeat] [-attachment] [-position];
            ```
            * background-color
            * background-image
            * background- repeat
            * background-position
            * background-attachment

    * 속성-boxmodel
        * Content 영역
            * Border
            * Padding
            * Margin

    * 속성-border
        * border 관련 속성
            * border-width
                ```css
                border-width: [top] [right] [bottom] [left];
                ```

            * border-style 기본 값
                ```css
                border-style: [top] [right] [bottom] [left];
                ```

            * border- color 기본 값
                ```css
                border-color: [top] [right] [bottom] [left];
                ```
            
            * border 축약
                ```css
                border: [-width] [-style] [-color];
                ``` 

    * 속성-padding
        * padding 속성
            ```css
            padding: [-top] [-right] [-bottom] [-left];
                   0      10px     20px      30px   /* 상, 우, 하, 좌 다름 */
                   0      10px     20px                 /* 좌, 우 같음 */
                   0      10px                              /* 상, 하 같음 & 좌, 우 같음 */
                   0                                            /* 상, 우, 하, 좌 모두 같음 */
            ```
            * length 고정값으로 지정합니다. (ex. px, em ....)
            * percent 요소의 width에 상대적인 크기를 지정합니다.
            * padding-top content 영역의 위쪽 여백을 지정합니다.
            * padding-right content 영역의 오른쪽 여백을 지정합니다.
            * padding-bottom content 영역의 아래쪽 여백을 지정합니다.
            * padding-left content 영역의 왼쪽 여백을 지정합니다.

    * 속성-margin
        * margin 속성
            ```css
            margin: [-top] [-right] [-bottom] [-left];
                  0      10px     20px      30px   /* 상, 우, 하, 좌 다름 */
                  0      10px     20px                 /* 좌, 우 같음 */
                  0      10px                              /* 상, 하 같음 & 좌, 우 같음 */
                  0                                            /* 상, 우, 하, 좌 모두 같음 */
            ```
            * margin-top border 영역의 위쪽 여백을 지정합니다.
            * margin-right border 영역의 오른쪽 여백을 지정합니다.
            * margin-bottom border 영역의 아래쪽 여백을 지정합니다.
            * margin-left border 영역의 왼쪽 여백을 지정합니다.
            * margin auto 기본적으로 브라우저에 의해 계산이 이루어지는데, 대부분의 경우 0(기본값) 또는 요소의 해당 측면에서 사용 가능한 공간과 같은 값을 가집니다. 이를 활용하여 수평 중앙 정렬을 할 수 있습니다. 아래 코드를 살펴봅시다.

        * margin collapse(마진 병합)
            * 두 요소가 상하로 인접한 경우: 위 요소의 하단 마진과 아래 요소의 상단 마진의 병합이 일어납니다.
            * 부모 요소와 첫 번째 자식 요소 또는 마지막 자식 요소
                * 부모 요소의 상단 마진과 첫 번째 자식 요소의 상단 마진 병합이 일어납니다.
                * 부모 요소의 하단 마진과 마지막 자식 요소의 하단 마진 병합이 일어납니다.
            * 내용이 없는 빈 요소의 경우: 해당 요소의 상단 마진과 하단 마진의 병합이 일어납니다.

    * 속성-margin&padding
        * 비교

            ||+|-|auto|단위|
            |----|---|---|---|---|
            |margin|o|o|o|px, %|
            |padding|o|x|x|px, %|

            * 음수값 사용 여부
            * % 값의 사용과 기준점

    * 속성-width
        * width 속성
            * auto 브라우저에 의해 자동으로 계산하여 적용합니다. ~ 요소의 레벨 기본 특성에 따라 다르게 동작합니다.
            * length 고정값으로 지정합니다. (ex. px, em ....)
            * percent 부모 요소의 width에 상대적인 크기를 지정합니다.

        * 계산방법
            * Ex 1>
                ```html
                <div class="box"> box </div>
                ```
                ```css 
                .box {
                width: 100px;
                padding: 20px;
                border: 10px solid black;
                }
                ```
                100px content + (20px * 2) padding + (10px * 2) border = 160px

                width(Content) + (padding * 2(좌우)) + (border * 2(좌우)) = 박스사이징

            * Ex 2>
                ```html
                <div class="parent">
                <div class="child">
                    child
                </div>
                </div>
                ```
                ```css
                .parent {
                width: 300px;
                border: 20px solid red;
                }
                .child {
                width: 50%;
                padding: 20px;
                border: 10px solid black;
                }
                ```
                padding (20px * 2) + border (10px * 2) = 60px<br>
                210px - 60px = 150p

    * 속성-height
        * height 속성
            * auto 브라우저 자동으로 계산하여 적용합니다. ~ 기본적으로 컨텐츠 영역의 내용만큼 높이를 가집니다.
            * length 고정값으로 지정합니다. (ex. px, em ....)
            * percent 부모 요소의 height에 상대적인 크기를 지정합니다. * 단, 부모 요소가 명시적으로 height 값이 있어야 합니다.

        * 계산방법
            * Ex 1>
                ```html
                <div class="box"> box </div>
                ```
                ```css
                .box {
                width: 100px;
                height: 100px;
                padding: 10px;
                border: 15px solid black;
                }
                ```
                100px content + ( 10px * 2) padding + ( 15px * 2 ) border = 150px 

                height + (padding * 2(상하)) + (border * 2(상하)) = 박스사이징

            * Ex 2>
                ```html
                <div class="parent">
                <div class="child">
                    child
                </div>
                </div>
                ```
                ```css
                .parent {
                width: 200px;
                border: 10px solid black;
                }
                .child {
                height: 50%;
                background: red;
                } 
                ```
                % -> height : 200px