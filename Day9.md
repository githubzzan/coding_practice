# 14번 문제(오랜 기간 보호한 동물(1)) JOIN
![image](https://user-images.githubusercontent.com/97568475/193165328-2c461eb8-975b-469c-ac0c-14e72cd47676.png)


* * *
# 14번 문제 나의 해답
```
SELECT a.name, a.datetime from animal_ins as a
left outer join animal_outs as b
on a.animal_id = b.animal_id
where b.animal_id is null
order by a.datetime
limit 3
```

* * *
# 14번 문제 피드백
앞에 13번 문제랑 유사해서 풀기 쉬웠다. 추가된 limit 3 만 생각을 하면 되었다.

* * *
# 15번 문제(오랜 기간 보호한 동물(1)) JOIN
![image](https://user-images.githubusercontent.com/97568475/193166061-71753c39-50fd-470e-8114-1625de85bee8.png)


* * *
# 15번 문제 나의 해답
첫 번째 답
```
SELECT distinct a.animal_id, a.animal_type, a.name from animal_ins as a
join animal_outs as b
on a.animal_id = b.animal_id
where a.sex_upon_intake like 'intact%'
order by a.animal_id
```

두 번째 답
```
SELECT distinct a.animal_id, a.animal_type, a.name from animal_ins as a
join animal_outs as b
on a.animal_id = b.animal_id
where a.sex_upon_intake like 'intact%' and (b.sex_upon_outcome like 'spayed%' or b.sex_upon_outcome like 'neutered%')
order by a.animal_id
```

* * *
# 15번 문제 피드백
첫 번째 답을 적고 나서 intact 중성화 안한 애들만 찾아버렸다. 그 후에 보호소에 들어온 후 중성화가 된 애들도 선별하는것을 써주어서 정답이 되었다.
