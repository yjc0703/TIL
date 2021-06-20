# 유용한 라이브러리
> 파이썬 개발에 유용한 라이브러리들

1. itertools : 반복 형태의 데이터를 처리하기 위한 유용한 기능을 제공
   - count : 반복하고자 하는 최대수를 몰라도 step 단위로 값을 반환
      ```python
      from itertools import count
      # 0 부터 10씩 증가하는 값과 [a, b, c] 를 병합
      for c, n in zip(count(0, 10), ['a', 'b', 'c']):
          print(c, n)
   
      out:
      0 a
      10 b
      20 c
      ```


2. heapq : 힙(Heap) 자료구조 제공. 우선순위 큐를 사용하기 위해 활용



3. bisect : 이진 탐색 기능을 제공



4. collections : 덱(deque), 카운터(counter) 등의 유용한 자료구조를 제공



5. math : 필수적인 수학기능 제공