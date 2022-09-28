# 12번 문제(없어진 기록 찾기) JOIN
![image](https://user-images.githubusercontent.com/97568475/192469594-7c6266ce-7a0d-4e08-bac0-b715530f7a6b.png)

* * *
# 12번 문제 나의 해답
### 두 번째 해답
```
SELECT b.ANIMAL_ID, b.NAME from ANIMAL_INS AS a
right JOIN ANIMAL_OUTS AS b
on a.ANIMAL_ID = b.ANIMAL_ID
where a.animal_id is null
order by b.animal_ID
```

* * *
# 12번 문제 피드백
값을 오른쪽으로 join으로 밀어 넣고 서로 겹치지 않는것을 뽑아오는 sql문 이었다.
'where a.animal_id is null' 이 코드를 추가함으로써 그 해답을 찾았다.

# 13번 문제(있었는데요 없었습니다) JOIN
![image](https://user-images.githubusercontent.com/97568475/192667723-a2e1ff46-b614-460a-8618-547690182838.png)

* * *
# 13번 문제 나의 해답
```

```

* * *
# 13번 문제 피드백
MySQL DateTime 포맷과 문자열 날짜값의 비교, 그리고 date_format() 날짜 포매팅을 공부하고 해답을 내봐야겠다.
