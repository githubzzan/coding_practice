# 37번 문제(식품분류별 가장 비싼 식품의 정보 조회하기) group by
![image](https://user-images.githubusercontent.com/97568475/197454857-ba338546-8e6c-4079-bd50-33ce7199af24.png)


* * *
# 37번 문제 나의 해답
```
SELECT F.CATEGORY, F.PRICE AS MAX_PRICE, F.PRODUCT_NAME
FROM FOOD_PRODUCT AS F, (
    SELECT CATEGORY, MAX(PRICE) AS MPRICE
    FROM FOOD_PRODUCT
    WHERE CATEGORY IN ('과자', '국', '김치', '식용유')
    GROUP BY CATEGORY
) M
WHERE F.CATEGORY = M.CATEGORY AND F.PRICE = M.MPRICE
ORDER BY MAX_PRICE DESC;
```

* * *
# 37번 문제 피드백
이중쿼리로 한다음 order by 활용

* * *
