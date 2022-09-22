# 5번 문제(동물 수 구하기) SUM,MAX,MIN
![image](https://user-images.githubusercontent.com/97568475/191645853-71113379-2469-4bef-a318-bce3a36f4dd5.png)

* * *
# 5번 문제 나의 해답
```
SELECT count(ANIMAL_TYPE) from ANIMAL_INS
```

* * *
# 5번 문제 피드백
없음

* * *
# 6번 문제(동명 동물 수 찾기) GROUP BY
![image](https://user-images.githubusercontent.com/97568475/191646072-04822639-f208-4bb5-a246-3b7491c6082b.png)

* * *
# 6번 문제 나의 해답
### 첫 번째 답
```
SELECT NAME, COUNT(NAME)
FROM ANIMAL_INS
group by NAME
order by NAME
```

### 두 번째 답
```
SELECT NAME, COUNT(NAME)
FROM ANIMAL_INS
group by NAME
having count(NAME) > 1
order by NAME
```

* * *
# 6번 문제 피드백
예시를 봤을 때 shadow가 1번 있었는데 예시답안에 나와 있지 않았을 때 1번 보다 더 많이 쓰인 이름들을 뽑아내는 문제였다.
그 포인트를 놓쳤다.

* * *
# 7번 문제(입양 시각 구하기(1)) GROUP BY
![image](https://user-images.githubusercontent.com/97568475/191646542-ebdf68c4-1166-4161-8807-31d2099657ad.png)

* * *
# 7번 문제 나의 해답
### 첫 번째 답
```
SELECT HOUR(DATETIME) AS HOUR, COUNT(DATETIME) AS COUNT
FROM ANIMAL_OUTS
where DATETIME between '2013-10-10 08:59:59' AND '2018-02-20 19:00:01'
GROUP BY HOUR
ORDER BY HOUR asc
```

### 두 번째 답
```
SELECT HOUR(DATETIME) AS HOUR, COUNT(DATETIME) AS COUNT
FROM ANIMAL_OUTS
where HOUR(datetime) >= 9 AND HOUR(DATETIME) <= 19
GROUP BY HOUR(DATETIME)
order by hour(datetime)
```

* * *
# 7번 문제 피드백
처음 답을 했을 때는 DATETIME값을 뽑아서 정렬을 한다음에 가장 처음이 언제인지 그다음 제일 마지막날이 언제인지 알아낸다음 그 사이값을 뽑아냇다
하지만 조건에서 09:00~19:59분으로 되어 있었고 그 외의 값들이 출력되었다.

그리고 나서 조건에 맞게 2번째 답으로 정답을 맞추었다.
