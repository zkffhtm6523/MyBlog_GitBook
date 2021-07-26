---
description: Query 작성 시 문법
---

# JpaRepository Method

## findByXX

"findBy" 이후에 엔티티의 속성 이름을 붙이다. 이 속성 이름은 첫 글자는 대문자로 한다.

예를 들어, name 검색한다면 "findByName"이며, mail에서 찾는다면 "findByMail"가 된다.

이 다음에는 기본형인 'findByXX" 이후에 계속 이어서 쓰면 된다.

## Like / NotLike

"퍼지 검색"에 관한 것이다. Like를 붙이면, 인수에 지정된 텍스트를 포함하는 엔티티를 검색한다. 또한 NotLike을 쓰면 인수의 텍스트를 포함하지 않는 것을 검색한다. "findByNameLike"이라면, name에서 인수의 텍스트를 퍼지 검색한다.

## StartingWith / EndingWith

```java
// name의 값이 "A"로 시작하는 항목을 검색한다.
List findByNameStartingWith("A");
```

## IsNull / IsNotNull

```java
// 값이 null이 거나, 혹은 null이 아닌 것을 검색한다. 인수는 필요없다.
List findByNameIsNull();
```



#### True / False

부울 값으로 true 인 것, 혹은 false 인 것을 검색한다. 인수는 필요없다. "findByCheckTrue\(\)"이라면, check라는 항목이 true 인 것만을 검색한다.

#### Before / After

시간 값으로 사용한다. 인수에 지정한 값보다 이전의 것, 혹은 이후 것을 검색한다. "findByCreateBefore\(new Date\(\)\)"라고 하면, create라는 항목의 값이 현재보다 이전의 것만을 찾는다 \(create가 Date 인 경우\).

#### LessThan / GreaterThan

숫자 값으로 사용한다. 그 항목의 값이 인수보다 작거나 큰 것을 검색한다. "findByAgeLessThan\(20\)"이라면, age의 값이 20보다 작은 것을 찾는다.

#### Between

두 값을 인수로 가지고 그 두 값 사이의 것을 검색한다. 예를 들어, "findByAgeBetween\(10, 20\)"라고 한다면 age 값이 10 이상 20 이하인 것을 검색한다. 수치뿐만 아니라 시간의 항목 등에도 사용할 수 있다.  
  
출처: [https://araikuma.tistory.com/329](https://araikuma.tistory.com/329) \[프로그램 개발 지식 공유\]

