# Chapter 02 파이썬 프로그래밍의 기초, 자료형
*****
## 02-1 숫자형
+ 정수형
  - 정수(integer)를 뜻하는 자료형
  ```python
  a = 123
  a = -178
  a = 0
  ```
+ 실수형
  - 실수형(floating-point), 소수점이 포함된 숫자
  ```python
  a = 1.2
  a = -3.45
  ```
  - 컴퓨터식 지수 표현 방식
  ```python
  a = 4.24E10
  a = 4.24e-10
  ```
+ 8진수와 16진수
  - 8진수(Octal)
  ```python
  >>> a = 0o177
  >>> print(a)
  127
  ```
  - 16진수(hexadecimal)
  ```python
  >>> a = 0x8ff
  >>> b = 0xABC
  >>> print(b)
  2748
  ```
+ 사칙연산
  ```python
  >>> a = 3
  >>> b = 4
  >>> a + b
  7
  >>> a - b
  -1
  >>> a * b
  12
  >>> a / b
  0.75
  ```
+ 제곱(**) 연산자
  ```python
  >>> a = 3
  >>> b = 4
  >>> a ** b
  81
  ```
+ 나머지를 반환하는 % 연산자
  ```python
  >>> 7 % 3
  1
  ```
+ 몫을 반환하는 // 연산자
  ```python
  >>> 7 / 4
  1.75
  >>> 7 // 4
  1
  ```

## 02-2 문자열 자료형
+ 큰 따옴표
  ```python
  "Hello World"
  ```
+ 작은 따옴표
  ```python
  'Hello World'
  ```
+ 큰 따옴표 3개
  ```python
  """Hello World"""
  ```
+ 작은 따옴표 3개
  ```python
  ''Hello World'''
  ```
이스케이프 코드
  |코드|설명|
  |---|--------|
  |\n|문자열 안에서 줄을 바꿀 때 사용|
  |\t|문자열 사이에 탭 간격을 줄 때 사용|
  |\\\ |\를 그대로 표현할 때 사용|
  |\'|'를 그대로 표현할 때 사용|
  |\"|"를 그대로 표현할 때 사용|
  |\r|캐리지 리턴(줄 바꿈 문자, 커서를 현재 줄의 가장 앞으로 이동)|
  |\f|폼 피드(줄 바꿈 문자, 커서를 현재 줄의 다음 줄로 이동)|
  |\a|벨 소리(출력할 때 PC 스피커에서 '삑' 소리가 난다|
  |\b|백 스페이스|
  |\000|NULL 문자|
+ 문자열 연산
  - 문자열 더해서 연결
    ```python
    >>> head = "Python"
    >>> tail = " is fun!"
    >>> head + tail
    'Python is fun!'
    ```
  - 문자열 곱하기
    ```python
    >>> a = "python"
    >>> a * 2
    'pythonpython'
    ```
  - 문자열 길이 구하기
    ```python
    >>> a = "Life is too short"
    >>> len(a)
    17
    ```
  - 문자열 인덱싱
    ```python
    >>> a = "Life is too short, You need Python"
    >>> a[3]
    'e'
    ```
+ 문자열 포매팅 string formatting
  ```python
  >>> "I eat %d apples." %3
  'I eat 3 apples.'
  ```
+ format 함수를 사용한 포매팅
  ```python
  >>> "I eat {0} apples.".format(3)
  'I eat 3 apples.'
  ```
+ f 문자열 포매팅
  ```python
  >>> name = '홍길동'
  >>> age = 30
  >>> f'나의 이름은 {name}입니다. 나이는 {age}입니다.'
  '나의 이름은 홍길동입니다. 나이는 30입니다.'
  ```
+ 문자열 관련 함수들
  - 문자 개수 count
  - 문자열에서의 문자 위치 find, index
  - 문자열 삽입 join
  - 소문자->대문자 upper
  - 대문자->소문자 lower
  - 왼쪽 공백 지우기 lstrip
  - 오른쪽 공백 지우기 rstrip
  - 양쪽 공백 지우기 strip
  - 문자열 바꾸기 replace
  - 문자열 나누기 split
## 02-3 리스트 자료형
+ 리스트
  ```python
  >>> odd = [1, 3, 5, 7, 9]
  ```
+ 리스트의 인덱싱과 슬라이싱
+ 리스트 연산하기
  - 더하기(+)
  - 반복하기(*)
  - 길이 구하기 - len 함수
+ 리스트 수정과 삭제
  - 값 수정하기
  - del을 이용해 요소 삭제하기
    ```python
    >>> a = [1, 2, 3]
    >>> del a[1]
    >>> a
    [1, 3]
    ```
+ 리스트 관련 함수
  - 요소 추가하기 - append
  - 정렬 - sort
  - 뒤집기 - reverse
  - 인덱스 반환 - index
  - 요소 삽입 - insert
  - 요소 제거 - remove
  - 요소 끄집어 내기 - pop
  - 요소 개수 세기 - count
  - 확장 - extend
## 02-4 튜플 자료형
+ 리스트와의 차이점
  리스트는 [], 튜플은 () - 소괄호는 생략 가능
  리스트는 요솟값의 생성, 삭제, 수정 가능
  튜플은 요솟값을 바꿀 수 없음
  단 1개의 요소만을 가질 때는 요소 뒤에 쉼표를 반드시 붙여야 함
## 02-5 딕셔너리 자료형
  Key와 Value를 한 쌍으로 가지는 자료형
  ```python
  >>> dic = {'name' : 'pey', 'phone' : '010-9999-1234'}
  ```
+ 딕셔너리 쌍 추가, 삭제
  - 추가하기
    ```python
    >>> a = {1: 'a'}
    >>> a[2] = 'b'
    >>> a
    {1: 'a', 2: 'b'}
    ```
  - 삭제하기 - del 함수 사용 (key값을 요소로 사용)
    ```python
    >>> del a[1]
    >>> a
    {2: 'b'}
    ```

+ 주의점
  Key에 리스트는 사용 불가, 튜플은 사용 가능
  판단하는 기준은 Key가 변하는 값인지, 변하지 않는 값인지(튜플 : 요솟값 바꿀 수 없음)
  Value는 상관없이 아무 값이나 넣을 수 있음
+ 딕셔너리 관련 함수
  - Key 리스트 만들기 - keys
  - Value 리스트 만들기 - values
  - Key, Value 쌍 얻기 - items
  - Key : Value 쌍 모두 지우기 - clear
  - Key로 Value 얻기 - get
  - 해당 Key가 딕셔너리 안에 있는지 조사하기 - in
## 02-6 집합 자료형
  집합(set)은 집합에 관련된 것을 쉽게 처리하기 위해 만든 자료
  중복을 허용하지 않고, 순서가 없음
  ```python
  >>> s1 = set([1, 2, 3])
  >>> s1
  {1, 2, 3}
  ```
+ 교집합
  - &
  - intersection
+ 합집합
  - |
  - union
+ 차집합
  - -
  - difference
+ 값 1개 추가하기 - add
+ 값 여러개 추가하기 - update
+ 특정 값 제거하기 - remove
## 02-7 불 자료형
  True : 참
  False : 거짓
## 02-8 자료형의 값을 저장하는 공간, 변수
변수_이름 = 변수에_저장할_값
