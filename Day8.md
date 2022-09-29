# 13번 문제(있었는데요 없었습니다) JOIN
![image](https://user-images.githubusercontent.com/97568475/192667723-a2e1ff46-b614-460a-8618-547690182838.png)

* * *
# 13번 문제 나의 해답
```
SELECT a.ANIMAL_ID, a.NAME
FROM ANIMAL_INS as a
LEFT JOIN ANIMAL_OUTS as b
ON a.ANIMAL_ID = b.ANIMAL_ID
WHERE a.DATETIME > b.DATETIME
ORDER BY a.DATETIME
```

* * *
# 13번 문제 피드백
간단하게 DATETIME 값을 비교하면 되는것 이었는데 너무 복잡하게 생각을 했던거 같다.
