# Python 공부

나도코딩(https://www.youtube.com/channel/UC7iAOLiALt2rtMVAWWl4pnw)님의 파이썬 코딩 무료 강의(기본편)을 보면서 작성하였습니다.

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

### 문자열 처리 함수

```py
python = "Python is Amazing"
print(python.lower()) # 소문자로
print(python.upper()) # 대문자로
print(python[0].isupper())
print(len(python)) # 길이
print(python.replace("Python", "Java")) # 문자열 바꿈

index = python.index("n") # 문자열 위치 찾기
index = python.index("n", index + 1) # 두번째 n의 위치 찾기

print(python.find("Java")) # 문자를 찾지 못할 경우 -1 출력
print(python.index("Java")) # 문자를 찾지 못할 경우 오류남

print(python.count("n")) # 문자열 n이 나오는 개수
```

### 문자열 포맷

```py
# 방법 1
print("나는 %d살입니다." % 35) # 정수만
print("나는 %s을 좋아해요" % "파이썬") # 문자열만
print("Apple 은 %c로 시작해요." % "A") # 한글자만 받겠다는 의미
# %s
print("나는 %s살입니다." % 35)
print("나는 %s색과 %s색을 좋아해요." % ("파란", "빨간"))

# 방법 2
print("나는 {}살입니다.".format(35))
print("나는 {}색과 {}색을 좋아해요.".format("파란", "빨간"))
print("나는 {0}색과 {1}색을 좋아해요.".format("파란", "빨간"))
print("나는 {1}색과 {0}색을 좋아해요.".format("파란", "빨간"))

# 방법 3
print("나는 {age}살이며, {color}색을 좋아해요.".format(age=35, color="빨간"))

# 방법 4 (v3.6 이상~)
age = 35
color = "빨간"
print(f"나는 {age}살이며, {color}색을 좋아해요.")
```

### 탈출 문자

```py
# \n : 줄바꿈
print("백문이 불여일견\n백견이 불여일타")

# \" \' : 문장 내에서 따옴표
# 저는 "고고고" 입니다.
print("저는 '고고고' 입니다.")
print('저는 "고고고" 입니다.')
print("저는 \"고고고\" 입니다.")

# \\ : 문장 내에서 \
print("C:\\Users\\hgko\\Desktop\\project\\Python\\PythonStudy")

# \r : 커서를 맨 앞으로 이동
print("Red Apple\rPine")

# \b : 백스페이스 (한 글자 삭제)
print("Redd\bApple")

# \t : 탭
print("Red\tApple")
```

### 리스트

```py
# 리스트 []

# 지하철 칸별로 10명, 20명, 30명
subway1 = 10
subway2 = 20
subway3 = 30

subway = [10, 20, 30]
print(subway)

subway = ["유재석", "조세호", "박명수"]

# 조세호 씨가 몇 번째 칸에 타고 있는지?
print(subway.index("조세호"))

# 하하 씨가 다음 정류장에서 다음 칸에 탐
subway.append("하하")

# 정형돈 씨를 유재석 / 조세호 사이에 태워봄
subway.insert(1, "정형돈")

# 지하철에 있는 사람을 한 명 씩 뒤에서 꺼냄
print(subway.pop())

# 같은 이름의 사람이 몇 명 있는지 확인
subway.append("유재석")
print(subway.count("유재석"))

# 정렬
num_list = [5,2,4,3,1]
num_list.sort()

# 순서 뒤집기
num_list.reverse()

# 모두 지우기
num_list.clear()

# 다양한 자료형 함께 사용
num_list = [5,2,4,3,1]
mix_list = ["유재석", 20, True]

# 리스트 확장
num_list.extend(mix_list)
```

### 사전

```py
cabinet = {3:"유재석", 100:"김태호"}
print(cabinet[3])
print(cabinet[100])

print(cabinet.get(3))
print(cabinet.get(5, "사용 가능"))

print(3 in cabinet) # True
print(5 in cabinet) # False

cabinet = {"A-3":"유재석", "B-100":"김태호"}
print(cabinet["A-3"])
print(cabinet["B-100"])

# 새 손님
cabinet["A-3"] = "김종국" # 업데이트
cabinet["C-20"] = "조세호" # 추가

# 간 손님
del cabinet["A-3"]

# key 들만 출력
print(cabinet.keys())

# value 들만 출력
print(cabinet.values())

# key, value 쌍으로 출력
print(cabinet.items())

# 전체 삭제
cabinet.clear()
```

### 튜플

```py
menu = ("돈까스", "치즈까스")

(name, age, hobby) = ("김종국", 20, "코딩")
print(name, age, hobby)
```

### 세트

```py
# 집합 (set)
# 중복 안됨, 순서 없음
my_set = {1,2,3,3,3}
print(my_set)

java = {"유재석", "김태호", "양세형"}
python = set(["유재석", "박명수"])

# 교집합 (java 와 python 을 모두 할 수 있는 개발자)
print(java & python)
print(java.intersection(python))

# 합집합 (java 할 수 있거나 python 도 할 수 있는 개발자)
print(java | python)
print(java.union(python))

# 차집합 (java 할 수 있지만 python 은 할 줄 모르는 개발자)
print(java - python)
print(java.difference(python))

# python 할 줄 아는 사람이 늘어남
python.add("김태호")

# java 를 잊어버림
java.remove("김태호")
```

### 자료구조의 변경

```py
# 커피숍
menu = {"커피", "우유", "주소"}
print(menu, type(menu)) # {'커피', '주소', '우유'} <class 'set'>

menu = list(menu)
print(menu, type(menu)) # ['커피', '주소', '우유'] <class 'list'>

menu = tuple(menu)
print(menu, type(menu)) # ['커피', '주소', '우유'] <class 'tuple'>

menu = set(menu)
print(menu, type(menu)) # ['커피', '주소', '우유'] <class 'set'>
```

### if

```py
weather = input("오늘 날씨는 어때요?")
if weather == "비" or weather == "눈":
    print("우산을 챙기세요")
elif weather == "미세먼지":
    print("마스크를 챙기세요")
else:
    print("준비물 필요 없어요")

temp = int(input("기운은 어때요?"))
if 30 <= temp:
    print("너무 더워요. 나가지 마세요")
elif 10 <= temp and temp < 30:
    print("괜찮은 날씨에요")
elif 0 <= temp < 10:
    print("외투를 챙기세요")
else:
    print("너무 추워요. 나가지 마세요")
```

### for

```py
# randrange()
for waiting_no in range(1, 6): # 1, 2, 3, 4, 5
    print("대기번호 : {0}".format(waiting_no))
```

### while

```py
customer = "토르"
person = "Unknown"
while person != customer:
    print("{0}, 커피가 준비 되었습니다.".format(customer))
    person = input("이름이 어떻게 되세요?")

```

### 한 줄 for

```py
students = [1,2,3,4,5]
students = [i+100 for i in students]

# 학생 이름을 길이도 반환
students = ["Iron man", "Thor", "I am groot"]
students = [len(i) for i in students]
```

### 함수

```py
def open_account():
    print("새로운 계좌가 생성되었습니다.")

def deposit(balance, money): # 입금
    print("입금이 완료되었습니다. 잔액은 {0} 원입니다.".format(balance + money))
    return balance + money

def withdraw(balance, money): # 출금
    if balance >= money: # 잔액이 출금보다 많으면
        print("출금이 완료되었습니다. 잔액은 {0} 원입니다.".format(balance - money))
        return balance - money
    else:
        print("출금이 완료되지 않았습니다. 잔액은 {0} 원입니다.".format(balance))
        return balance

def withdraw_night(balance, money): # 저녁에 출금
    commission = 100 # 수수료 100원
    return commission, balance - money - commission

balance = 0
balance = deposit(balance, 1000)
# balance = withdraw(balance, 500)
commission, balance = withdraw_night(balance, 500)
print("수수료 {0} 원이며, 잔액은 {1} 원입니다.".format(commission, balance))
```

### 함수 기본값

```py
def profile(name, age, main_lang):
    print("이름 : {0}\t나이 : {1}\t주 사용언어 : {2}".format(name, age, main_lang))

profile("고형균", 35, "파이썬")

# 같은 학교 같은 학년 같은 반 같은 수업
def profile(name, age=17, main_lang="파이썬"):
    print("이름 : {0}\t나이 : {1}\t주 사용언어 : {2}".format(name, age, main_lang))

profile("고형균")
```

### 가변인자

```py
# def profile(name, age, lang1, lang2, lang3, lang4, lang5):
#     print("이름 : {0}\t나이 : {1}\t".format(name, age), end=" ")
#     print(lang1, lang2, lang3, lang4, lang5)

def profile(name, age, *language):
    print("이름 : {0}\t나이 : {1}\t".format(name, age), end=" ")
    for lang in language:
        print(lang, end=" ")
    print()

profile("고형균", 35, "Python", "Java", "C", "C++", "C#", "JavaScript")
profile("김태호", 40, "Kotlin", "Swift", "", "", "")
```

### 지역변수와 전역변수

```py
gun = 10

def checkpoint(soldiers): # 경계근무
    global gun # 전역 공간에 있는 gun 사용
    gun = gun - soldiers
    print("[함수 내] 남은 총 : {0}".format(gun))

def checkpoint_ret(gun, soldiers):
    gun = gun - soldiers
    print("[함수 내] 남은 총 : {0}".format(gun))
    return gun

print("전체 총 : {0}".format(gun))
#checkpoint(2) # 2명이 경계 근무 나감
gun = checkpoint_ret(gun, 2)
print("남은 총 : {0}".format(gun))
```

### 표준 입출력

```py
import sys
print("Python", "Java", file=sys.stdout)
print("Python", "Java", file=sys.stderr)

# 시험 성적
scores = {"수학":0, "영어":50, "코딩":100}
for subject, score in scores.items():
    #print(subject, score)
    print(subject.ljust(8), str(score).rjust(4), sep=":")

# 은행 대기순번표
# 001, 002, 003, ...
for num in range(1, 21):
    print("대기번호 : " + str(num).zfill(3))
```

### 다양한 출력포맷

```py
# 빈 자리는 빈공간으로 두고, 오른쪽 정렬을 하되, 총 10자리 공간을 확보
print("{0: >10}".format(500))
# 양수일 땐 +로 표시, 음수일 땐 -로 표시
print("{0: >+10}".format(500))
print("{0: >+10}".format(-500))
# 왼쪽 정렬하고, 빈칸으로 _로 채움
print("{0:_<+10}".format(500))
# 3자리 마다 콤마를 찍어주기
print("{0:,}".format(1000000000))
# 3자리 마다 콤마를 찍어주기, +- 부호도 붙이기
print("{0:+,}".format(1000000000))
# 3자리 마다 콤마를 찍어주기, +- 부호도 붙이고, 자릿수 확보하기
# 돈이 많으면 행복해지니까 빈 자리는 ^ 로 채워주기
print("{0:^<+30,}".format(1000000000))
# 소수점 출력
print("{0:f}".format(5/3))
# 소수점 특정 자리수 까지만 표시 (소수점 3째 자리에서 반올림)
print("{0:.2f}".format(5/3))
```

### 파일 입출력

```py
score_file = open("score.txt", "w", encoding="utf8") # write
print("수학 : 0", file=score_file)
print("영어 : 50", file=score_file)
score_file.close()

score_file = open("score.txt", "a", encoding="utf8") # update
score_file.write("과학 : 80")
score_file.write("\n코딩 : 100")
score_file.close()

score_file = open("score.txt", "r", encoding="utf8") # read
print(score_file.read())
score_file.close()

score_file = open("score.txt", "r", encoding="utf8")
print(score_file.readline(), end="") # 줄별로 읽기, 한 줄 읽고 커서는 다음 줄로 이동
print(score_file.readline(), end="")
print(score_file.readline(), end="")
print(score_file.readline(), end="")
score_file.close()

score_file = open("score.txt", "r", encoding="utf8")
while True:
    line = score_file.readline()
    if not line:
        break
    print(line, end="")
score_file.close()

score_file = open("score.txt", "r", encoding="utf8")
lines = score_file.readlines() # list 형태로 저장
for line in lines:
    print(line, end="")
score_file.close()
```

### pickle

```py
import pickle
profile_file = open("profile.pickle", "wb") # b: 바이너리
profile = {"이름":"고형균", "나이":36, "취미":["축구", "볼링", "코딩"]}
print(profile)
pickle.dump(profile, profile_file) # profile 에 있는 정보를 file 에 저장
profile_file.close()

profile_file = open("profile.pickle", "rb")
profile = pickle.load(profile_file) # file 에 있는 정보를 profile 에 불러오기
print(profile)
profile_file.close()
```

### with

```py
# import pickle

# with open("profile.pickle", "rb") as profile_file:
#     print(pickle.load(profile_file))

with open("study.txt", "w", encoding="utf8") as study_file:
    study_file.write("파이썬을 열심히 공부하고 있어요")

with open("study.txt", "r", encoding="utf8") as study_file:
    print(study_file.read())
```

### 클래스

```py
class Unit:
    def __init__(self, name, hp, damage):
        self.name = name
        self.hp = hp
        self.damage = damage
        print("{0} 유닛이 생성되었습니다.".format(self.name))
        print("체력 {0}, 공격력 {1}\n".format(self.hp, self.damage))

marine1 = Unit("마린", 40, 5)
marine2 = Unit("마린", 40, 5)
tank = Unit("탱크", 150, 35)
```

### 메소드

```py
class AttackUnit:
    def __init__(self, name, hp, damage):
        self.name = name
        self.hp = hp
        self.damage = damage

    def attack(self, location):
        print("{0} : {1} 방향으로 적군을 공격합니다. [공격력 {2}]".format(self.name, location, self.damage))

    def damaged(self, damage):
        print("{0} : {1} 데미지를 입었습니다.".format(self.name, damage))
        self.hp -= damage
        print("{0} : 현재 체력은 {1} 입니다.".format(self.name, self.hp))
        if self.hp <= 0:
            print("{0} : 파괴되었습니다.".format(self.name))

firebat1 = AttackUnit("파이어뱃", 50, 16)
firebat1.attack("5시")

# 공격 2번 받는다고 가정
firebat1.damaged(25)
firebat1.damaged(25)
```

### 상속

```py
class Unit:
    def __init__(self, name, hp):
        self.name = name
        self.hp = hp

class AttackUnit(Unit):
    def __init__(self, name, hp, damage):
        Unit.__init__(self, name, hp)
        self.damage = damage
```

### 다중 상속

```py
# 날 수 있는 기능을 가진 클래스
class Flyable:
    def __init__(self, flying_speed):
        self.flying_speed = flying_speed

    def fly(self, name, location):
        print("{0} : {1} 방향으로 날아갑니다. [속도 {2}]".format(name, location, self.flying_speed))

# 공중 공격 유닛 클래스
class FlyableAttackUnit(AttackUnit, Flyable):
    def __init__(self, name, hp, damage, flying_speed):
        AttackUnit.__init__(self, name, hp, damage)
        Flyable.__init__(self, flying_speed)

# 발키리 : 공중 공격 유닛, 한번에 14발 미사일 발사.
valkrie = FlyableAttackUnit("발키리", 200, 6, 5)
valkrie.fly(valkrie.name, "3시");
```

### 메소드 오버라이딩

```py
class FlyableAttackUnit(AttackUnit, Flyable):
    def __init__(self, name, hp, damage, flying_speed):
        AttackUnit.__init__(self, name, hp, 0, damage)
        Flyable.__init__(self, flying_speed)

    def move(self, location):
        self.fly(self.name, location) # <= 메소드 오버라이딩
```

### pass

```py
def game_start():
    print("[알림] 새로운 게임을 시작합니다.")

def game_over():
    pass

game_start()
game_over()
```

### super

```py
class BuildingUnit(Unit):
    def __init__(self, name, hp, location):
        #Unit.__init__(self, name, hp, 0)
        super().__init__(name, hp, 0)
        self.location = location
```

### 예외처리

```py
try:
    print("나누기 전용 계산기입니다.")
    nums = []
    nums.append(int(input("첫 번째 숫자를 입력하세요 : ")))
    nums.append(int(input("두 번째 숫자를 입력하세요 : ")))
    nums.append(int(nums[0] / nums[1]))
    print("{0} / {1} = {2}".format(nums[0], nums[1], nums[2]))
except ValueError:
    print("에러! 잘못된 값을 입력하였습니다.")
except ZeroDivisionError as err:
    print(err)
except Exception as err:
    print("알 수 없는 에러가 발생하였습니다.")
    print(err)
```

### 예외 발생시키기

```py
class BigNumberError(Exception):
    def __init__(self, msg):
        self.msg = msg

    def __str__(self):
        return self.msg

try:
    print("한 자리 숫자 나누기 전용 계산기입니다.")
    num1 = int(input("첫 번째 숫자를 입력하세요 : "))
    num2 = int(input("두 번째 숫자를 입력하세요 : "))
    if num1 >= 10 or num2 >= 10:
        raise BigNumberError("입력값 : {0}, {1}".format(num1, num2))
    print("{0} / {1} = {2}".format(num1, num2, int(num1 / num2)))
except ValueError:
    print("잘못된 값을 입력하였습니다. 한 자리 숫자만 입력하세요.")
except BigNumberError as err:
    print("에러가 발생하였습니다. 한 자리 숫자만 입력하세요.")
    print(err)
```

### 모듈

모듈을 사용하기 위해 `theater_module.py` 파일을 생성한다.

```py
# 일반 가격
def price(people):
    print("{0}명 가격은 {1}원 입니다.".format(people, people * 10000))

# 조조 할인 가격
def price_morning(people):
    print("{0}명 조조 할인 가격은 {1}원 입니다.".format(people, people * 6000))

# 군인 할인 가격
def price_soldier(people):
    print("{0}명 군인 할인 가격은 {1}원 입니다.".format(people, people * 4000))
```

생성한 모듈을 사용하기 위한 5가지 방법이다.

```py
# 1) 기본
import theater_module
theater_module.price(3) # 3명이서 영화 보러 갔을 때 가격
theater_module.price_morning(4) # 4명이서 조조 할인 영화 보러 갔을 때
theater_module.price_soldier(5) # 5명의 군인이 영화 보러 갔을 때

# 2) 별칭 사용
import theater_module as mv
mv.price(3)
mv.price_morning(4)
mv.price_soldier(5)

# 3) 전체 사용
from theater_module import *
price(3)
price_morning(4)
price_soldier(5)

# 4) 특정한 함수 사용
from theater_module import price, price_morning
price(5)
price_morning(6)

# 5) 함수에 별칭 사용
from theater_module import price_soldier as price
price(5)
```

### **all**

```py
__all__ = ["vietnam"]
```

### 모듈 직접 실행

```py
class ThailandPackage:
    def detail(self):
        print("[태국 패키지 3박 5일] 방콕, 파타야 여행 (야시장 투어) 50만원")

if __name__ == "__main__":
    print("Thailand 모듈을 직접 실행")
    print("이 문장은 모듈을 직접 실행할 때만 실행돼요")
    trip_to = ThailandPackage()
    trip_to.detail()
else:
    print("Thailand 외부에서 모듈 호출")
```

### 패키지, 모듈 위치

```py
import inspect
import random
print(inspect.getfile(random))
```

### pip install

https://pypi.org/search/

- `pip install beautifulsoup4`
- `pip list`
- `pip show beautifulsoup4`
- `pip install --upgrade beautifulsoup4`
- `pip uninstall beautifulsoup4`
