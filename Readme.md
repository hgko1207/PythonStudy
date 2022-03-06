# Python 공부

## 환경설정

### Python 설치

- https://www.python.org/downloads/ 홈페이지 접속 후 다운로드 탭을 선택하고, 현재 버전(3.10.2) 다운로드를 합니다.
- 다운로드 완료 후 설치를 시작합니다. **Customize installation** 클릭하고, **install location** 란에 `c:\Python310` 입력 후 설치 버튼을 클릭합니다.

### Visual Studio Code 설치

https://code.visualstudio.com/ 홈페이지 접속 후 다운로드 후 설치합니다.

- python 익스텐션 설치

## 기본 시작

파이썬 기본 중에 쓰임이 있는 부분만 정리하였습니다.

### 주석

```py
print("주석")
#print("주석")

'''
여러문장
주석입니다.
'''
```

### 숫자처리함수

```py
print(abs(-5)) #5
print(pow(4, 2)) # 4^2 = 4*4 = 16
print(max(5, 12)) # 12
print(min(5, 12)) # 5
print(round(3.14)) # 3

from math import *
print(floor(4.99)) # 내림. 4
print(ceil(3.14)) # 올림. 4
print(sqrt(16)) # 제곱근. 4
```

### 랜덤함수

```py
from random import *

print(random()) # 0.0 ~ 1.0 미만의 임의의 값 생성
print(random(10)) # 0.0 ~ 10.0 미만의 임의의 값 생성
print(int(random() * 10)) # 0 ~ 10 미만의 임의의 값 생성
print(int(random() * 10) + 1) # 1 ~ 10 이하의 임의의 값 생성
print(int(random() * 45) + 1) # 1 ~ 45 이하의 임의의 값 생성
print(randrange(1, 46)) # 1 ~ 46 미만의 임의의 값 생성
print(randint(1, 45)) # 1 ~ 45 이하의 임의의 값 생성
```

### 문자열

```py
sentence = '나는 소년입니다'
print(sentence)
sentence2 = "파이썬은 쉬워요"
print(sentence2)
sentence3 = """
나는 소년이고,
파이썬은 쉬워요
"""
print(sentence3)
```

### 슬라이싱

```py
jumin = "990101-1234567"

print("성별 : " + jumin[7])
print("연 : " + jumin[0:2]) # 0 부터 2 직전까지 (0, 1)
print("월 : " + jumin[2:4])
print("일 : " + jumin[4:6])

print("생년월일 : " + jumin[:6]) # 처음부터 6 직전까지
print("뒤 7자리 : " + jumin[7:]) # 7 부터 끝까지
print("뒤 7자리 (뒤에부터) : " + jumin[-7:])
# 맨 뒤에서 7번째부터 끝까지
```
