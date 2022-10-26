# 39번 문제(진료과별 총 예약 횟수 출력하기) group by
![image](https://user-images.githubusercontent.com/97568475/197933384-a3d93f63-020d-4dde-94e5-0b5897ad0901.png)


* * *
# 39번 문제 나의 해답
```
SELECT MCDP_CD as '진료과코드' , count(APNT_YMD) as '5월예약건수'
from APPOINTMENT  
where date_format(APNT_YMD , '%Y-%m') = '2022-05'
group by MCDP_CD
order by 5월예약건수 , 진료과코드
```

* * *
# 39번 문제 피드백
count와 date_format 활용

* * *
# 40번 문제(가격대 별 상품 개수 구하기) group by
![image](https://user-images.githubusercontent.com/97568475/197938102-6d35fe44-0a3d-427b-80af-f9ec5d9cdb2d.png)


* * *
# 40번 문제 나의 해답
```
SELECT TRUNCATE(PRICE, -4) AS PRICE_GROUP, COUNT(PRODUCT_ID) AS PRODUCTS
FROM PRODUCT
GROUP BY TRUNCATE(PRICE, -4)
ORDER BY PRICE_GROUP ASC;
```

* * *
# 40번 문제 피드백
TRUNCATE 활용
1. TRUNCATE
 
1-1. Truncate 특징
1) DDL 명령어이다.
2) 모든 레코드(행)를 삭제해버리는 특징이 있다.
3) 조건절 사용을 못한다 (where절 사용 불가)
4) IDENTITY를 초기화 할 수 있다.
5) 테이블 구조, 열, 제약조건, 인덱스는 그대로 남는다.
6) 트랜잭션 로그 공간을 덜 사용한다.
> delete문은 행을 한번에 하나씩 제거하고 삭제된 각 행에 대해 트랜잭션 로그를 기록하게 된다.
그에 반해 truncate는 해당 테이블의 데이터 저장소의 페이지를 취소하는 방식으로 데이터를 제거하고 페이지 할당 취소만을 트랜잭션에 넣기 때문에 공간을 덜 사용한다.
7) Auto Commit이라서 한번 실행하면 복구 할 수 없다.
* * *
