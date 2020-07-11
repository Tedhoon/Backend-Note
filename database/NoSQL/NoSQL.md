# NoSQL

- Not only SQL

- RDBMS의 한계를 극복하기 위해 만들어진 새로운 형태의 데이터저장소

- RDBMS처럼 고정된 스키마(Table-Column) 및 JOIN이 존재하지 않음

- 스키마 변경? ALERT 등 필요 없음

## Why NoSQL?

기본적으로 RDBMS를 사용하지만,
초당 데이터가 수십만개씩 쌓이는 서비스가 많아지면서(쇼셜, 온라인 서비스등), NoSQL을 사용하는 경우가 많아지고 있음

- 95% read, 5% write 경우는 RDBMS 가 성능이 나쁘지 않음
- 50% write > 인 경우 RDBMS는 성능 저하 또는 불안정
- NoSQL + Redis (In memory cache) 등을 고려하게 됨

NoSQL 데이터베이스는 각 데이터베이스마다 기반으로 하는 데이터 모델이 다르므로, 데이터 모델별로 대표적인 데이터베이스를 알아둘 필요가 있음

> 데이터 모델
- Key/Value Store [redis]
- Wide Column Store [...]
- Document Store [mongoDB]
- Graph Store [...]


