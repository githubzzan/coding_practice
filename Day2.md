# SQL 3번 문제(중복 제거하기)
![image](https://user-images.githubusercontent.com/97568475/191422338-3e1caba0-20a4-4395-a445-d5ee480bb1de.png)

* * *

# SQL 3번 문제 나의 해답
```
SELECT count(distinct NAME) from ANIMAL_INS
```

* * *
# SQL 3번 문제 피드백
없음

* * *
# SQL 4번 문제(고양이와 개는 몇 마리 있을까?)
![image](https://user-images.githubusercontent.com/97568475/191422699-5a400699-e1c4-413f-8691-eea47323f5ef.png)

* * *
# SQL 4번 문제 나의 해답
```
// 1번째 해답
SELECT ANIMAL_TYPE, COUNT(ANIMAL_TYPE) AS count
FROM ANIMAL_INS
GROUP BY ANIMAL_TYPE

// 2번째 해답
SELECT ANIMAL_TYPE, COUNT(ANIMAL_TYPE) AS count
FROM ANIMAL_INS
GROUP BY ANIMAL_TYPE
ORDER by animal_type
```

* * *
# SQL 4번째 문제 피드백
### 문제의 마지막에 이때 고양이를 개보다 먼저 조회해주세요. 라는 점을 놓친점







