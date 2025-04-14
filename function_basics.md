# 리스트(list)와 배열(array)의 차이점 정리

---

### ✅ 리스트(list)와 배열(array) 비교표

| 구분 | 리스트 (`list`) | 배열 (`array`) |
| --- | --- | --- |
| **제공 모듈** | 기본 제공 (내장 타입) | `array` 모듈 또는 `numpy` 등 외부 라이브러리 |
| **자료형 혼합** | 가능 (O) | 불가능 (X), 동일한 자료형만 가능 |
| **용도** | 범용 자료 저장용 | 수치 계산, 대규모 데이터 처리용 |
| **메모리 효율** | 낮음 | 높음 |
| **연산 속도** | 느림 | 빠름 |
| **수학적 연산 지원** | 기본적으로 없음 | `numpy` 사용 시 강력한 연산 지원 |
| **예시** | `mylist = [1, "a", 3.14]` | `array.array('i', [1, 2, 3])` 또는 `np.array([1, 2, 3])` |

---

### ✅ 실무 예제 비교

### 1. 리스트 사용 예제:

```python
my_list = [1, 2, 3, "hello", 5.5]
print(my_list[3])  # hello

```

- 다양한 타입을 섞어서 저장 가능
- 수학 계산에는 적합하지 않음

### 2. 배열(array 모듈) 사용 예제:

```python
import array
a = array.array('i', [1, 2, 3, 4])
print(a[2])  # 3

```

- 모든 요소가 정수형 `'i'`
- 빠르고 효율적인 메모리 사용 가능

### 3. 넘파이(numpy) 배열 예제:

```python
import numpy as np
arr = np.array([1, 2, 3])
print(arr + 10)  # [11 12 13]

```

- 벡터 연산, 행렬 연산 등 고속 연산 지원

---

### 🎯 핵심 요약

- **리스트**: 자유로운 자료형 혼합, 일반적 데이터 저장에 적합
- **배열**: 동일 자료형, 빠르고 효율적인 계산 처리에 적합 (특히 `numpy`)

---

### 📘 리스트 실습 코드 설명

```python
# 리스트 선언
list_a = [1, 2, 3]

# 리스트 뒤에 요소 추가
print("#리스트 뒤에 요소 추가")
list_a.append(4)
list_a.append(5)
print(list_a)
print()

# 리스트 중간에 요소 추가
print("리스트 중간에 요소 추가")
list_a.insert(0, 10)
print(list_a)

```

### ✅ 한 줄씩 설명

- `list_a = [1, 2, 3]` : 숫자 1, 2, 3을 가진 리스트 생성
- `list_a.append(4)` : 리스트의 **맨 뒤에** 4 추가 → `[1, 2, 3, 4]`
- `list_a.append(5)` : 다시 5 추가 → `[1, 2, 3, 4, 5]`
- `list_a.insert(0, 10)` : 0번째 위치(맨 앞)에 10 삽입 → `[10, 1, 2, 3, 4, 5]`

### 🔍 변화 시각화

| 단계 | 리스트 내용 |
| --- | --- |
| 초기 | `[1, 2, 3]` |
| append(4) | `[1, 2, 3, 4]` |
| append(5) | `[1, 2, 3, 4, 5]` |
| insert(0, 10) | `[10, 1, 2, 3, 4, 5]` |

### 💡 추가 팁

- 리스트는 **순서가 있는 데이터 집합**이야.
- 인덱스(번호)를 통해 원하는 요소에 접근 가능해. 예: `list_a[2]`는 2번째 요소인 `2`
- 자료형이 달라도 한 리스트에 넣을 수 있어: `[1, "hello", 3.14]`

---

### 🧹 리스트 삭제 시 주의점

### ❌ 앞에서부터 삭제하면 문제 생겨요!

```python
my_list = [10, 20, 30, 40, 50]
for i in range(len(my_list)):
    del my_list[i]  # ❌ IndexError 또는 값 누락 발생

```

### ✅ 뒤에서부터 삭제하면 안전!

```python
my_list = [10, 20, 30, 40, 50]
for i in range(len(my_list)-1, -1, -1):
    del my_list[i]

```

- 인덱스가 밀리지 않아서 안전하게 삭제 가능

---

### 📦 리스트 요소 삭제: pop()

### 기본 사용법

```python
my_list = [10, 20, 30]
val = my_list.pop()
print(val)        # 30
print(my_list)    # [10, 20]

```

- 마지막 요소를 꺼내서 반환하고 삭제함

### 인덱스를 지정하여 꺼내기

```python
my_list = [10, 20, 30, 40]
val = my_list.pop(1)
print(val)        # 20
print(my_list)    # [10, 30, 40]

```

### 빈 리스트에서 pop()?

```python
empty_list = []
empty_list.pop()  # ❌ IndexError 발생

```

### 안전하게 pop 쓰기

```python
if my_list:
    my_list.pop()

```

### 스택(Stack) 구현 예시

```python
stack = []
stack.append(1)
stack.append(2)
stack.append(3)

print(stack.pop())  # 3
print(stack.pop())  # 2
print(stack)        # [1]

```

---

### 📊 pop(), remove(), del 비교표

| 메서드 | 기준 | 반환값 | 설명 |
| --- | --- | --- | --- |
| `pop()` | 인덱스 | O | 지정한 위치에서 꺼내 삭제 |
| `remove()` | 값 | X | 첫 번째로 나오는 값을 삭제 |
| `del` | 인덱스 | X | 특정 인덱스 삭제 (반환 없음) |

---

### 🎯 한 줄 요약!

> pop()은 꺼내고, remove()는 찾아서 지우고, del은 바로 날려버림!
>