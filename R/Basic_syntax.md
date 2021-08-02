# R의 기초 사용법 정리
## \# (해시 기호)
- 주석(Comment)의 기능
- 프로그램 전반적인 내용, 명령어의 내용 등이 무엇을 의미하는지 알 수 있도록 사용자가 설명을 달아주는 기능
- \# 뒤에 있는 한 줄이 주석으로 처리되며, R에서 지정된 문법을 검사하지 않음
- 단, 한 줄만 주석으로 처리되므로 다른 줄도 하고 싶으면 해당 줄 앞에 #를 써야 함
<br /><br />

## ;(세미콜론)
- 하나의 명령어가 끝났음을 알려주는 기능
- 한 줄에 하나의 명령밖에 없으면 세미콜론을 해 주지 않아도 명령어가 끝났음을 인식함
<br /><br />

## Ctrl + Enter(컨트롤+엔터)
- R의 명령어를 실행하는 기능
- 명령어가 한 줄인 경우 마우스의 위치는 해당 줄의 아무 곳에 있어도 상관이 없음
- 명령어가 두 줄 이상인 경우 반드시 해당 명령어가 있는 곳을 블록을 잡고 실행
<br /><br />

## Shift + Enter(시프트 + 엔터)
- 동일한 위치에 다른 Argument(함수에 들어가는 값)를 올 수 있도록 해줌
- Shift + Enter를 이용해 명령어가 길게 표현되는 것을 방지함
<br /><br />

## 대소문자
- R은 대소문자를 구별(Case Sensitive)
- 소문자 ‘x’와 대문자 ‘X’는 전혀 다른 것을 의미하기 때문에 주의해야 함
<br /><br />

## 연산자
### 산술 연산자(Arithmetic Operator)
- 1개 이상의 수치에 대한 연산
- 더하기, 빼기, 곱하기, 나누기, 거듭제곱, 몫, 나머지를 구할 수 있음
- 산술 연산자의 우선순위(높은 순)
  - 괄호 (( ))
  - 거듭제곱(^, **)
  - 곱하기(*), 나누기(/)
  - 더하기(+), 빼기(-)
- 동일한 우선순위의 산술 연산자가 나열된 경우 왼쪽이 오른쪽보다 우선순위를 갖게 됨
<br /><br />

### 할당 연산자(Allocation Operator)
- 어떤 객체의 이름(변수 이름, 데이터 이름)에 특정한 값을 저장할 때 사용하는 연산자
- 객체에 무엇이 있는지를 일부러 새로운 명령어를 실행하지 않아도 알 수 있는 기능
<br />

연산자 | 설명 | 사용 예시
:-:|:-:|:-:
<- | 오른쪽의 값을 왼쪽의 이름에 저장 | x <- 3
= | 오른쪽의 값을 왼쪽의 이름에 저장 | y = 4
-> | 왼쪽의 값을 오른쪽의 이름에 저장 | 5 -> z
<br /><br />

### 할당 연산자(Allocation Operator)
- 두 개 값에 대한 비교로써 맞으면 TRUE, 
- 맞지 않으면 FALSE를 반환하여 비교 연산의 최종적인 결과가 갖는 값
<br />

연산자 | 설명 | 사용 예시 | 사용 결과
:---:|:---:|:---:|:---:
\> | 크다 | 3 > 4 | FALSE
\>= | 크거나 같다 | 3 >= 4 | FALSE
< | 작다 | 3 < 4 | TRUE
<= | 작거나 같다 | 3 <= 4 | TRUE
== | 같다 | 3 == 4 | FALSE
!= | 같지 않다 | 3 != 4 | TRUE
! | 부정 | !(3 == 4) | TRUE
<br /><br />

### 논리 연산자(Logical Operator)
- 두 개 이상의 조건을 비교하여 결과를 냄
- &, &&는 모든 조건이 참일 때에만 최종적인 결과가 TRUE가 됨
- |, ||는 조건 중에서 하나라도 참이면 최종적인 결과가 TRUE가 됨
- 벡터(Vector)가 오면 &와 &&의 결과 또는 |와 ||의 결과에는 차이가 있음
<br />

연산자 | 설명 | 사용 예시
---|---|---
& | AND | (조건1)  & (조건2)
&& | AND | (조건1) && (조건2)
\| | OR | (조건1) \| (조건2)
\|\| | OR | (조건1) \|\| (조건2)

<br /><br />

## 데이터 유형
### 기본데이터유형
- 기본적인 데이터 유형에는 수치형, 문자형, 논리형, 복소수형이 있음
- 수치형, 문자형, 논리형이 자주 사용
- 복소수형은 수학분야를 다룰 때에 사용

데이터 유형 | 설명 
---|---
수치형(Numeric) | 숫자로 되어 있으며, 정수형(Integer)과 실수형(Double)이 있음 
문자형(Character) |  하나의 문자 또는 문자열로 되어 있으며, “” 또는 ‘’로 묶여 있음
논리형(Logical) | 참과 거짓의 논리값으로 TRUE(or T)나 FALSE(or F)를 가짐
복소수형(Complex) |  실수와 허수로 이루어진 복소수

<br /><br />

### 특수한형태의데이터유형
데이터 유형 | 설명 
---|---
NULL | 존재하지 않는 객체로 지정할 때 사용
NA | Available의 약자로 결측치(Missing value)를 의미
NaN | Not available Number의 약자로 수학적으로 계산이 불가능한 수를 의미 <br />※예 : sqrt(-3)로 음수에 대한 제곱근은 구할 수 없음 
Inf | Infinite의 약자로 양의 무한대
-Inf | 음의 무한대