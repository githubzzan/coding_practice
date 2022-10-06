# 21번 문제(DATETIME에서 DATE로 형 변환) STRING, DATE
![image](https://user-images.githubusercontent.com/97568475/194197080-21997cf7-06a6-446a-a844-8c064afd793e.png)


* * *
# 21번 문제 나의 해답
```
SELECT animal_id, name, date_format(datetime, '%Y-%m-%d') as 날짜
from animal_ins
order by animal_id
```

* * *
# 21번 문제 피드백
date_format을 활용할줄 아는지에 관한 문제인거 같다.

* * *
# 22번 문제(역순 정렬하기) SELECT
![image](https://user-images.githubusercontent.com/97568475/194197749-4c794ed4-2c16-4e6a-9ad1-a335149cb2cf.png)


* * *
# 22번 문제 나의 해답
```
SELECT name, datetime from animal_ins
order by animal_id desc
```

* * *
# 22번 문제 피드백
order by asc, desc 정렬을 다룰줄 아는지 묻는 문제이다.

* * *
# 23번 문제(이름이 없는 동물의 아이디) IS NULL
![image](https://user-images.githubusercontent.com/97568475/194197953-5cbc9dbe-fe24-4bb8-8983-978d50df5434.png)


* * *
# 23번 문제 나의 해답
```
SELECT animal_id from animal_ins
where name is null
```

* * *
# 23번 문제 피드백
IS NULL을 이해하고 있는지 파악하는 문제

* * *
# 24번 문제(이름이 없는 동물의 아이디) IS NULL
![image](https://user-images.githubusercontent.com/97568475/194202433-4f26f99d-3713-4fd5-8cf7-20f6a1f36c69.png)


* * *
# 24번 문제 나의 해답
```
SELECT a.animal_id, a.name from animal_ins as a
join animal_outs as b 
on a.animal_id = b.animal_id
order by b.datetime - a.datetime desc
limit 2
```

* * *
# 24번 문제 피드백
STRING,Date를 활용하여 join을 쓸 수 있는가 다루는 문제

* * *
