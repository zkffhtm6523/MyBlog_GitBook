# WebHook && Pooling

[![image](https://user-images.githubusercontent.com/66704969/120198932-a15e7000-c25d-11eb-9f5e-8d59bea082b9.png)](https://user-images.githubusercontent.com/66704969/120198932-a15e7000-c25d-11eb-9f5e-8d59bea082b9.png)

> **Pooling** : 우리의 앱에서 엔드포인트에 이벤트가 발생했는지 주기적으로 요청을 보내는 방식이라 비효율적

> **WebHook** : 엔드포인트에서 발생한 이벤트가 우리의 앱에 수신되는 형태

> 예\) ATM기에서 현금을 2만원을 뽑았을때 SMS를 관리하는 시스템과 고객의 계좌를 관리하는 시스템 2개가 서로 긴밀하게 연결되어야 한다. 이때 웹훅을 사용한다. 고객 계좌 관리 시스템에서 현금이 인출되었다는 이벤트가 발생하여\(웹훅 엔드포인트\) SMS 시스템에서 그 이벤트를 수신하여 고객에게 ‘현금 2만원이 출금되었습니다’ 라는 문자를 쏴줄 수 있다.

> **웹훅은 한마디로 이벤트에 대한 이벤트 핸들러다.**
