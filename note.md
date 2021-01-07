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

    * ```<ol>```
    ```html
    <ol>
        <li>냄비에 국물용 멸치를 넣고 한소끔 끓여 멸치 육수를 7컵(1,400ml) 만든다.</li>
        <li>콩나물을 넣고 뚜껑을 덮어 콩나물이 익을 때까지 끓인다.</li>
        <li>뚜껑을 열고 대파, 마늘, 고춧가루를 넣고 끓인다.</li>
        ...
    </ol>
    ```

    * ```<dl>```
    ```html
    <dl>
        <dt>리플리 증후군</dt>
        <dd>허구의 세계를 진실이라 믿고 거짓된 말과 행동을 상습적으로 반복하는 반사회적 성격장애를 뜻하는 용어</dd>
        <dt>피그말리온 효과</dt>
        <dd>타인의 기대나 관심으로 인하여 능률이 오르거나 결과가 좋아지는 현상</dd>
        <dt>언더독 효과</dt>
        <dd>사람들이 약자라고 믿는 주체를 응원하게 되는 현상</dd>
    </dl>
    ```

    * ```<img>```
    ```html
    <img src="./images/pizza.png" alt="피자">
    ```

    * 상대경로와 절대경로
    ```html
    <!-- 상대경로 -->
    <img src="./images/pizza.png" alt="피자">

    <!-- 절대경로 -->
    <img src="C:/users/document/images/pizza.png" alt="피자">
    <img src="http://www.naver.com/pizza.png" alt="피자">
    ```

    * 표의 구성 요소
    ```html
    <head>
        <style>
            th, td { border: 1px solid; }
        </style>
    </head>
    <table>
        <tr>
            <td>1</td>
            <td>2</td>
            <td>3</td>
            <td>4</td>
        </tr>
        <tr>
            <td>5</td>
            <td>6</td>
            <td>7</td>
            <td>8</td>
        </tr>
        <tr>
            <td>9</td>
            <td>10</td>
            <td>11</td>
            <td>12</td>
        </tr>
        <tr>
            <td>13</td>
            <td>14</td>
            <td>15</td>
            <td>16</td>
        </tr>
    </table>
    ```

    * 표의 구조와 관련된 태그
    ```html
    <table>
        <caption>Monthly Savings</caption>
        <thead>
            <tr>
                <th>Month</th>
                <th>Savings</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>January</td>
                <td>$100</td>
            </tr>
            <tr>
                <td>February</td>
                <td>$80</td>
            </tr>
        </tbody>
        <tfoot>
            <tr>
                <td>Sum</td>
                <td>$180</td>
            </tr>
        </tfoot>
    </table>
    ```

    * 복잡한 표 만들기
    ```html
    <table>
        <caption>Specification values</caption>
        <thead>
        <tr>
            <th rowspan="2">Grade.</th>
            <th rowspan="2">Point.</th>
            <th colspan="2">Strength.</th>
            <th rowspan="2">Percent.</th>
        </tr>
        <tr>
            <th>kg/mm</th>
            <th>lb/in</th>
        </tr>
        </thead>
        <tbody>
        <tr>
            <td>Hard</td>
            <td>0.45</td>
            <td>56.2</td>
            <td>80,000</td>
            <td>20</td>
        </tr>
        <tr>
            <td>Medium</td>
            <td>0.45</td>
            <td>49.2</td>
            <td>70,000</td>
            <td>25</td>
        </tr>
        <tr>
            <td>Soft</td>
            <td>0.45</td>
            <td>42.2</td>
            <td>60,000</td>
            <td>30</td>
        </tr>
        </tbody>
    </table>
    ```

    * type = 'text'
    ```html
    <input type="text" placeholder="ㅇㅇㅇ">
    ```

    * type="password"
    ```html
    <input type="password">
    ```

    * type="radio"
    ```html
    <input type="radio" name="gender"> 남자
    <input type="radio" name="gender"> 여자
    ```

    * type="checkbox"
    ```html
    <input type="checkbox" name="hobby"> 등산
    <input type="checkbox" name="hobby"> 독서
    <input type="checkbox" name="hobby"> 운동
    ```

    * type="file"
    ```html
    <input type="file">
    ```

    * type="submit|reset|image|button"
    ```html
    <form action="./test.html">
        메시지: <input type="text" name="message"><br>
        <input type="submit">
        <input type="reset">
        <input type="image" src="http://placehold.it/50x50?text=click" alt="click" width="50" height="50">
        <input type="button" value="버튼">
    </form>
    ```

    * ```<select>```
    ```html
    <select>
        <option>서울</option>
        <option>경기</option>
        <option>강원</option>
        ...
    </select>
    ```

    * ```<button>```
    ```html
    <button type="submit|reset|button">ㅇㅇㅇ</button>
    ```