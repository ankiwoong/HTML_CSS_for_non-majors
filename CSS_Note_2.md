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