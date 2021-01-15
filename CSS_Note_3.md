* 미디어 쿼리
    * 각 미디어 매체에 따라 다른 스타일 시트를 적용할 수 있게 만드는 것
    * CSS2 Media Type
        * https://www.w3.org/TR/CSS21/media.html%23media-types
        * 동일한 미디어 타입에서 광범위하게 적용
        * 미디어 타입을 제대로 지원하는 기기가 없음

* 미디어 타입 & 미디어 특성
    ```css
    @media mediaqueries { /* style rules  */ }
    ```
    * all, braille, embossed, handheld, print, projection, screen, speech, tty, tv

* Syntax - 1
    ```
    media_query_list
    : S* [media_query [ ',' S* media_query ]* ]?
    ;
    media_query
    : [ONLY | NOT]? S* media_type S* [ AND S* expression ]*
    | expression [ AND S* expression ]*
    ;
    expression
    : '(' S* media_feature S* [ ':' S* expr ]? ')' S*
    ;
    ```
    * [ a ] : a가 나올 수도 있고 나오지 않을 수도 있습니다.
    * a | b : a 또는 b 둘 중에 하나를 선택합니다.
    * "|"는 파이프 라인 기호로 키보드의 역슬래시(\) 키를 Shift 키를 누른 채로 누르면 나옵니다.
    * a? :  a가 0번 나오거나 1번만 나올 수 있음
    * a* : a가 0번 나오거나 그 이상 계속 나올 수 있음
    * media_type : all, screen, print 등 명세에 정의된 미디어 타입
    * media_feature : width, orientation 등 명세에 정의된 미디어 특성
    * min-/max- 접두사
        ```
        @media screen { ... }
        : 미디어 타입이 screen이면 적용됩니다.

        @media screen and (min-width: 768px) { ... }
            : 미디어 타입이 screen이고 width가 768px 이상이면 적용됩니다. 두 개 중 하나라도 만족하지 않으면 거짓이 됩니다.

        @media (min-width: 768px) and (max-width: 1024px) { ... }
            : and는 연결된 모든 표현식이 참이면 적용됩니다.(and 키워드는 연결된 부분이 모두 참이어야 적용이 됩니다.)

        @media (color-index)
            : 미디어 장치가 color-index를 지원하면 적용됩니다.

        @media screen and (min-width: 768px), screen and (orientation: portrait), ...
            : 쉼표로 연결된 미디어 쿼리 중 하나라도 참이면 적용됩니다.( and 키워드와 반대라고 생각하면 됩니다.)

        @media not screen and (min-width: 768px)
            : not 키워드는 하나의 media_query 전체를 부정합니다.
            : (not screen) and (min-width: 768px) 잘못된 해석!
            : not (screen and (min-width: 768px)) 올바른 해석!
            : @media not screen and (min-width: 768px), print
            첫 번째 미디어 쿼리에만 not 키워드가 적용되며, 두 번째 미디어 쿼리(print)에는 영향이 없습니다.
        ```
    * 미디어 쿼리 선언 방법
        ```
        @media screen and (color)
        : CSS 파일 내부에 또는 <style> 태그 내부에 사용가능 합니다. 대부분의 경우 이렇게 사용합니다.

        <link rel="stylesheet" media="screen and (color)" href="example.css">
        : <link> 태그의 media 속성에 미디어 쿼리를 선언합니다. 미디어 쿼리가 참이면 뒤에 css 파일 규칙이 적용됩니다.

        @import url(example.css) screen and (color);
            : CSS 파일 내부에 또는 <style> 태그 내부에 사용가능 합니다. @import문 뒤에 미디어 쿼리를 선언하면 됩니다.
        ```

* Syntax - 2
    ```
    media_query_list
    : S* [media_query [ ',' S* media_query ]* ]?
    ;
    media_query
    : [ONLY | NOT]? S* media_type S* [ AND S* expression ]*
    | expression [ AND S* expression ]*
    ;
    expression
    : '(' S* media_feature S* [ ':' S* expr ]? ')' S*
    ;
    ```
    * [ a ] : a가 나올 수도 있고 나오지 않을 수도 있습니다.
    * a | b : a 또는 b 둘 중에 하나를 선택합니다.
    * "|"는 파이프 라인 기호로 키보드의 역슬래시(\) 키를 Shift 키를 누른 채로 누르면 나옵니다.
    * a? :  a가 0번 나오거나 1번만 나올 수 있음
    * a* : a가 0번 나오거나 그 이상 계속 나올 수 있음
    * media_type : all, screen, print 등 명세에 정의된 미디어 타입
    * media_feature : width, orientation 등 명세에 정의된 미디어 특성

    ```
    @media screen { ... }
    : 미디어 타입이 screen이면 적용됩니다.

    @media screen and (min-width: 768px) { ... }
        : 미디어 타입이 screen이고 width가 768px 이상이면 적용됩니다. 두 개 중 하나라도 만족하지 않으면 거짓이 됩니다.

    @media (min-width: 768px) and (max-width: 1024px) { ... }
        : and는 연결된 모든 표현식이 참이면 적용됩니다.(and 키워드는 연결된 부분이 모두 참이어야 적용이 됩니다.)

    @media (color-index)
        : 미디어 장치가 color-index를 지원하면 적용됩니다.

    @media screen and (min-width: 768px), screen and (orientation: portrait), ...
        : 쉼표로 연결된 미디어 쿼리 중 하나라도 참이면 적용됩니다.( and 키워드와 반대라고 생각하면 됩니다.)

    @media not screen and (min-width: 768px)
        : not 키워드는 하나의 media_query 전체를 부정합니다.
        : (not screen) and (min-width: 768px) 잘못된 해석!
        : not (screen and (min-width: 768px)) 올바른 해석!
        : @media not screen and (min-width: 768px), print
        첫 번째 미디어 쿼리에만 not 키워드가 적용되며, 두 번째 미디어 쿼리(print)에는 영향이 없습니다.
    ```
    ```
    @media screen and (color)
    : CSS 파일 내부에 또는 <style> 태그 내부에 사용가능 합니다. 대부분의 경우 이렇게 사용합니다.

    <link rel="stylesheet" media="screen and (color)" href="example.css">
    : <link> 태그의 media 속성에 미디어 쿼리를 선언합니다. 미디어 쿼리가 참이면 뒤에 css 파일 규칙이 적용됩니다.

    @import url(example.css) screen and (color);
        : CSS 파일 내부에 또는 <style> 태그 내부에 사용가능 합니다. @import문 뒤에 미디어 쿼리를 선언하면 됩니다.
    ```

* 실습 - 1
    * 디스플레이 크기에 따른 body요소의 background-color 변경
        * 조건 사항
            ```
            0~767px 이면 : mobile | gold
            768px~1024px 이면 : tablet | lightblue
            1025px~ 이면 : desktop | lightpink
            ```
        * mobile first
        * desktop first