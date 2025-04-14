# 파이썬 in 문법 정리

---

## ✨ 1. `for i in` vs `if i in` 비교표

| 문법 구문 | 역할 | 예시 | 설명 |
| --- | --- | --- | --- |
| `for i in` | **반복(iteration)** | `for i in range(5):` | 리스트나 튜플 등을 순회하며 반복 실행 |
| `if i in` | **포함 여부 확인(조건식)** | `if i in my_list:` | 어떤 값이 포함돼 있는지 확인 (True/False) |

---

## 🔍 2. `for i in` - 반복문 용도

```python
for i in [1, 2, 3]:
    print(i)

```

- 리스트에서 **하나씩 꺼내서 `i`에 저장**하고, 그걸 반복 실행함.
- `range(5)`는 사실 `[0, 1, 2, 3, 4]`와 동일한 효과.

```python
for fruit in ["🍎", "🍌", "🍇"]:
    print("과일:", fruit)

```

---

## ✅ 3. `if i in` - 포함 여부 조건문

```python
my_list = [1, 2, 3]

if 2 in my_list:
    print("2가 리스트에 있어요!")

```

- 리스트 안에 특정 값이 **존재하는지**를 확인함.
- 결과는 `True` 또는 `False`로 반환됨.

---

## 🌌 4. `i`의 의미는?

- `i`는 그냥 변수 이름일 뿐이야!
- **약속된 건 아니고, 보통 'index' 또는 'iterator'의 약자**로 많이 쓰여서 자연스럽게 그렇게 사용되는 거야.
- 마음대로 바꿔도 돼!

```python
for apple in ["🍎", "🍏"]:
    print(apple)

```

위 코드에서 `i` 대신 `apple`도 가능! 가독성 좋은 이름을 쓰는 게 중요해.

---

## 🎓 5. 실전 예제

```python
students = ["슬이", "진이", "하린", "도원"]

# for in - 반복문
for name in students:
    print("출석:", name)

# if in - 조건문
if "슬이" in students:
    print("슬이 오늘도 개근이네~ 👏")

```

---

## 🤖 6. 한 줄 요약

> for i in → 반복에 사용
> 
> 
> `if i in` → 포함여변 검사에 사용
> 

---