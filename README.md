**CREATE**

**UPDATE**

**DELETE**

**READ**
* select 문(기본 검색을 위해 사용)
   * select * from x : x에 있는 데이터 전부를 출력
   * select x1, x2, x3 from x : x에 있는 특정속성(x1, x2, x3)만 출력
* where 문(조건 검색을 위해 사용)
   * select * from x where x1 = '1234': x에 있는 x1속성값이 1234인 경우를 출력
   * select * from x where x1 = '1234' and x2 > '123': x에 잇는 x1속성값이 1234인 경우와 x2가 123보다 큰 경우를 출력
