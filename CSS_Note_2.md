* 속성-typography
    * em 폰트의 전체 높이를 의미합니다.
    * ex ( = x-height ) 해당 폰트의 영문 소문자 x의 높이를 의미합니다.
    * Baseline 소문자 x를 기준으로 하단의 라인을 의미합니다.
    * Descender 소문자에서 baseline 아래로 쳐지는 영역을 의미합니다. 서체에 따라 descender의 길이가 다릅니다. ( g, j, p, q, y )
    * Ascender 소문자 x의 상단 라인 위로 넘어가는 영역을 의미합니다. ( b, d, h, l )

* 속성-font-family
    ```css
    font-family: family-name | generic-family ( | initial | inherit );
    ```
    * family-name : 폰트 이름
    * generic-family : 폰트가 없을시 적용 하는 폰트
    ```css
    h1 {
        font-family: Helvetica, Dotum, '돋움', Apple SD Gothic Neo, sans-serif;
    } 
    ```

* 속성-line-height
    ```css
    line-height: normal | number | length | initial | inherit ;
    ```
    * line-height 텍스트 라인의 높이를 의미하는 것으로 주로 행간을 제어할 때 사용됩니다.
    * normal 기본값으로 브라우저의 기본 속성을 따릅니다.
    폰트에 따라 브라우저에 따라 다르지만 보통 1.2 정도로 할당되어 있습니다.
    * number font-size를 기준으로 설정한 숫자만큼 배율로 적용합니다.
    * length px, em 등 고정 수치로 할당할 수 있습니다.
    * % font-size를 기준으로 설정한 퍼센트만큼 배율로 적용합니다.

    ```css
    body { 
        font-size: 20px; 
        line-height: 2;
    }       /* line-height = 40px; */
    body { 
        font-size: 20px; 
        line-height: 200%; 
    }    /* line-height = 40px; */
    ```

* 속성-font-size
    ```css
    font-size: keyword | length | initial | inherit ;
    ```
    * keyword medium(기본 값), xx-small, x-small, small, large, x-large, xx-large, smaller, larger
    * length px, em 등 고정 수치로 지정합니다.
    * % 부모 요소의 font-size 기준의 퍼센트로 지정합니다.
    * absolute size (keyword) 기본 값인 medium에 대한 상대적인 크기로, 브라우저마다 사이즈가 다르게 정의되어있습니다.
    * relative size (keyword) 부모 요소의 font-size 크기에 대해 상대적입니다. smaller는 0.8배, larger는 1.2배입니다.
    * length px, em, rem 등의 단위를 이용하여 고정된 크기를 지정할 수 있습니다. - em :  부모 요소의 font-size에 em 값을 곱한 크기 - rem : 루트의 font-size에 rem 값을 곱한 크기
    * percent (%) 부모 요소의 font-size를 기준으로 백분율 계산된 값을 지정할 수 있습니다.
    * viewport units vw, vh 단위로 뷰포트를 기준으로 하여, 유동적인 font-size를 지정할 수 있습니다. vw는 뷰포트 width의 1%, vh는 뷰포트 height의 1% 값을 가집니다.

* 속성-font-weight
    ```css
    font-weight: normal | bold | bolder | lighter | number | initial | inherit ;
    ```
    * normal 기본 값 (400)
    * bold 굵게 표현(700)
    * bolder 부모 요소 보다 두껍게 표현
    * lighter 부모 요소 보다 얇게 표현
    * number 100, 200, 300, 400, 500, 600, 700, 800, 900 (클수록 더 두껍게 표현)

* 속성-font-style
    ```css
    font-style: normal | italic | oblique | initial | inherit;
    ```
    * normal font-family 내에 분류된 기본 값
    * italic italic 스타일로 표현합니다.
    * oblique oblique 스타일로 표현합니다.

* 속성-font-variant
    ```css
    font-variant: normal | small-caps | initial | inherit ;
    ```
    * normal 기본 값
    * small-caps 소문자를 작은 대문자로 변형합니다.

* 속성-font
    ```css
    font: font-style font-variant font-weight font-size/line-height font-family | initial | inherit;
    ```
    * font-style font-style 지정, 기본 값은 normal
    * font-variant font-variant 지정, 기본 값은 normal
    * font-weight font-weight 지정, 기본 값은 normal
    * font-size/line-height font-size/line-height 지정, 기본 값은 normal
    * font-family font-family 지정
    * font-size와 font-family는 반드시 선언해야 하는 필수 속성입니다.
    * 빠진 속성이 있다면 기본 값으로 지정됩니다.
    * 각 속성의 선언 순서를 지켜야 합니다.

