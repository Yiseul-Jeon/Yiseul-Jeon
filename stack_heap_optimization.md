# 📘 함수와 가변 매개함수 기초 정리 노트

---

## ✅ 함수란?

- 코드를 저장해놓고, 필요할 때 불러서 실행하는 도구!

```python
def 함수이름(매개변수):
    실행할 코드들

```

예시:

```python
def say_hello(name):
    print("안녕,", name)

say_hello("슬아")

```

---

## ✅ 매개변수 vs 인자 (parameter vs argument)

| 구분 | 예시 | 설명 |
| --- | --- | --- |
| 매개변수 | name | 함수를 "정의"할 때 사용하는 변수 |
| 인자 | "슬아" | 함수를 "호출"할 때 넣는 실제 값 |

암기법 ✨:

> "함수를 만들 때 괄호 안 = 매개변수!"
"함수를 부를 때 넣는 값 = 인자!"
> 

---

## ✅ 가변 매개변수 `values`

- 몇 개의 값이 들어올지 모를 때 사용하는 매개변수

```python
def print_n_times(n, *values):
    for i in range(n):
        for value in values:
            print(value)
            print()

print_n_times(2, "안녕", "파이썬")

```

결과:

```
안녕
파이썬

안녕
파이썬

```

---

## ✅ 함수 이름 작명 규칙

| 규칙 | 설명 | 예시 |
| --- | --- | --- |
| 영어/숫자/밑줄 사용 가능 | 숫자는 앞에 못 옴 | seul, my_func, print3 ✅ |
| 숫자로 시작 ❌ | 에러남 | 3print ❌ |
| 특수기호 ❌ | -, @, # 안 됨 | say-hi ❌ |
| 띄어쓰기 ❌ | 하나의 단어처럼 | my function ❌ |
| 예약어 ❌ | 이미 쓰이는 파이썬 키워드 | print ❌ |

---

## ✅ 예시 함수

**1. 여러 줄 print()**

```python
def seul():
    print("슬아 함수다아~")
    print("여러 줄도 된다아~")
    print("함수 안에선 뭐든 가능하다아~")

```

**2. for문 사용하기**

```python
def seul():
    for i in range(3):
        print("슬아가 최고야!", i)

```

**3. 다른 함수 안에서 또 함수 부르기**

```python
def hello():
    print("안녕 슬아!")

def seul():
    print("슬아 함수 시작!")
    hello()
    print("슬아 함수 끝~")

```

---