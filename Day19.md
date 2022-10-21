# 36번 문제(조건별로 분류하여 주문상태 출력하기) string,Date
![image](https://user-images.githubusercontent.com/97568475/197129435-d4ef0248-b662-495b-a409-d5fc7acdf777.png)


* * *
# 36번 문제 나의 해답
```
SELECT
    order_id, product_id, date_format(out_date, "%Y-%m-%d") as out_date,
    case 
        when out_date <= "2022-05-01" then "출고완료"
        when out_date > "2022-05-01" then "출고대기"
        else "출고미정"
    end as 출고여부
from food_order;
```

* * *
# 36번 문제 피드백
case문 활용해서 

* * *
