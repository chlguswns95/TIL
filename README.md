# git

> 분산 버전 관리 시스템 (DVCS, Distributed Version Control System)

윈도우 환경에서는 git 설치 및 실행을 위해 git bash를 다운로드 받는다.

## 기본 명령어

### 저장소(repository) 생성

```bash
$ git init
```

* `.git` 폴더가 숨김 폴더로 생성되고, git bash에서는 `(master)` 라고 표기 된다.
  * 저장소 생성시 상위 폴더에 `.git` 저장소가 있지 않은지 확인할 필요가 있다.
    * 예) 바탕화면에 실수로 `git init` 에서 `.git` 이 있는 경우

### 기본 버전 관리 흐름

* git은 저장소 내에 모든 파일의 변경사항을 추적함
* 작업을 완료하고 `add` -> `commit` 을 통해 버전을 기록한다.
  * `working directory` 에서 `add` 명령어를 통해 `staging area` 상태(`staged`)로
  * `staged` 상태인 파일들을 모두 `commit` 명령어를 통해 버전 기록

#### `add`

> `working directory` 에서 `add` 명령어를 통해 `staging area` 상태(`staged`)로
>
> 버전으로 기록할 파일을 모으기 위해 사용

```bash
$ git add a.txt    # 특정 파일
$ git add test/    # 특정 폴더
$ git add .        # 현재 디렉토리 (하위 디렉토리 포함)
```

#### `commit` 

> `staged` 상태인 파일들을 모두 `commit` 명령어를 통해 **버전 기록**

```bash
$ git commit -m '커밋 메시지'
[master ce0578b] 커밋 메시지
 1 file changed, 1 deletion(-)
 delete mode 100644 a.txt
```

* 커밋 메시지는 현재 버전에 대해 알 수 있도록 작성
* 지금까지 커밋을 확인하기 위해서는 `git log` 명령어 사용

### 상태 확인 

#### `status`

> working directory와 staging area의 상태를 확인할 수 있다. 
>
> 특정 파일이 변경되었는지 (추가/수정/삭제), `staged` 상태인지

```bash
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   b.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        c.txt
```

#### `log`

> 커밋 로그를 확인

```bash
$ git log 
$ git log --oneline # 한줄로 간략히 표기
$ git log -2 # 최근 n개의 로그만 확인
$ git log --oneline -2 # 한줄로 최근 n개만
```

--

### 무엇을 저장하는가

- 현실세계에 존재하는 모든 글자
- 따옴표('') 로 둘러싼 글자와 숫자
- 58 (숫자) vs '58'     (글자 / 문자열)
- 참 / 거짓 , True /     Falsehttps://github.com/JaeYeopHan/Interview_Question_for_Beginnerhttps://github.com/JaeYeopHan/Interview_Question_for_Beginner

 

- 숫자 -> int     (정수), float (실수), complex (복소수)
- 글자 ->     String (문자열)
- 참 / 거짓 ->     boolean (True / False)



### 어떻게 저장하는가

- dust = 60     // 변수
- 숫자는 0 부터 카운트

 

- dust =     [58, 40, 70] // 리스트(인덱스 접근)

  print(dust[1]) // 40

 

- location =     {'영등포구' : 58, '강남구' : 40 } // 딕셔너리 (키 접근)

  print(dust['영등포구']) // 58



### 조건문

- if / else

 

​	if dust > 50:

​	print('50초과')

​	else:

​	print('50이하')

 

- if / elif /else

 

​	if dust > 150:

​	print('매우나쁨')

​	elif 조건:

​	print('나쁨')

​	elif 조건:

​	print('보통')

​	else:

​	print('좋음')



### 반복문

- while // 종료조건 필요

 

​	dust = [59, 24, 102, 45, 64]

​	n = 0

​	while n < 3:

​	print('dust[n]')

​	n = n + 1

 

- for // 종료조건 불필요

 

​	dust = [59, 24, 102, 45, 64]

​	for i in range(3): //

​	print('정해진 범위에서 계속')

 

​	lunch_box = ['햄버거', '피자', '치킨']

​	for lunch in lunch_box:

​	print(lunch)

 

​	for i in range(len(lunch_box)):

​	print(lunch_box[i])

 

- range

 

​	\# range(5)

​	# 숫자가 0 부터 4 까지

​	print(range(5))

​	print(list(range(5)))

​	print(range(0, 5))

 

### 함수기초

함수는 재사용성을 높이기 위함 (인풋->아웃풋)

 

- def calc(a, b):

  print(3 * a + b)

 

​	calc(3, 4)

​	calc(4, 5)



### 모듈(Module)

모듈은 함수의 집합체(종합선물세트)

 

- 함수가 포함된 코드를 불러옴 (import)

 

​	random.choice(리스트)

​	ex) random.choice(menu)

 

​	random.sample(리스트, 개수)

 

​	\# 변수명이 lunch_box 인 리스트를 만들어주세요

​	# 점심메뉴 3개 이상, 초밥 냉면 떡볶이

​	lunch_box = ['연어초밥', '회냉면', '라볶이']

​	print(lunch_box)

 

​	# 1. random (모듈을 가져옴)

​	import random

​	# 2. lunch_box 에서 하나를 선택, menu 변수에 저장

​	menu = random.choice(lunch_box)

​	# 3. menu 변수를 출력

​	print(menu)

\--

​	numbers = range(1, 46)

​	random.sample(numbers, 6) // 여러가지 출력

\--

​	# 1. 필요한 모듈을 불러오세요.

​	import random

​	# 2. 1~45까지 숫자를 numbers에 저장하세요.

​	numbers = range(1, 46)

​	\# 3. numbers 중에 6개의 숫자를 뽑아 lucky에 저장하세요.

​	lucky = random.sample(numbers, 6)

​	# 4. lucky를 출력하세요.

​	print(lucky)

​	print(sorted(lucky)) // 정렬