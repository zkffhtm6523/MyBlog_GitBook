# Configuration

## 프로젝트 구조

[![images](https://camo.githubusercontent.com/05776cadf462fdbe878ccd6970ed9f430674f102d2ffe9c6bad19efe806adbc8/68747470733a2f2f6d656469612e766c70742e75732f696d616765732f7a6b666668746d363532332f706f73742f65306232626439632d626331642d343564352d613735312d6165326266643365396531322f696d6167652e706e67)](https://camo.githubusercontent.com/05776cadf462fdbe878ccd6970ed9f430674f102d2ffe9c6bad19efe806adbc8/68747470733a2f2f6d656469612e766c70742e75732f696d616765732f7a6b666668746d363532332f706f73742f65306232626439632d626331642d343564352d613735312d6165326266643365396531322f696d6167652e706e67)

## 1. servlet-contex.xml

| **servlet-contex.xml** |
| :---: |
| WEB Application 에서 client 요청을 받기 위한 설정 |
| JSP와 관련있는 객체\(bean\) 설정 - controller, MultipartResolver, Interceptor\(로그인 등\) |
| 어노테이션 `<annotation-driven/>` |
| URL 관련 설정 |

* **servlet**에서 보듯이 요청과 관련된 객체를 정의
* url과 관련된 controller나, @\(어노테이션\), ViewResolver, Interceptor, MultipartResolver 등의 설정

[![images](https://camo.githubusercontent.com/71547f55e34f4216d10af8df7db0730e581a8642d5c1784faa0d887da637bc90/68747470733a2f2f696d616765732e76656c6f672e696f2f696d616765732f7a6b666668746d363532332f706f73742f31653666313066352d303664352d343964382d386437332d3933313933373762343537382f696d6167652e706e67)](https://camo.githubusercontent.com/71547f55e34f4216d10af8df7db0730e581a8642d5c1784faa0d887da637bc90/68747470733a2f2f696d616765732e76656c6f672e696f2f696d616765732f7a6b666668746d363532332f706f73742f31653666313066352d303664352d343964382d386437332d3933313933373762343537382f696d6167652e706e67)

```text
DispatcherServlet Context: defines this servlet's request-processing infrastructure
```

위와 같은 주석이 있는데, **DispatcherServlet과 관련된 설정**을 해야함을 알 수 있습니다.

## 2. root-contex.xml

| root-contex.xml |
| :---: |
| JSP와 관련없는 객체\(bean\)을 설정합니다.\(service, repository\) |
| 비지니스 로직을 위한 설정을 합니다. |
| 외부 jar 파일등으로 사용하는 클래스는 `<bean>`태그를 이용하여 작성합니다. |
| URL 관련 설정 |

> 따라서 **Service, Repository\(DAO\), DB**등 비즈니스 로직과 관련된 설정 servlet-context.xml 과는 반대로 view와 관련되지 않은 객체를 정의

[![](https://camo.githubusercontent.com/1e379428c56f90f0975d0997f18ebce92654b85066297a11d64272eda490de12/68747470733a2f2f696d616765732e76656c6f672e696f2f696d616765732f7a6b666668746d363532332f706f73742f33396137323563302d663461612d346535612d386132622d6436303030666535323861622f696d6167652e706e67)](https://camo.githubusercontent.com/1e379428c56f90f0975d0997f18ebce92654b85066297a11d64272eda490de12/68747470733a2f2f696d616765732e76656c6f672e696f2f696d616765732f7a6b666668746d363532332f706f73742f33396137323563302d663461612d346535612d386132622d6436303030666535323861622f696d6167652e706e67)

\(출처: [https://docs.spring.io/spring/docs/current/spring-framework-reference/web.html\#mvc](https://docs.spring.io/spring/docs/current/spring-framework-reference/web.html#mvc)\)

## 3. web.xml

> 설정을 위한 설정파일입니다. 즉, **최초로 WAS가 최초로 구동될 때, 각종 설정을 정의**해줍니다. 여러 xml파일을 인식하도록 각 파일을 가리켜 줍니다.

