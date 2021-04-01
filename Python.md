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
## 2. 출력
print함수로 문자열을 입력하려면 '' 또는 "" 으로 감싸야 한다.
```Python
print('Life is short!')
print('use Python!')
```
print 함수로 계산식 출력하는 법 중 희한한 기호 세가지


```Python
print(13//5)
print(21%4)
print(2**5)
```
<ol>
<li>//는 나눗셈의 몫을 구할때 쓴다.</li>
<li>%는 나눗셈에서 나누고 난 나머지값을 나타낼 때 쓴다.</li>
<li>*갯수만큼 지수이다.</li>
</ol>
- 사칙연산은 다른 언어들과 동일하게 (+,-,/,*)사용

## 3. 자료형(Data type)
### 3.1 Boolean(불리언)
Boolean의 데이터 값은 항상 True, False 두가지 뿐이다.
코드 입력시 변수명 = True 혹은 False로 대문자로 작성해야 인식된다.
```Python
Boolean = True
print(3<8)
```
