# SqlSession

## 기존 Project

> Controller -&gt; Service -&gt; Mapper.java -&gt; Mapper.xml Controller &lt;- Service &lt;- Mapper.java &lt;-

## SqlSession 사용 시

> **Controller** -&gt; ServiceImpl\(Interface implement\) -&gt; DaoImpl\(Interface implement\) : return sqlsession.selectList\(NameSpace + ".\); -&gt; user.xml -&gt; DaoImpl -&gt; ServiceImpl -&gt; Controller

## 정리

> **즉, 기존 Project의 방식은 Mapper.java 클래스 이름을 별도로 지정 및 Mapper.xml을 별도로 계속 생성해줘야 한다.**

## 예시

> UserMapper, AccountMapper 등 생성해주고, UserMapper 안에 InsertUser Interface를 생성 필요, 그리고 거기에 맞는 mapper의 xml도 생성해줘야 한다.

> 하지만 sqlsession에는 select 등 이미 다 구현이 되어 있어서, 대규모 프로젝트에는 그것만 사용하도록 강제할 수 있다.

> 또한 return sqlsession\("queryID", VO\) 이런 식으로 한다면 query에 맞는 user.xml에 자동적으로 mapping해준다

