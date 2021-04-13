# Python

## 1. 변수(Variable)

변수는 일시적으로, 또는 영구적으로 값(value)를 저장하기 위해 사용한다.
예를 들어, 내 통장잔고가 300만원이 있었는데 노트북을 구입하느라 70만원을 사용했고, 남은 통장잔고는 230만원일때, 아래와 같이 변수를 사용하여 표현할 수 있다.

```Python
account = 300
notebook = 70
account = account - notebook
print ('account')
```

이 경우 account로 지정한 변수는 최초에 300, 연산 후 230이 된다.

### 1.1 변수명 짓는 규칙

- 숫자는 맨 앞에 사용하지 않는다(에러 발생). 중간이나 맨 뒤에 사용한다.
- 영어 소문자로 시작한다.
- 2개의 단어를 쓰면 언더바 사용을 권장한다. ex) shoe_size
- 변수 이름에는 글자, 숫자, 밑줄만 쓸 수 있다.
- s 나 s_n 처럼 축약하지 말고 student, student_name 과 같이 쓴다.

## 2. 입력

- 사용자가 입력한 값을 프로그램 안에 넣는 방법.

### 2.1 input 함수

- input 함수는 입력하기 위한 함수이다.

```Python
example = input()
example = input("쓰고싶은 내용")
```

코드 입력시 변수 example의 값을 입력하라고 창이 뜨게 되며 해당 창에 변수의 값을 입력한다.
그리고 그 창에 입력한 값은 문자열로 출력된다.
input() 괄호 안에 따옴표로 감싸 문자열과 변수의 값을 같이 쓸 수도 있다.

### 2.2 type 함수

변수의 값을 넣을 때 사용하면 기존에 문자열로 입력한 변수를 숫자로 인식한다.

```Python
name = "123"
name_int = int(name)
print (name_int)
```

123

<hr>

- int : 정수(integer)
- float : 부동소숫점
- str : 문자열(string)
- bool : 불리언(Boolean)
<hr>

#### 2.2.1 Type casting

서로 다른 타입이어도 변환이 가능하다.

- int to float(정수를 부동소숫점으로)

```Python
float(3)
```

3.0

- float to int(부동소숫점을 정수로)

```Python
int(3.4)
```

4 (부동소숫점을 정수로)

#### 2.2.2 type ( )

변수 지정후 print(type(변수명)) 입력하면 해당 변수가 int인지 float인지 str인지 bool인지 알려준다.

```Python
variable1 = 4.5
print (type(variable1))
```

<class 'float'>

## 3. 출력

### 3.1 print 함수

화면에 문자나 숫자, 변수 등을 출력한다.

#### 3.1.1 문자열(str) 입력

print함수로 문자열을 입력하려면 '' 또는 "" 으로 감싸야 한다.

```Python
print ('Life is short!')
print ('use Python!')
```

print 함수로 계산식 출력하는 법 중 특이한 기호들

