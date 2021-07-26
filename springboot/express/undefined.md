# 환경설정

## 1. **프로젝트 생성**

```bash
mkdir 원하는 프로젝트폴더
cd 프로젝트 폴더

# package.json 생성
npm init --yes

# express & body-parser => package.json 추가 
npm install express body-parser mongoose

# index.js 파일 생성
vim index.js

################ index.js ####################
const express = require('express')
const app = express()
const port = 3000

app.get('/', (req, res) => {
  res.send('Hello World!')
})

app.listen(port, () => {
  console.log(`Example app listening at http://localhost:${port}`)
})
####################################

# package.json 파일 수정
vi package.json

# script -> start 추가
scripts": { "start": "node index.js"}

# 백그라운드로 index.js 실
npm run start &
```

## 2. MongoDB 설

* 기존 DB 설치 완료된 상황에서 패키지 설치 진행

```bash
# 현재 경로
/Users/david/Programming/2021_Project/nodejs_express_v2

# npm install 후 package.json에 추가
npm install mongoose --save
```

