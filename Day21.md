# 38번 문제(식품분류별 가장 비싼 식품의 정보 조회하기) group by
![image](https://user-images.githubusercontent.com/97568475/197700343-b86dbac8-fbaf-45fc-8f59-4bdba6c72821.png)


* * *
# 38번 문제 나의 해답
```
SELECT 
    ORDER_ID
    ,PRODUCT_ID
    ,DATE_FORMAT(OUT_DATE,'%Y-%m-%d')AS OUT_DATE
    ,CASE
        WHEN OUT_DATE > DATE('2022-05-01') THEN '출고대기'
        WHEN DATE('2022-05-01') >= OUT_DATE THEN '출고완료'
        WHEN OUT_DATE IS NULL THEN '출고미정'
     END AS '출고여부'
FROM FOOD_ORDER
ORDER BY ORDER_ID;
```

* * *
# 38번 문제 피드백
DATE_FORMAT을 해서 날짜값 만들고 case문 

* * *
