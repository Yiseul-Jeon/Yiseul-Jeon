# IndexError와 예외 처리 정리

### 🔹 IndexError란?

- 리스트, 문자열, 튜플 등 **시퀀스 자료형**에서 **존재하지 않는 인덱스에 접근**하려고 할 때 발생하는 오류.

```python
text = "파이썬"
print(text[5])  # IndexError: string index out of range

```

- 인덱스는 `0`부터 시작하며, 길이를 초과하는 인덱스 접근은 에러 발생.

---

### 🔸 IndexError 방지 방법

1. `len()` 함수로 길이 확인 후 접근

```python
if index < len(text):
    print(text[index])

```

1. 슬라이싱 사용 (`s[0:len(s)]`)은 안전

```python
text[0:100]  # 실제 있는 범위까지만 반환하므로 에러 없음

```

---

### 🔹 예외 처리 (`try ~ except`)

- 프로그램이 중단되지 않도록 예외 발생 시 대처할 수 있는 구조

```python
try:
    print(text[5])
except IndexError:
    print("인덱스 범위를 벗어났습니다.")

```

### 🔸 구조

```python
try:
    # 예외 발생 가능성 있는 코드
except 예외타입:
    # 예외 발생 시 실행할 코드
else:
    # 예외 없을 때 실행
finally:
    # 예외 유무와 관계없이 항상 실행

```

---

### 🎯 실전 예제

```python
def safe_access(seq, index):
    try:
        return seq[index]
    except IndexError:
        return "인덱스 오류: 접근 불가"

print(safe_access("파이썬", 10))

```

---

### ✅ 마무리 요약

| 항목 | 설명 |
| --- | --- |
| IndexError | 존재하지 않는 인덱스에 접근할 때 발생 |
| 예외 처리 | try ~ except 구조로 프로그램 안정성 확보 |
| 방지법 | `len()` 확인, 슬라이싱 사용, 예외 처리 활용 |