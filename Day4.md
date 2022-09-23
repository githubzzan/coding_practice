# 8번 문제(동물 수 구하기) SUM,MAX,MIN
![image](https://user-images.githubusercontent.com/97568475/191909343-edfcc598-aa92-4da8-9c34-181594a8b71f.png)

* * *
# 8번 문제 나의 해답
```
SELECT MIN(DATETIME) FROM ANIMAL_INS
ORDER BY DATETIME
```

* * *
# 8번 문제 피드백
없음

* * *
# 9번 문제(동물 수 구하기) SUM,MAX,MIN
![image](https://user-images.githubusercontent.com/97568475/191909118-8c5cd999-5405-4916-8aad-9c9b0823a12b.png)

* * *
# 9번 문제 나의 해답
첫 번째 답
```
SELECT HOUR(DATETIME) AS HOUR, COUNT(DATETIME) AS COUNT
FROM ANIMAL_OUTS
where HOUR(datetime) >= 0 AND HOUR(DATETIME) <= 23
GROUP BY HOUR(DATETIME)
order by hour(datetime)
```

두 번째 답
```
SELECT HOUR(DATETIME) AS HOUR, count(ifnull(a.DATETIME,0)) AS COUNT 
from (select count(*) as DATETIME
from ANIMAL_OUTS
where HOUR(DATETIME) >= 0 AND HOUR(DATETIME) <=23
GROUP BY HOUR(DATETIME))
as a
```

* * *
# 9번 문제 피드백
9번은 해결하지 못하였다. 내일 다시 도전할 계획이다.
지난번 문제처럼 해결할려고 하였으나 HOUR값이 없는값도 표시를 해야한다.
그리고 GROUP BY null값을 표기하는 방법을 찾고 있었으나 해결하지 못하였다.
내일 다시 도전할 것이다.
