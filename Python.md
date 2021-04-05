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
print(name_int)
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
print(type(variable1))
```

<class 'float'>

## 3. 출력

### 3.1 print 함수

화면에 문자나 숫자, 변수 등을 출력한다.

#### 3.1.1 문자열(str) 입력

print함수로 문자열을 입력하려면 '' 또는 "" 으로 감싸야 한다.

```Python
print('Life is short!')
print('use Python!')
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
print("I am a %s, you are a %s.")
%("boy","girl")
```

## 4.자료형(Data type)

### 4.1 Boolean(불리언)

Boolean의 데이터 값은 항상 True, False 두가지 뿐이다.
코드 입력시 변수명 = True 혹은 False로 대문자로 작성해야 인식된다.

```Python
Boolean = True
print(3<8)
```

#### 4.1.1 print문에서의 사용

```Python
print(4 < 7) True
print(4 > 2) False
print(3 == 3) 서로 같은지
print(3 != 3) 서로 다른지
print(3 >= 3) 이상
print(3 <= 3) 이하
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
print(example[2])
```

t

```python
example = 'python'
print(example[-2])
```

o

### 5.2.2 Slice

대괄호 안에서 몇번째 부터 몇번째 '직전' 까지의 문자열만 추출하는 방법이다.

```python
example = 'python'
print(example[2:4])
```

th
