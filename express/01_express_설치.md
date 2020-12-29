express란 서버사이드 자바스크립트 웹개발 프레임워크

프로젝트 생성

    npm init -y

express 설치

    npm install express --save

01_Test.js 파일 실행

~ express 서버를 가장 간단한 상태로 구현 성공 ~

    const express = require('express');
    const app = express();
    const port = process.env.PORT || 3000;

    app.get('/', (req, res) => {
        res.json({
            success: true,
        });
    });

    app.listen(port, () => {
        console.log(`server is listening at localhost : ${process.env.PORT}`);
    });

localhost:3000 으로 접속하면 

    {"success":true} 출력

- require 는 nodejs에서 다른 패키지 불러올 때 사용.<br>
  별도의 path를 지정하지 않은 해당 코드에서는 node_modules 에서 express 모듈을 찾는다.
  
- app 이라는 변수에 express 함수의 변환 값 저장. 이 변수롤 REST End Point들을 생성한다.

- process.env 는 nodejs에서 환경 변수를 가져올 때 사용. 환경 변수가 입력되지 않을시 port에서 3000번을 지정하는 코드이다.

- app.get 으로 REST API의 GET Request를 정의. path 지정 '/' 한 곳으로 서버 작동 확인한다.

- app.listen ~ express 서버를 실행할 때 필요한 포트 정의 및 실행 시 callback 함수를 받는다.<br>
  express를 3000 post에 실행하고 exptress 서버 구축 성공시 두 번째 파라미터인 callback 함수에서 해당 로그를 출력한다.

ref https://medium.com/withj-kr/nodejs-express%EB%A1%9C-%EC%84%9C%EB%B2%84-%EA%B5%AC%EC%84%B1%ED%95%98%EA%B8%B0-1-express-%EA%B8%B0%EB%B3%B8%EA%B8%B0-c0245b4120bc
