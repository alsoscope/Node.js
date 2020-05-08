## Webpack

Webpack 이란?
웹에서 사용되는 여러 개의 자원(assets : js, css, jpg)을 웹 브라우저가 이해할 수 있는 번들로 묶고
패키징 할 수 있는 자바 스크립트 모듈 번들러이다.(번들링)

번들링 : 여러 개의 파일 중에 종속성이 존재하는 파일을 하나의 파일로 묶어 패키징 시키는 과정

Webpack 을 사용하는 이유
각기 다른 자바 스크립트를 로딩할 때, 스크립트 

Node.js 환경에서 실행한다.

1. Webpack 시작하기

npm 으로 설치한다.


2. index.js

        function component(){
            const element = document.createElement('div');

            //element.innerHTML=_.join(['Hello', 'webpack'], '');
            element.innerHTML="htmlString";

            return element;
        }

        document.body.appendChild(component());

**Element.innerHTML**<br>
Element 속성(property) innerHTML은 요소(element) 내에 포함된 HTML 또는 XML 마크업을 가져오거나 설정한다.

**_.join(array, [separator=','])**<br>
//Lodash, currently included via a script, is required for this line to work<br>
자바 스크립트 유틸리티 라이브러리.

Converts all elements in array into a string separated by separator.

- Arguments<br>
    __array (Array)__: The array to convert.<br>
    **[separator=','] (string)**: The element separator.

- Returns<br>
    __(string)__: Returns the joined string.

- Example

        _.join(['a', 'b', 'c'], '~');
        // => 'a~b~c'

- index.html lodash CDN 경로<br>
  `<script src="https://cdn.jsdelivr.net/npm/lodash@4.17.15/lodash.min.js"></script>`

3. Visual Studio Code - __Live Server__ 설정

    VS 코드의 라이브 서버 플러그인을 이용하면 로컬에서 파일을 실행할 수 있다.<br>
    에디터에서 수정 후 저장을 하면 로컬 서버에 바로 반영이 된다.

- 라이브 서버 설치<br>
    File Preferences Settings<br>
    또는 Ctrl + Shift + X 로 Extensions 활용

    live server 검색하고 설치한다.

    Explorer (탐색기) 에서 테스트용 폴더 추가, 파일 작성한다. (html:5 입력하면 자동완성 된다.)

    코드 탭에서 오른쪽 클릭, Open with Live Server 클릭,<br>
    혹은 Alt + L, Alt + O 입력한다.

    로컬 서버로 코드가 렌더링 된다.
    
    OS에서 기본 브라우저로 삼고 있는 탭으로 열린다.<br>
    다른 브라우저로 열고 싶다면 기본 브라우저를 변경하면 된다.

ref https://velog.io/@decody/Webpack-%EC%84%A4%EC%A0%95<br>
https://developer.mozilla.org/ko/docs/Web/API/Element/innerHTML
