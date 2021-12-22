# ** WEBPACK **
- install : npm i -D webpack webpack-cli webpack-dev-server@next
- json 수정
```json
"scripts": {
    "dev": "webpack-dev-server --mode development",
    "build": "webpack --mode production"
  }
```
- parcel은 세 개가 자동화
- webpack-dev-server을 통해 개발 특화 환경을 구성.
- mode는 개발, 제품 모드를 선택할 수 있음
---
## webpack config
- root에 webpack.config.js 파일을 제공해주어야 함.
---
## 개발 서버 오픈 html-webpack-plugin
- install : npm i -D html-webpack-plugin
---
## copy-webpack-plugin
- install : npm i -D copy-webpack-plugin
- webpack.config.js 수정
---
## css-loader, style-loader
- install : npm i -D css-loader style-loader
- webpack.config.js 에 module 추가

- css-loader: css파일을 해석하는 용도
- style-loader: html의 태그 부분에 해석된 부분을 삽입해준다.
- 순서는 style-loader -> css-loader 순서로.
---

## sass-loader, sass
- install : npm i -D sass-loader sass
- webpack.config.js에 module에 sass-loader 추가.
---
## postcss, autoprefixer@9, postcss-loader
- install : npm i -D postcss autoprefixer@9 postcss-loader
- package.json 에 browserslist 추가
- .postcssrc.js 파일 추가 autoprefixer 플러그인 추가
---

## babel 추가
- install : npm i -D @babel/core @babel/preset-env @babel/plugin-transform-runtime
- .babelrc.js 추가
```js
module.exports = {
  presets: ['@babel/preset-env'],
  plugins: [
    ['@babel/plugin-transfrom-runtime']
  ]
}
```
- webpack.config.js에 rules 추가
- babel-loader 추가로 설치하면 Babel 구성 끝
- npm i -D babel-loader
--- 
