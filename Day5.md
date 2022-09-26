# 9번 문제(입양 시각 구하기(2)) GROUP BY
![image](https://user-images.githubusercontent.com/97568475/191909118-8c5cd999-5405-4916-8aad-9c9b0823a12b.png)

* * *
# 9번 문제 나의 해답
세 번째 답
```
SET @HOUR = 0;
SELECT (@HOUR := @HOUR +1) AS HOUR,
    (SELECT COUNT(HOUR(DATETIME)) 
    FROM ANIMAL_OUTS 
    WHERE HOUR(DATETIME)=@HOUR) AS COUNT 
    FROM ANIMAL_OUTS
WHERE @HOUR < 24;
```
* * *
네 번째 답
```
SET @HOUR = -1;
SELECT (@HOUR := @HOUR +1) AS HOUR,
    (SELECT COUNT(HOUR(DATETIME)) 
    FROM ANIMAL_OUTS 
    WHERE HOUR(DATETIME)=@HOUR) AS COUNT 
    FROM ANIMAL_OUTS
WHERE @HOUR < 23;
```
* * * 
# 9번 문제 피드백

처음 세 번째 답을 사용햇을 때는 0의 값이 나타나지 않았다
그래서 네 번째 답이 나왔습니다.

## 사용자 정의 변수

* SET 변수 선언
```
SET @변수이름 = 대입값; 
-- or 
SET @변수이름 := 대입값;
 
 
SELECT @변수이름 := 대입값;
```
 * SET 이외의 명령문에서는 = 가 비교연산자로 취급되기 때문에, SELECT 로 변수를 선언하고 값을 대입할 때는 := 를 사용한다.

* 사용자 정의 변수 사용법
``` 
SET @start = 15, @finish = 20;

-- 또는
 
SELECT @start := 15, @finish := 20;
 
SELECT * FROM employee WHERE id BETWEEN @start AND @finish;
```

## 지역 변수 선언 및 초기화
```
DELIMITER $$
  CREATE PROCEDURE testPro(var1 INT)
  BEGIN
    DECLARE start INT DEFAULT 1; -- int start = 1 과 같다.
    DECLARE finish INT DEFAULT 10;
 
    SELECT var1, start, finish;
    SELECT * FROM employees WHERE id BETWEEN start AND fisnish;
  END $$
DELIMITER ;
 
CALL testPro(1);
```

* DECLARE 로 먼저 선언 후에 사용하며, 지역변수로 사용하거나 스토어 프로시저(저장 프로시저)의 매개변수로 사용될 수 있다. 또한 변수의 범위는 변수가 선언되는 곳의 BEGIN ~ END 블록으로 제한된다.

## 시스템 변수
* 시스템 변수 확인하기
```
SHOW GLOBAL VARIABLES; 
-- 모든 시스템 변수를 확인한다.
 
SHOW GLOBAL VARIABLES LIKE 'CHAR%'; 
-- 변수 이름이 CHAR로 시작되는 시스템 변수를 확인한다.
```

* 시스템 변수 수정하기
```
SET GLOBAL [시스템 변수 이름] = 적용할 값 ;
// 예를들어 character_set_server의 값을 utf8 로 바꾸고 싶다면,
SET GLOBAL character_set_server = utf8;
```

