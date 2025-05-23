# ⚠️ 파이썬 return의 들여쓰기 주의점

## 📌 핵심 개념

파이썬에서는 **들여쓰기(Indentation)** 로 코드의 영역(범위)를 구분한다.
함수나 반복문 내부에서 `return`이 어디 위치하느냐에 따라 **함수 동작이 완전히 달라진다!**

---

## ❌ 잘못된 예시 (오류 발생 or 예상치 못한 결과)

```python
def sum_all(start=0, end=100, step=1):
    output = 0
    for i in range(start, end + 1, step):
        output += i
        return output  # ❗ 잘못된 들여쓰기 → 반복 한 번만 돌고 끝남

```

### ➤ 문제점:

- `return output`이 `for문 안`에 있어
- 반복문이 **단 한 번만 실행되고** 바로 함수 종료

## ✅ 올바른 예시 (정상 동작)

```python
def sum_all(start=0, end=100, step=1):
    output = 0
    for i in range(start, end + 1, step):
        output += i
    return output  # ✅ for문이 끝난 후 결과를 돌려줌

```

## 🔍 왜 이런 차이가 생길까?

| 위치 | 의미 |
| --- | --- |
| `for` 안쪽 들여쓰기 | 반복할 때마다 실행됨 |
| `for` 밖 들여쓰기 | 반복문이 끝난 후 한 번 실행 |

## 📘 실습 예시 출력 비교

```python
print(sum_all(0, 100, 10))

```

- 잘못된 버전: `0`만 출력됨
- 올바른 버전: `550` 출력됨 (0 + 10 + ... + 100)

## ✅ 정리 요약

- `return`은 **반복문(for, while)** 또는 조건문(if) 블록이 끝나고 써야 전체 흐름을 마무리 가능
- 들여쓰기가 하나라도 다르면 **파이썬은 다른 코드 블록**으로 인식함

---

💡 **실전 꿀팁**

> return은 마치 "계산 결과를 밖에 전달하는 택배" 같아.
> 
> 
> 아직 계산 중인데 중간에 문 닫아버리면 배송 안 가! 반드시 다 끝낸 뒤에 보내야 해. 🚚📦
> 

📚 관련 예제: 『혼자 공부하는 파이썬』 287~288쪽