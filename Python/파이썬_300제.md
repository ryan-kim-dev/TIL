# [초보자를 위한 파이썬 300제](https://wikidocs.net/book/922)

## 01. 파이썬 시작하기 001 ~010

- 004 print 기초

sep = "/"
sep = ";"
print문 안에서 쉼표로 구분하여 여러가지를 한번에 출력할때 공백을 /나 ;로 바꿔준다.

- 005 print 탭과 줄바꿈

파이썬에서 역슬래시는 \n 줄바꿈, \t tab 입력 등 명령어에 직접적으로 들어가는 내용이라 문자열에 아무 기능 없이 \를 쓰고 싶다면 \\ 두번 입력하면 \로 사용가능하다

- 009 print 줄바꿈

한줄에 두개 이상의 명령을 적으려면 ; 세미콜론을 사용한다
여러 print문을 한줄에 붙여서 작성해도 자동으로 줄바꿈되어 출력되니 줄바꿈되게 하지 않으려면 end = "" 써준다

```
print("samsung");print("lg")
```

```
samsung
lg
```

```
print("samsung", end = "");print("lg")
```

`samsunglg`

---

## 02. 파이썬 변수 011 ~ 020

- 012 변수 사용하기

변수값으로 정수 입력시 돈 단위표기로 쉼표 사용하면 파이썬에서 튜플로 인식하므로 쉼표 쓰지 않기

- 013 문자열 출력

print문 사용시 괄호 내부에서 +”추가하고 싶은 내용” 입력하면 변수에 추가로 문자열 “추가하고 싶은 내용” 을 붙여서 출력한다

---

## 03. 파이썬 문자열 021 ~ 030

- 022 문자열 슬라이싱

슬라이싱을 사용할 때 시작 인덱스를 생략하면 0으로 간주하고, 끝 인덱스를 생략하면 문자열의 끝까지 출력한다.

```python
number = "24가 2210"
print(number[:3])
print(number[-4:])
```

```
24가
2210
```

- 023 문자열 인덱싱

```
오프셋 : 컴퓨터 과학에서 배열이나 자료 구조 오브젝트 내의 오프셋(offset)은 일반적으로 동일 오브젝트 안에서 오브젝트 처음부터 주어진 요소나 지점까지의 변위차를 나타내는 정수형이다.

이를테면, 문자 A의 배열이 abcdef를 포함한다면 'c' 문자는 A 시작점에서 2의 오프셋을 지닌다고 할 수 있다.
```

출처: https://ko.wikipedia.org/wiki/%EC%98%A4%ED%94%84%EC%85%8B_(%EC%BB%B4%ED%93%A8%ED%84%B0_%EA%B3%BC%ED%95%99)

`example[start:end:stride]`

stride : 보폭

```python
example = "0123456789"
print(example[::2])
print(example[::3])
print(example[::-1])
print(example[::-3])
```

```
02468
0369
9876543210
9630
```

---

- 024 문자열 슬라이싱
  문자열을 역순으로 뒤집어 출력하려면 오프셋 -1로 stride 사용하기

```py
string = "python"
print(string[::-1])
```

`nohtyp`

---

- 025 문자열 치환

string(문자열)은 immutable type([불변객체](https://ko.wikipedia.org/wiki/%EB%B6%88%EB%B3%80%EA%B0%9D%EC%B2%B4))이라 수정할 수 없다.
그래서 string을 바꾸고 싶다면 replace나 list를 이용해야 한다.

replace 메서드 : 일괄적으로 ','왼쪽의 문자열을 오른쪽 문자열로 한번에 변환. `print(변수명.replace("k","L"))`  
list : `cars = ['benz', 'audi', 'bmw']`

---

- 027 문자열 다루기

`변수명2 = 변수명1.split(".")` 사용해서 .을 기준으로 나누고 인덱싱으로 쓸 부분만 print문으로 출력

---

- 028 문자열은 immutable

|                 | 데이터 타입                              |
| --------------- | ---------------------------------------- |
| 가변(mutable)   | list, set, dict                          |
| 불변(immutable) | int, float, bool, tuple, string, unicode |

---

- 030 replace 메서드
  replace 메서드를 사용해서 문자열을 수정하려면 같은 변수명으로 새로 선언을 하던지 새로운 변수명으로 새로 선언을 해야한다.

```python
string = 'abcd'
string.replace('b', 'B')
print(string)
```

`abcd`
