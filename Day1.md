# 1번
문제 설명
ANIMAL_INS 테이블은 동물 보호소에 들어온 동물의 정보를 담은 테이블입니다. ANIMAL_INS 테이블 구조는 다음과 같으며, ANIMAL_ID, ANIMAL_TYPE, DATETIME, INTAKE_CONDITION, NAME, SEX_UPON_INTAKE는 각각 동물의 아이디, 생물 종, 보호 시작일, 보호 시작 시 상태, 이름, 성별 및 중성화 여부를 나타냅니다.

NAME	TYPE	NULLABLE
ANIMAL_ID	VARCHAR(N)	FALSE
ANIMAL_TYPE	VARCHAR(N)	FALSE
DATETIME	DATETIME	FALSE
INTAKE_CONDITION	VARCHAR(N)	FALSE
NAME	VARCHAR(N)	TRUE
SEX_UPON_INTAKE	VARCHAR(N)	FALSE
동물 보호소에 들어온 모든 동물의 아이디와 이름을 ANIMAL_ID순으로 조회하는 SQL문을 작성해주세요. SQL을 실행하면 다음과 같이 출력되어야 합니다.

ANIMAL_ID	NAME
A349996	Sugar
A350276	Jewel
A350375	Meo
A352555	Harley
A352713	Gia
A352872	Peanutbutter
A353259	Bj

-------------------------------------------------------------------------------
# 1번 해답 코드

### SELECT ANIMAL_ID, NAME
### from ANIMAL_INS
-------------------------------------------------------------------------------
# 1번 피드백

### 없음

-------------------------------------------------------------------------------
# 2번
문제 설명
ANIMAL_INS 테이블은 동물 보호소에 들어온 동물의 정보를 담은 테이블입니다. ANIMAL_INS 테이블 구조는 다음과 같으며, ANIMAL_ID, ANIMAL_TYPE, DATETIME, INTAKE_CONDITION, NAME, SEX_UPON_INTAKE는 각각 동물의 아이디, 생물 종, 보호 시작일, 보호 시작 시 상태, 이름, 성별 및 중성화 여부를 나타냅니다.

NAME	TYPE	NULLABLE
ANIMAL_ID	VARCHAR(N)	FALSE
ANIMAL_TYPE	VARCHAR(N)	FALSE
DATETIME	DATETIME	FALSE
INTAKE_CONDITION	VARCHAR(N)	FALSE
NAME	VARCHAR(N)	TRUE
SEX_UPON_INTAKE	VARCHAR(N)	FALSE
동물 보호소에 가장 먼저 들어온 동물의 이름을 조회하는 SQL 문을 작성해주세요.

예시
예를 들어 ANIMAL_INS 테이블이 다음과 같다면

ANIMAL_ID	ANIMAL_TYPE	DATETIME	INTAKE_CONDITION	NAME	SEX_UPON_INTAKE
A399552	Dog	2013-10-14 15:38:00	Normal	Jack	Neutered Male
A379998	Dog	2013-10-23 11:42:00	Normal	Disciple	Intact Male
A370852	Dog	2013-11-03 15:04:00	Normal	Katie	Spayed Female
A403564	Dog	2013-11-18 17:03:00	Normal	Anna	Spayed Female
이 중 가장 보호소에 먼저 들어온 동물은 Jack입니다. 따라서 SQL문을 실행하면 다음과 같이 나와야 합니다.

NAME
Jack
※ 보호소에 가장 먼저 들어온 동물은 한 마리인 경우만 테스트 케이스로 주어집니다.

-------------------------------------------------------------------------------
# 2번 내가 쓴 코드

### SELECT ANIMAL_ID, NAME, DATETIME FROM ANIMAL_INS
### ORDER BY NAME, DATETIME DESC

-------------------------------------------------------------------------------
# 2번 피드백

### 없음
