# 10번 문제(이름이 있는 동물의 아이디) IS NULL
![image](https://user-images.githubusercontent.com/97568475/192454679-88853ea4-7bbc-43db-8aea-94b53a8cb099.png)

* * *
# 10번 문제 나의 해답
```
SELECT ANIMAL_ID FROM ANIMAL_INS where NAME is not null
```

* * *
# 10번 문제 피드백
없음.

* * *
# 11번 문제(NULL 처리하기) IS NULL
![image](https://user-images.githubusercontent.com/97568475/192454953-ba01beec-82de-4e3b-a697-3b903e3d88c4.png)

* * *
# 11번 문제 나의 해답
```
SELECT ANIMAL_TYPE, ifnull(NAME, 'No name'), SEX_UPON_INTAKE FROM ANIMAL_INS
```

* * *
# 11번 문제 피드백
없음.

* * *
# 12번 문제(없어진 기록 찾기) JOIN
![image](https://user-images.githubusercontent.com/97568475/192469594-7c6266ce-7a0d-4e08-bac0-b715530f7a6b.png)

* * *
# 12번 문제 나의 해답
```
SELECT b.ANIMAL_ID, b.NAME from ANIMAL_INS AS a
right JOIN ANIMAL_OUTS AS b
on a.ANIMAL_ID = b.ANIMAL_ID
```

* * *
# 12번 문제 피드백
아직 해결을 못한 상태이다. right join으로 옆으로 값을 밀어놓고 했지만 아직 미해결
