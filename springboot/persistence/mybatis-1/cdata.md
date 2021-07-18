# CDATA

### 1. 개념

> 특수문자, 비교연산자 등 단어나 문장을 문자열로 인식하게 함

### 2. 예시

```markup
//사용 전

<select id ="list" parameterType="int" resultType="board.test.testDto">

SELECT
  *
FROM
  employees
where
  salary > 100

</select>

//사용 후

<select id = "list" parameterType="int" resultType="board.test.testDto">

SELECT
  *
FROM
  employees
where
  salary <![CDATA[ > ]]> 100
</select>
```

