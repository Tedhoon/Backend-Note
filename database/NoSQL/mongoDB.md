# MongoDB

MongoDB는 `document DB`
> JSON 기반의 Document 기반 데이터 관리

```js
// MongoDB Document 예)

{
    "_id": ObjectId("5099803df3f42312312391"),
    "username": "davelee",
    "name": { first: "Dave", last: "Lee" }
}
```

## MongoDB 데이터 구조

- RDBMS의 table이 아니라, `collection`에 JSON 형태의 Document를 넣음
- 각 Document가 하나의 로우(레코드)라고 함
- 결국 MongoDB라는 Database는 `collection의 집합`

<img src="https://www.fun-coding.org/00_Images/nosqlstructure.png">


## MongoDB Collection

Collection은 MongoDB Document의 집합

RDBMS Table과 유사한 개념, 단 정규화된 데이터 구조, 즉 Schema가 정의되어 있지 않음

<img src="https://www.fun-coding.org/00_Images/mongodb_mysql.png">


# MongoDB 다뤄보기

Robomongo 설치 (MongoDB 관리 GUI 툴) 

👉 https://robomongo.org/download