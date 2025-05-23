# [파이썬 f-문자열(f-string) 정리 - p.146 기준]

---

## ✅ f-문자열이란?

- 파이썬 3.6부터 도입된 **문자열 포매팅 방식**
- 문자열 앞에 접두사 **f** 또는 **F**를 붙이고, 문자열 내부에서 **중괄호 `{}`*를 사용하여 변수, 표현식, 함수 등을 직접 삽입할 수 있음

---

## ✅ 문법

```python
변수 = 값
print(f"문자열 {변수}")

```

### 예시

```python
name = "슬"
age = 30
print(f"이름은 {name}, 나이는 {age}살입니다.")

```

🟰 출력: `이름은 슬, 나이는 30살입니다.`

---

## ✅ 왜 사용하는가?

- 코드가 **간결하고 가독성 높음**
- **변수를 문자열 안에 쉽게 포함**할 수 있음
- **계산식, 메서드, 함수 호출 등도 직접 삽입** 가능
- 복잡한 `format()` 함수보다 훨씬 직관적임

---

## ✅ 다양한 예제

### 1. 변수 삽입

```python
name = "슬"
print(f"안녕하세요, {name}님!")

```

### 2. 표현식 삽입

```python
a = 10
b = 20
print(f"{a} + {b} = {a + b}")

```

### 3. 소수점 자리 지정

```python
pi = 3.14159
print(f"원주율은 {pi:.2f}")  # 3.14

```

### 4. 정렬

```python
text = "정렬"
print(f"{text:<10}")  # 왼쪽 정렬
print(f"{text:^10}")  # 가운데 정렬
print(f"{text:>10}")  # 오른쪽 정렬

```

### 5. 천 단위 콤마

```python
money = 1000000
print(f"총 금액은 {money:,}원입니다.")

```

### 6. 딕셔너리/리스트 접근

```python
user = {"name": "슬", "age": 30}
print(f"{user['name']}님의 나이는 {user['age']}살입니다.")

```

### 7. 함수 호출

```python
def greeting():
    return "안녕하세요"

print(f"{greeting()} 슬님!")

```

---

## ✅ 한 줄 요약

> f-문자열은 문자열 안에 {}로 변수를 바로 넣어 출력할 수 있는, 파이썬에서 가장 간단하고 강력한 문자열 포매팅 방식이다!
> 

---

📘 *참고 페이지: 파이썬 교재 p.146*