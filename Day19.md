# 36번 문제(헤비 유저가 소유한 장소)
![image](https://user-images.githubusercontent.com/97568475/196601310-398bc6cf-f7ee-4daf-95f0-d7aaed728e81.png)


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
내부조인을 이용해서 다중쿼리를 이용해서 만들었다.

* * *
