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