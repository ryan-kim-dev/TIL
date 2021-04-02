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
* 숫자는 맨 앞에 사용하지 않는다(에러 발생). 중간이나 맨 뒤에 사용한다.
* 영어 소문자로 시작한다.
* 2개의 단어를 쓰면 언더바 사용을 권장한다. ex) shoe_size
* 변수 이름에는 글자, 숫자, 밑줄만 쓸 수 있다.
* s, s_n 으로 축약하지 말고 student, student_name 과 같이 쓴다.

## 2. 입력
사용자가 입력한 값을 프로그램 안에 넣는 방법.
### 2.1 type 함수

변수의 값을 넣을 때 사용하면 기존에 문자열로 입력한 변수를 숫자로 인식한다.
```Python
name = "123"
name_int = int(name)
print(name_int)
```
123
<hr>

* int : 정수(integer)
* float : 부동소숫점
* str : 문자열(string)
* bool : 불리언(Boolean)
<hr>

####2.1.1 type casting
서로 다른 타입이어도 변환이 가능하다.
```Python
float(3)
```
3.0 (정수를 부동소숫점으로)

```Python
int(3.4)
```
4 (부동소숫점을 정수로)

#### 2.1.2 type ( )
변수 지정후 print(type(변수명)) 입력하면 해당 변수가 int인지 float인지 str인지 bool인지 알려준다.
```Python
변수 = 4.5
print(type(변수))
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


```Python
print(13//5)
print(21%4)
print(2**5)
```
<ol>
<li>//는 나눗셈의 몫을 구할때 쓴다.</li>
<li>%는 나눗셈에서 나누고 난 나머지값을 나타낼 때 쓴다.</li>
<li>2의 5승을 출력하라는 코드</li>
</ol>
- 사칙연산은 다른 언어들과 동일하게 (+,-,/,*)사용


## 4. 자료형(Data type)
### 4.1 Boolean(불리언)
Boolean의 데이터 값은 항상 True, False 두가지 뿐이다.
코드 입력시 변수명 = True 혹은 False로 대문자로 작성해야 인식된다.
```Python
Boolean = True
print(3<8)
```
#### 4.1.1 print문에서의 사용
```Python
print(3 == 3) 서로 같은지
print(3 != 3) 서로 다른지
print(3 >= 3) 이상
print(3 <= 3) 이하
```