* 속성-webfont
    ```css
    @font-face { 
    font-properties 
    }
    ```
    * font-family(필수) 글꼴의 이름을 지정
    * src(필수) 다운로드 받을 글꼴의 경로(URL)
    * font-style(옵션) 글꼴의 스타일 지정, 기본 값은 normal
    * font-weight(옵션) 글꼴의 굵기 지정, 기본 값은 normal

* 속성-vertical-align
    ```css
    vertical-align: keyword | length | percent | initial | inherit ;
    ```
    * length 요소를 지정한 길이만큼 올리거나 내림. 음수 허용
    * % 요소를 line-height를 기준으로 올리거나 내림. 음수 허용
    * keyword baseline(기본 값), sub, super, top, text-top, middle, bottom, text-bottom

* 속성-text-align
    ```css
    text-align: left | right | center | justify | initial | inherit ;
    ```
    * left 텍스트를 왼쪽으로 정렬
    * right 텍스트를 오른쪽으로 정렬
    * center 텍스트를 중앙으로 정렬
    * justify 텍스트를 라인 양쪽 끝으로 붙여서 정렬. (마지막 라인은 정렬 하지 않음)
    * text-align은 inline-level에 적용
    * text-align은 block-level에 적용할 수 없음

* 속성-text-indent
    ```css
    text-indent: length | initial | inherit;
    ```
    * length px, em 등 고정 수치로 지정. 음수 허용
    * % 부모 요소의 width를 기준으로 퍼센트로 지정

* 속성-text-decoration
    ```css
    text-decoration: text-decoration-line text-decoration-color text-decoration-style | initial | inherit;
    ```
    * none 텍스트 꾸밈을 생성하지 않음 ( 기본값 )
    * underline 밑줄로 꾸밈을 설정
    * overline 윗줄로 꾸밈을 설정
    * line-through 중간을 지나는 줄로 꾸밈을 설정
    * text-decoration-color 텍스트 꾸밈의 색상을 지정하는 속성입니다.    
    * text-decoration-style 꾸밈에 사용되는 선의 스타일을 지정하는 속성입니다.
    * solid 한줄 스타일 ( 기본 값 )
    * double 이중선 스타일
    * dotted 점선 스타일
    * dashed 파선 스타일
    * wavy 물결 스타일

* 속성-단어 관련 속성
    * white-space 속성
        ```css
        white-space: normal | nowrap | pre | pre-line | pre-wrap | initial | inherit;
        ```
        * normal 공백과 개행을 무시하고, 필요한 경우에 자동 줄바꿈 발생. 기본 값
        * nowrap 공백과 개행을 무시하고, 자동 줄바꿈이 일어나지 않음.
        * pre 공백과 개행을 표현하고, 자동 줄바꿈이 일어나지 않음.
        * pre-line 공백은 무시하고, 개행만 표현. 필요한 경우에 자동 줄바꿈 발생.
        * pre-wrap 개행은 무시하고, 공백만 표현. 필요한 경우 자동 줄바꿈 발생.

    * letter-spacing 속성
        ```css
        letter-spacing: normal | length | initial | inherit;
        ```
        * normal 기본 값
        * length 길이만큼 자간을 지정. 음수 허용

    * word-spacing 속성
        ```css
        word-spacing: normal|length|initial|inherit;
        ```
        * normal 기본 값
        * length 길이만큼 단어 사이의 간격을 지정. 음수 허용

    * word-break 속성
        ```css
        word-break: normal | break-all | keep-all | initial | inherit;
        ```
        * normal 기본 값. 중단점은 공백이나 하이픈(-)(CJK는 음절)
        * break-all 중단점은 음절. 모든 글자가 요소를 벗어나지 않고 개행
        * keep-all 중단점은 공백이나 하이픈(-)(CJK는 그 외 기호도 포함)

    * word-wrap 속성
        ```css
        word-wrap: normal|break-word|initial|inherit;
        ```
        * normal 기본 값. 중단점에서 개행
        * break-word 모든 글자가 요소를 벗어나지 않고 강제로 개행

* 속성-display
    ```css
    display: value;
    ```
    * none 요소가 렌더링 되지 않음
    * inline inline level 요소처럼 렌더링
    * block block level 요소처럼 렌더링
    * inline-block inline level 요소처럼 렌더링(배치)되지만 block level의 성질을 가짐
    * height 나 width 등과 같은 박스모델 속성을 적용할 수 있다

    |display|width|height|margin|padding|border
    |--|--|--|--|--|--|--|
    |block|o|o|o|o|o|o|
    |inline|x|x|좌/우|o|o|o|
    |inline-block|o|o|o|o|o|o|