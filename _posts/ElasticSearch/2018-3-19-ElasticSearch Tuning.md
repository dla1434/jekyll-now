---
layout: post
title: ElasticSearch 최적화
---

# ElasticSearch Tuning

# 성능 최적화
##1 Query

### 1.1 Query
1. Query대신 Filter 사용
- filter는 _score를 사용하지 않기 때문에 query에 비해 속도가 빠르다.
- 필터는 오직 결과가 검색과 일치하는지만 관심을 가진다는 것이다. 결과적으로 다른 쿼리보다 빠르고 쉽게 캐시에 저장할 수 있다.
- 필터 결과는점수에 의해 정렬되지 않는다. (모든 결과에 대한 점수가 1.0이기 때문)
  - _score : 문서가 지정한 조건과 얼마나 유사한지 평가

##2 refresh
1. refresh_interval 을 증가 시킬수록 색인 처리량은 늘어난다.
2. 시스템 자원을 덜 사용하기 때문이다. 대신 데이터의 신선도는 낮아질 수 있다. 신선도가 낮아도 되는 경우라면 refresh를 수동으로 하는 것도 고려해봐라.


##1.2 flush

```

```
