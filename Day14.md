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
![image](https://user-images.githubusercontent.com/97568475/195523619-598ac8ff-7806-41e3-bf7d-2cb9f974ac6a.png)


* * *
# 28번 문제 나의 해답
```

```

* * *
# 28번 문제 피드백
같은 food_type에서 즐겨찾기수로 먼저 비교를 하고 조회하는 방식으로 해야할거같다. 미완성..
* * *

