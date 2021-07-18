---
description: NoSQL
---

# Redis

* **레디스\(Redis\)** :  Remote Dictionary Server의 약자
* "Key-Value" 구조의 비정형 데이터를 저장하고 관리하기 위한 [오픈 소스](https://ko.wikipedia.org/wiki/%EC%98%A4%ED%94%88_%EC%86%8C%EC%8A%A4) 기반 비관계형 DBMS
* 2009년 [살바토르 산필리포](https://ko.wikipedia.org/w/index.php?title=%EC%82%B4%EB%B0%94%ED%86%A0%EB%A5%B4_%EC%82%B0%ED%95%84%EB%A6%AC%ED%8F%AC&action=edit&redlink=1)\(Salvatore Sanfilippo\)가 처음 개발
* 2015년부터 Redis Labs가 지원.
* 모든 데이터를 메모리로 불러와서 처리하는 메모리 기반 DBMS

### 데이터 모델

* Key-Value
  * 하나의 Key에 하나의 Value를 갖는 데이터 모델
  * Key로만 접근 가능
* Column
  * 하나의 Key에 여러개의 Value를 갖을 수 있는 데이터 모델
  * 중첩된 HashMap 구조
* Document
  * Value가 Json이나 XML Document를 갖는 데이터 모델
  * Value의 일부로 질의하고 일부만 가져올 수 있음
* Graph
  * 관계에 특화된 모델
  * 노드와 간선에 대한 정보

이 중 Redis는 Key-Value 데이터 모델을 사용합니다.  단순한 형태의 Key-Value 방식으로 빠른 속도 지

### 데이터 타입

* String
  * Command Docs : http://redis.io/commands\#string
  * Text, 숫자 등 일반적인 Value
* Set
  * Command Docs : http://redis.io/commands\#set
  * Value가 Set 자료구조가 되므로, 하나의 Key 값에 여러 값을 Set 자료구조를 통해 저장 가능
  * Set간의 집합 연산을 제공
* Sorted Set
  * Command Docs : http://www.redis.io/commands\#sorted\_set
  * score라는 필드가 추가되어 정렬의 기준이 됨.
  * score를 통해 질의 가능
  * 그 외에는 위의 Set과 같음
* Hashes
  * Command Docs : https://redis.io/commands\#hash
  * Value가 Map 자료구조와 같은 Key/Value 형태가 됨
  * 하나의 Key에 여러개의 필드를 갖는 구조가 됨
* List
  * Command Docs : https://redis.io/commands\#list
  * Value가 linkedList 자료구조가 됨
  * Push/Pop 연산 가능
  * index 활용 질의 가능

## [**참고 사이트**](https://blog.kingbbode.com/25)\*\*\*\*



