- JSDOM 설치중

      npm init -y

      npm i jsdom --save-dev

      node jsdomtest.js
      jsdom test....
      Hello world
      (node:3976) ExperimentalWarning: The fs.promises API is experimental

1.Node.js (windows system): ExperimentalWarning: The fs.promises API is experimental

The root cause is that the version of node is not up to date, and the module introduced in the project is up to date, and the version of node.js is lower than the version of the module:

The solution is to upgrade npm, node.js:

npm install npm@latest -g

https://nodejs.org/zh-cn/Download the latest version to install the same path.

- 업데이트 해야함

- 버전확인

      c:\_dev\_nodejs\tdl>npm -v
      6.4.1

      c:\_dev\_nodejs\tdl>node -v
      v10.15.0

- 구글링

- npm 업데이트 -g 옵션 없을시 현재 프로젝트만 적용됨

      c:\_dev\_nodejs\tdl>npm i -g npm

      c:\_dev\_nodejs\tdl>npm -v
      6.14.5

- 캐시 삭제. 캐시가 남아있는 경우 에러가 날 수 있다.

      npm cache clean --force

      c:\_dev\_nodejs\tdl>npm cache clean -f
      npm WARN using --force I sure hope you know what you are doing.

      c:\_dev\_nodejs\tdl>npm install -g n
      npm ERR! code EBADPLATFORM
      npm ERR! notsup Unsupported platform for n@6.5.1: wanted {"os":"!win32","arch":"any"} (current: {"os":"win32","arch":"x64"})
      npm ERR! notsup Valid OS:    !win32
      npm ERR! notsup Valid Arch:  any
      npm ERR! notsup Actual OS:   win32
      npm ERR! notsup Actual Arch: x64

      npm ERR! A complete log of this run can be found in:
      npm ERR!     C:\Users\a\AppData\Roaming\npm-cache\_logs\2020-06-05T14_00_10_278Z-debug.log

- --no optional 명령어를 이용해보기

      c:\_dev\_nodejs\tdl>npm --no-optional install -g n

      안되는 건 똑같음

      c:\_dev\_nodejs\tdl>npm cache verify
      Cache verified and compressed (~\AppData\Roaming\npm-cache\_cacache):
      Content verified: 0 (0 bytes)
      Index entries: 0
      Finished in 0.025s

      이런것도 해보고..

윈도우는 npm install -g n 지원 안한다고 한다. 어쩐지 리눅스만...

윈도우즈는 Node.js 공식 홈페이지에서 윈도우 인스톨러를 받으면 알아서 덮어씌워 준다고 한다.

https://nodejs.org/ko/download/package-manager/#windows

그 밖의 방법으로

Chocolatey , Scoop을 사용 할 수 있다고 한다.

msi 파일 LTS 버전으로 덮어쓰기함.

      C:\Users\a>node -v
      v10.15.0

      C:\Users\a>node -v
      v12.18.0
