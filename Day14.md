# 27번 문제(우유와 요거트가 담긴 장바구니)
![image](https://user-images.githubusercontent.com/97568475/194453864-d5c8b2f9-e57f-4eab-aed3-7d3c62ad7c70.png)


* * *
# 27번 문제 나의 해답
```
select distinct c.cart_id
from CART_PRODUCTS as c, CART_PRODUCTS as t
where c.cart_id = t.cart_id and c.name like 'Yogurt' and t.name like 'milk'
order by cart_id
```

* * *
# 27번 문제 피드백
self join 으로 2개를 묶고 중복을 제거한 후에 조건을 걸쳐서 뽑아낸다.

* * *
# 28번 문제(경기도에 위치한 식품창고 목록 출력하기) IS NULL
![image](https://user-images.githubusercontent.com/97568475/195233521-95efd055-253a-459e-bbf0-6452c61ebd81.png)


* * *
# 28번 문제 나의 해답
```
SELECT WAREHOUSE_ID, WAREHOUSE_NAME, ADDRESS, case when FREEZER_YN is null then 'N'
else FREEZER_YN end
from FOOD_WAREHOUSE
where address like '경기도%'
order by WAREHOUSE_ID
```

* * *
# 28번 문제 피드백
null 값을 N 문자열로 바꿀 수 있는가, 경기도로 시작하는 문자열을 찾을 수 있는가 
* * *

