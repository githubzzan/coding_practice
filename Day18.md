# 35번 문제(헤비 유저가 소유한 장소)
![image](https://user-images.githubusercontent.com/97568475/196601310-398bc6cf-f7ee-4daf-95f0-d7aaed728e81.png)


* * *
# 35번 문제 나의 해답
```
SELECT p.ID, p.NAME, g.HOST_ID
FROM PLACES as p
INNER JOIN 
    (SELECT HOST_ID, count(ID) as c 
     FROM PLACES GROUP BY HOST_ID 
     HAVING c >= 2) as g 
     ON p.HOST_ID = g.HOST_ID
ORDER BY p.ID
```

* * *
# 35번 문제 피드백
내부조인을 이용해서 다중쿼리를 이용해서 만들었다.

* * *
