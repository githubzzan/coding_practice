# 15번 문제(상위 n개 레코드) SELECT
![image](https://user-images.githubusercontent.com/97568475/193711953-dac874de-aaa3-417d-afa5-228e72b36318.png)


* * *
# 15번 문제 나의 해답
```
SELECT name from animal_ins
order by datetime
limit 1
```

* * *
# 15번 문제 피드백
없음.

* * *
# 16번 문제(최대값 구하기) SUM, MAX, MIN
![image](https://user-images.githubusercontent.com/97568475/193712135-d4f5cb87-f461-4f5d-801d-78d16d9b8cce.png)



* * *
# 16번 문제 나의 해답
```
SELECT MAX(DATETIME) AS 시간 FROM ANIMAL_INS
```

* * *
# 16번 문제 피드백
없음.

* * *
# 17번 문제(아픈동물찾기) SELECT
![image](https://user-images.githubusercontent.com/97568475/193715523-337bb86f-73f0-46cd-957f-dab64ccb5147.png)



* * *
# 17번 문제 나의 해답
```
SELECT ANIMAL_ID, NAME FROM ANIMAL_INS
where intake_condition = 'sick'
order by animal_id
```

* * *
# 17번 문제 피드백
없음.

* * *
# 18번 문제(어린동물 찾기) SELECT
![image](https://user-images.githubusercontent.com/97568475/193717977-0601312f-7a2a-4f4c-9b82-c596cce6aac3.png)




* * *
# 18번 문제 나의 해답
```
SELECT animal_id, name from animal_ins
where intake_condition != 'aged'
order by animal_id
```

* * *
# 18번 문제 피드백
없음.

* * *
