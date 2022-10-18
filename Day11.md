# 20번 문제(상위 n개 레코드) STRING, DATE
![image](https://user-images.githubusercontent.com/97568475/193965902-8f4861f7-00fd-4665-a1e6-8e89e6524c92.png)


* * *
# 20번 문제 나의 해답
```
SELECT animal_id, name from animal_ins
where name like '%el%' and animal_type like 'Dog'
order by name
```

* * *
# 20번 문제 피드백
없음.

* * *
# 21번 문제(상위 n개 레코드) STRING, DATE
![image](https://user-images.githubusercontent.com/97568475/193965992-4b4fad0f-0d07-46d4-bd39-f4ce47d57df0.png)


* * *
# 21번 문제 나의 해답
```
SELECT animal_id, name, case 
when (sex_upon_intake like 'Neutered%' or sex_upon_intake like 'Spayed%') then 'O'
else 'X' 
end as '중성화'
from animal_ins
order by animal_id
```

* * *
# 21번 문제 피드백
if, case문을 잘 다룰 수 있는지 물어보는 문제 였던거 같다.

* * *
