# 기초

> 파이썬은 동적 타이핑 인터프리터 언어



1. 설치 - 아나콘다
   - 파이썬 핵심 라이브러리와 가상환경을 지원
   - 웹용 REPL 인 쥬피터 노트북 포함
   - https://www.anaconda.com/



2. 예약어

   ```python
   import keyword
   keyword.kwlist
   ```



3. 접근제어자
   - 언어에서 제공하는 접근제어자 없음
   - 관례적으로 사용
     - _ : protected
     - __ : private



4. 식별자
   - [pep naming conventions](https://www.python.org/dev/peps/pep-0008/#prescriptive-naming-conventions).
   - 내장함수 이름으로 식별자 선언이 가능하므로 주의
   - 되돌리려면 del 사용



5. 자료형
   - 정수
   - 실수
     - 0 생략 가능(ex: .3)
   - 복소수
     - 수학에서 허수 i 를 j 로 표현
   - 논리



6. 연산자
   - ** : 제곱
   - // : 몫에서 소수점 이하를 버리고 정수만
     - 옧이 음수일 때는 내림된 작은 수로



7. 진법
   - 2진법 : 0b
   - 8진법 : 0o(알파벳 소문자 o)
   - 16진법 : 0x



8. 내장함수
   - https://docs.python.org/3.8/library/functions.html
   
   
   
9. 식
   - 식은 하나의 값으로 축약 가능
      ```python
      1 + 1 # 2
      ```


10. 문
   - 문은 실행 가능한 코드 조각으로 축약 불가능
      ```python
      a = 1
      ```
      
      
11. 복합할당
   - 같은 값을 동시에 할당 가능
   ```python
   a = b = 1
   ```
   * 하나의 변수 값을 변경해도 나머지 변수에는 영향을 주지 않는다(값타입)
      ```python
      a = 2
      print(a) # 2
      print(b) # 1
      ```
   * mutable 복합할당은 주의할 것(참조타입인 경우 유의할 것)
      ```python
      a = b = [1, 2, 3]
      a.append(4)
      print(a) # [1, 2, 3, 4]
      print(a) # 1, 2, 3, 4
      ```
      


12. 언팩킹
   - 파이썬에서 swapping
      ```
      a = 1
      b = 2
      a, b = b, a
      ```

   - 좌, 우변의 갯수가 같으면 동시에 할당 가능
      ```
      a, b = 1, 2
      ```

   - 좌, 우변 갯수가 맞지 않는 경우 starred(*)
       ```
       a, *b = 1, 2, 3, 4
       print(a) # 1
       print(b) # [2, 3, 4]
       ```

13. 증감할당
- python 에서는 ++ 연산자 지원하지 않음.
   ```python
   a += 1
   ```

14. 조건판별
- and, or (&&, || 미지원)

15. interning
- 객체 재사용을 위한 기법
- 숫자 -5 ~ 256 까지 
- 동일한 영문자가 이미 사용된 경우(공백이 있는경우 X)
- interning 지원되지 않는 경우 명시적으로 사용 가능  
    ``` intern('hello world') ```