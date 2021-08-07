# next\(\) 메소드

## 예제 

```javascript
var express = require('express');
var router = express.Router();

// 첫 번째 라우터 
router.get('/', function(req, res, next) {
    console.log('step1');
    // next 메소드
    next();
});

// 두 번째 라우터 
router.get('/', function(req, res, next) {
    res.send('으악');
});

module.exports = router;
```

![](../../.gitbook/assets/image%20%282%29.png)

## 용도 

* 다음 라우터로의 전

