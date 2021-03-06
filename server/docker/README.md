# Docker

## Docker란?

> 리눅스 컨테이너를 기반으로 하여 특정한 서비스를 패키징하고 배포하는데 유용한 오픈소스 프로그램

#### **도커 사용 이유**

[![image](https://user-images.githubusercontent.com/66704969/120500465-d30d3d80-c3fb-11eb-9417-cb8a062875bf.png)](https://user-images.githubusercontent.com/66704969/120500465-d30d3d80-c3fb-11eb-9417-cb8a062875bf.png)

> 일반적인 '호스팅 서비스'는 우리의 로컬 컴퓨터 환경과 상이하다. JVM 설치, 톰캣 설치 등 환경이 다를 수 밖에 없다.

> 컨테이너에 이미지\(Image\)를 담아서 구동시키는 방식으로 쉽게 배포

#### VM\(Virtual Machine\) VS 컨테이너\(Container\)

[![image](https://user-images.githubusercontent.com/66704969/120504649-495f6f00-c3ff-11eb-84cb-924562eb8575.png)](https://user-images.githubusercontent.com/66704969/120504649-495f6f00-c3ff-11eb-84cb-924562eb8575.png)

> 컨테이너\(Container\)는 가상 머신 대신에 도커 엔진\(Docker Engine\) 위에서 동작한다는 특징

> 별도의 Guest OS가 사용되지 않아서 성능적으로 매우 개선됨. 메모리 용량도 적게 차지함.

#### 도커\(Docker\) 패러다임

> 도커는 **변경 불가능한 인프라\(Immutable Infrastructure\)** 를 주요 패러다임으로 상정

> 서버를 구축한 이후에는 변경이나 업데이트를 할 수 없음

