**CREATE**

**UPDATE**

**DELETE**

**READ**
* select 문(기본 검색을 위해 사용)
   * select * from x : x에 있는 데이터 전부 출력
   * select x1, x2, x3 from x : x에 있는 특정속성(x1, x2, x3)만 데이터 출력
   * 
* where 문(조건 검색을 위해 사용)
   * select * from x where x1 = '1234' : x에 있는 x1 속성값이 1234인 경우의 데이터 출력
   * select * from x where x1 = '1234' and x2 > '123' : x에 잇는 x1 속성값이 1234인 경우와 x2 속성값이 123보다 큰 경우의 데이터 출력
   * select * from x where date(x3) between '2020-07-13' and '2020-07-14' : x에 있는 x3의 속성값이 2020-07-13~14일 데이터 출력
   * select * from x where x4 in (2,3) : x에 잇는 x4의 속성값이 2~3사이일 데이터 출력
   * select * from x where x5 like '%abcd%' : x에 있는 x5 속성값 중 특정 키워드(abcd)를 포함한 데이터 출력
   * select count(distinct(x6)) from x : 중복을 제거한 x6 속성값의 개수 추출
   * select count(x) from (select distinct * from x) t : 전체 데이터에서 중복이 있을때 제거하고 개수 추출
   * 
* group by(기존 속성으로 묶는 것)
   * select x1, count(*) from x group by x1 : x 테이블에서 x1속성으로 묶고, 개수 추출
   * select x2, max(x3) from x group by x2 : x 테이블에서 x2속성으로 묶고, x3의 최대값 추출
   * select x2, round(avg(x3),2) from x group by x2 : x 테이블에서 x2속성으로 묶고, x3의 소숫점 둘째자리 까지의 평균값 추출
   * select x2, sum(x3) from x group by x2 : x 테이블에서 x2 속성으로 묶고, x3의 모든 합 추출

* order by(결과값의 정렬)
   * select x2, count(*) from x group by x2 order by count(*) : x2 속성값 별로 개수 집계, 오름차순 정렬(default)
   * select x2, count(*) from x group by x2 order by count(*) desc : x2 속성값 별로 개수 집계, 내림차순 정렬

* alias(별칭)
   * select count(*) from x as y where y.x1 = '1234' : 별칭(y)을 사용하면 추후 지정한 값이 너무 복잡해 끌어오기 힘든 상황을 방지 

* join(여러 개의 테이블을 조건에 맞게 테이블을 연결한 것)
   * inner join(테이블 x, y가 있다고 가정할 때, 이 둘의 교집합만을 join)
    *select * from orders o 
inner join users u
on o.user_id = u.user_id  
   * left join(테이블 x, y가 있다고 가정할 때, 왼쪽 테이블 x를 중심으로 join)
   * 













