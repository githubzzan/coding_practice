# 28번 문제(경기도에 위치한 식품창고 목록 출력하기) IS NULL
![image](https://user-images.githubusercontent.com/97568475/195523619-598ac8ff-7806-41e3-bf7d-2cb9f974ac6a.png)

* * *
# 28번 문제 나의 해답
```
SELECT FOOD_TYPE, REST_ID, REST_NAME, FAVORITES
from REST_INFO
where (food_type, favorites) in (select food_type, max(favorites) from rest_info group by food_type)
order by FOOD_TYPE desc
```

* * *
# 28번 문제 피드백
where in 절 사용 in 안에서 다시 최대값찾아내기

* * *
# 29번 문제(나이 정보가 없는 회원 수 구하기) IS NULL
![image](https://user-images.githubusercontent.com/97568475/195740331-da915f3b-26f4-4b22-9f2e-f305cf254b8a.png)



* * *
# 29번 문제 나의 해답
```
SELECT count(USER_ID) as users from user_info
where age is null
```

* * *
# 29번 문제 피드백
간단한 count, is null 문제

* * *