| code          | description                                         |
| ------------- | --------------------------------------------------- |
| print(13//5)  | //는 나눗셈의 몫을 구할때 쓴다.                     |
| print(21%4)   | %는 나눗셈에서 나누고 난 나머지값을 나타낼 때 쓴다. |
| print(2\*\*5) | **는 거듭제곱이다. 즉 (x ** y) 일때 x의 y승         |

- 사칙연산은 다른 언어들과 동일하게 (+,-,/,\*)사용

### 3.2 다양한 출력 방법(자주 안씀)

| 단축 표기 | 뜻                                        |
| --------- | ----------------------------------------- |
| %s        | string - 한글자 이상의 문자열 입력시 사용 |
| %e        | character - 한글자의 문자 입력시 사용     |
| %d        | int - 정수                                |
| %f        | float - 부동소숫점                        |

- 문자열 안에 넣어서 사용한다.

```python
print ("I am a %s, you are a %s.")
%("boy","girl")
```

## 4.자료형(Data type)

### 4.1 Boolean(불리언)

Boolean의 데이터 값은 항상 True, False 두가지 뿐이다.
코드 입력시 변수명 = True 혹은 False로 대문자로 작성해야 인식된다.

```Python
Boolean = True
print (3<8)
```

#### 4.1.1 print문에서의 사용

```Python
print (4 < 7) True
print (4 > 2) False
print (3 == 3) 서로 같은지
print (3 != 3) 서로 다른지
print (3 >= 3) 이상
print (3 <= 3) 이하
```

# 5. 문자열

## 5.1 문자열 메서드

| 함수      | 설명                                                       | 예시                           |
| --------- | ---------------------------------------------------------- | ------------------------------ |
| count()   | 특정 문자열이 등장하는 수를 구함.                          | print(변수명.count("kim"))     |
| find()    | 특정 문자열이 몇번째에 처음 등장하는지 표시.               | print(변수명.find("kim"))      |
| replace() | 일괄적으로 ','왼쪽의 문자열을 오른쪽 문자열로 한번에 변환. | print(변수명.replace("k","L")) |
| strip()   | 문자열의 양쪽에 있는 공백이나 () 안에 지정한 내용 제거     | print(변수명.strip())          |

변수로 여러줄의 문자열을 입력하고자 할 때 """ 으로 감싸면 여러 줄의 문자열을 변수로 입력할 수 있다.

## 5.2 문자열 인덱싱과 슬라이싱

![python index](https://res.cloudinary.com/practicaldev/image/fetch/s--A7oqOWqx--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/1wr90mjnil60r7226bgq.png)

> Index란 번호를 매기는 것을 의미한다.

### 5.2.1 Index

문자열 내에서 입력한 번호에 위치하는 데이터를 표시하는 방법이다. 0부터 시작하며 역순은 -1부터 시작한다.

```python
example = 'python'
print (example[2])
```

t

```python
example = 'python'
print (example[-2])
```

o

### 5.2.2 Slice

대괄호 안에서 몇번째 부터 몇번째 '직전' 까지의 문자열만 추출하는 방법이다.

```python
example = 'python'
print (example[2:4])
```

th

# 6. 리스트

## 6.1 리스트 선언

### 6.1.1 대괄호 사용하여 리스트 선언하기

[] 대괄호 안에 리스트의 내용을 넣는다.

```python
cars = ['benz', 'audi', 'bmw']
print (cars)
```

['benz', 'audi', 'bmw']

### 6.1.2 변수로 리스트 런언하기

list(변수명)

```python
a = 'asd'
a = list(a)
print (a)
```

['a', 's', 'd']

## 6.2 리스트 추가

.append 사용시 리스트의 맨 끝에 데이터를 새로 추가한다.  
.insert 사용시 입력한 인덱스 번호 위치에 데이터를 새로 추가하고 기존의 데이터는 한칸 뒤로 밀려난다.

```python
cars = ['benz', 'audi', 'bmw']

cars.append('hyundai')
cars.insert(1,'kia')

print (cars)
```

['benz', 'kia', 'audi', 'bmw', 'hyundai']

## 6.3 리스트 삭제

.remove 또는 del 명령어로 삭제가 가능하다.

```python
cars = ['benz', 'audi', 'bmw']

cars.remove('benz')
del cars[1]

print (cars)
```

['audi']

- cars.remove('benz') 로 리스트가 'audi','bmw' 가 된 상태에서 del cars[1] 명령을 받아 인덱스번호 1번째 자리에 있는 'bmw'를 제거하였다.

['porsche', 'audi', 'bmw']

## 6.4 리스트 수정

```python
cars = ['benz', 'audi', 'bmw']
cars[0] = 'porsche'

print (cars)
```

['porsche', 'audi', 'bmw']

- 변수명[인덱스번호] = '수정할 데이터' 로 선언하여 기존 내용을 수정할 데이터로 바꾼다.

# 7. 조건문

콜론`:` 으로 닫고 tab으로 띄우고 print("실행문") 작성한다.

```python
cash = int(input("돈 얼마있어?"))
if cash > 15000:
    print ("점심 나가서 먹자")
```

input 값이 15000보다 크면 "점심 나가서 먹자" 출력.

## 7.1 and 조건

- 조건 1, 조건 2 둘다 맞아야 실행된다.

```python
age1 = int(input("홍길동의 나이는?"))
age_digit1 = int(age1)
age2 = int(input("심청이의 나이는?"))
age_digit2 = int(age2)

if age_digit1 >= 19 and age_digit2 >= 19:
    print ("성인입니다")
```

홍길동의 나이와 심청이의 나이가 둘 다 19 이상이어야 '성인입니다' 출력됨.

## 7.2 or 조건

- 둘 중 하나만 맞아도 실행된다.

```python
age1 = int(input("홍길동의 나이는?"))
age_digit1 = int(age1)
age2 = int(input("심청이의 나이는?"))
age_digit2 = int(age2)

if age_digit1 >= 19 or age_digit2 >= 19:
    print ("둘다 성인 맞니? 아닌거같은데.")
```

둘 중 한명만 인풋값 19 이상이면 print문 출력됨.

## 7.3 not 조건

- 작성한 조건이 아닐경우 실행된다.

```python
age1 = int(input("홍길동의 나이는?"))
age_digit1 = int(age1)

if not age_digit1 >= 19:
    print ("미성년자")
```

홍길동의 나이가 19 이상일 경우 미성년자 라고 출력되게 입력하였지만 if not을 앞에 붙여서 해당 조건이 아닐경우 미성년자 라고 출력이 됨.
즉 19 미만의 값을 줄 경우 미성년자 라고 출력됨.

## 7.4 else 구문

- if 조건에 해당하지 않는 값들에 대해 실행할 내용을 else 구문으로 만들어준다.
- elif와 같이 사용시 elif구문보다 위에 먼저 올 수 없다.

```python
age = int(input("나이는?"))
if age >= 19:
    print ("성인입니다")
else:
    print ("미성년입니다")
```

나이가 19세 미만이면 '미성년입니다' 출력.

## 7.5 elif 구문

조건이 여러가지 일 때 if조건에 해당하지 않는 조건의 값에 대해 실행할 내용을 elif 구문으로 만들어준다.

```python
age = int(input("나이는?"))
if age >= 19:
    print ("성인입니다")
elif age >= 13 and age < 19:
    print ("청소년입니다")
else:
    print ("아동입니다")
```

나이가 19세 이상일 경우 '성인입니다' 출력.  
13세 이상 19세 미만일 경우 '청소년입니다' 출력.  
둘 다 해당하지 않으면 '아동입니다' 출력.

# 8. 반복문

## 8.1 for 반복문

### 8.1.1 for 반복문의 기본 형태

```python
for 반복자 in 반복할 수 있는 것:
    실행코드
```

반복자 : 변수  
반복할 수 있는 것 : 문자열, 리스트, 딕셔너리, 범위  
실행코드 : print ()

### 8.1.2 for 반복문과 range(범위 자료형) 함께 사용하기

```python
for example in range(100):
    print("출력")
```

'출력' 100번 출력

## 8.2 while 반복문

- 참일 경우에만 반복되고 아닐경우 실행되지 않는다.

```python
while True:
    print (".",end="")
```

.............................이 무한하게 반복된다.
