## Webpack

Webpack 이란?

Webpack 을 사용하는 이유

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

ref https://velog.io/@decody/Webpack-%EC%84%A4%EC%A0%95

https://developer.mozilla.org/ko/docs/Web/API/Element/innerHTML
