# 30번 문제(조건에 맞는 회원수 구하기) SELECT
![image](https://user-images.githubusercontent.com/97568475/196065888-7cfe8b71-0a5b-4013-b3b4-9e21392110e3.png)



* * *
# 30번 문제 나의 해답
```
SELECT count(user_id) as users from user_info
where joined like '2021%' and age >= 20 and age <=29
```

* * *
# 30번 문제 피드백
where 절과 count를 할수 있는지

* * *
# 31번 문제(상품 별 오프라인 매출 구하기) JOIN
![image](https://user-images.githubusercontent.com/97568475/196076325-985c1707-8576-43b8-aff9-32bd6c715807.png)


* * *
# 31번 문제 나의 해답
```
SELECT P.PRODUCT_CODE, (P.PRICE * SUM(O.SALES_AMOUNT)) AS SALES
FROM PRODUCT AS P
JOIN OFFLINE_SALE AS O
ON P.PRODUCT_ID = O.PRODUCT_ID
GROUP BY P.PRODUCT_ID
ORDER BY SALES DESC, PRODUCT_CODE ASC
```

* * *
# 31번 문제 피드백
먼저 판매량 총합을 내도록 SUM을 이용하고 join을 통해서 합쳐준다음 매출액(판매가*판매량)을 구해냇다

* * *
