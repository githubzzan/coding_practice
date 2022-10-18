# 33번 문제(카테고리 별 상품 개수 구하기) STRING, Date
![image](https://user-images.githubusercontent.com/97568475/196315091-9becc319-7c2a-4b66-a7fd-8a4a201aa98b.png)


* * *
# 33번 문제 나의 해답
```
SELECT substr(product_code, 1, 2) as category, count(product_id) as products
from product
group by category
order by category
```

* * *
# 33번 문제 피드백
substr('읽을거리',1,2) -> 1번째 부터 읽으시고, 2글자만 가져오시오 활용

* * *
# 34번 문제(카테고리 별 상품 개수 구하기) STRING, Date
![image](https://user-images.githubusercontent.com/97568475/196324799-31af01d4-b0b0-4a90-965a-6b3ff47861aa.png)


* * *
# 34번 문제 나의 해답
처음답
```
SELECT MEMBER_ID, MEMBER_NAME, GENDER, DATE_OF_BIRTH from MEMBER_PROFILE
where DATE_format(DATE_OF_BIRTH, '%m') = '03' and gender like 'W' and TLNO is not null
order by MEMBER_ID
```

두번째 답
```
SELECT MEMBER_ID, MEMBER_NAME, GENDER, date_format(DATE_OF_BIRTH, '%Y-%m-%d') from MEMBER_PROFILE
where DATE_format(DATE_OF_BIRTH, '%m') = '03' and gender like 'W' and TLNO is not null
order by MEMBER_ID
```

* * *
# 34번 문제 피드백
DATE_OF_BIRTH 을 출력하니 시간값까지 나와있어서 date로 바꾸어주고 출력햇다.

* * *
