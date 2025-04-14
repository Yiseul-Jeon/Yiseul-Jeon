# 🌀 while 반복문 완전 정복

### ✅ while 반복문이란?

- while문은 **조건이 참(True)**일 동안 계속 반복 실행되는 문법이다.
- 반복 **횟수가 정해져 있지 않을 때** 많이 사용한다. 예: 사용자 입력, 서버 대기 등

### ✅ 기본 구조

```python
while 조건식:
    실행할 문장

```

### ✅ 예제 1: 1부터 5까지 출력

```python
i = 1
while i <= 5:
    print(i)
    i += 1

```

📌 결과:

```
1
2
3
4
5

```

---

### ✅ 실무 활용 예제 모음

| 예제명 | 코드 요약 | 설명 |
| --- | --- | --- |
| 사용자 입력 반복 | `input()`과 `while` | 사용자가 `exit` 입력할 때까지 계속 묻기 |
| 비밀번호 입력 제한 | 시도횟수 제한 | 비밀번호 맞추기 최대 3번까지 |
| 무한 루프 + 조건 종료 | `break` | 무한 반복 도중 조건 맞으면 탈출 |

### 💡 예제 2: 사용자 입력이 `exit`일 때까지 반복

```python
while True:
    msg = input("입력하세요 (exit 입력 시 종료): ")
    if msg == "exit":
        print("종료합니다.")
        break
    print("입력한 내용:", msg)

```

### 💡 예제 3: 비밀번호 맞추기 (최대 3회 시도)

```python
password = "python123"
attempt = 0

while attempt < 3:
    pw = input("비밀번호 입력: ")
    if pw == password:
        print("접속 성공!")
        break
    else:
        print("틀렸습니다.")
    attempt += 1
else:
    print("3회 실패. 계정 잠김.")

```

---

### ⚠️ 무한 루프 주의

```python
while True:
    print("무한 반복중... 멈출 수 없어!")

```

🛑 Ctrl + C 눌러야 멈춘다. 조심!

---

## 🔁 while문 vs for문 비교표

| 항목 | while문 | for문 |
| --- | --- | --- |
| 🔁 반복 조건 | 조건이 참일 동안 | 반복 가능한 범위나 객체 순회 |
| 🧠 제어 방식 | 조건 기반 | 횟수 기반 |
| ⏱ 적합한 상황 | 무한 루프, 사용자 입력 등 | 리스트, 범위 등 반복 가능한 객체 |
| 💥 무한 루프 | 가능 (while True) | 일반적으로는 어려움 |
| 🧹 초기값/증감 | 직접 설정 필요 | 자동 처리 (`range()`) |
| 🔧 사용 예시 | 게임 루프, 서버 체크 | 리스트 출력, 카운트 반복 등 |

---

### 🎯 실전 상황별 추천

| 상황 | 추천 반복문 |
| --- | --- |
| 사용자 입력에 따라 반복 | ✅ while |
| 1~100까지 출력 | ✅ for |
| 리스트 순회 | ✅ for |
| 정답 맞힐 때까지 반복 | ✅ while |

---

### 🎓 연습문제 예시

```python
# for문 - 리스트 출력
nums = [10, 20, 30]
for n in nums:
    print(n)

# while문 - 정답 맞힐 때까지
answer = "파이썬"
while True:
    guess = input("정답은? ")
    if guess == answer:
        print("정답입니다!")
        break

```

---