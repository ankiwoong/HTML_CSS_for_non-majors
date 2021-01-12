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