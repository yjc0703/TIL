# numpy

> 과학 계산을 위한 파이썬 패키지



1. import

   ```python
   import numpy as np
   ```

   numpy 약어는 관례상 np로 사용



2. 생성

   - array : 리스트를 배열로 생성
   - zeros : 0으로 채워진 배열 생성
   - ones : 1로 채워진 배열 생성
   - eye : 단위행렬 생성
     - 단위행렬 : 주대각선의 원소가 모두 1이며 나머지는 모두 0(=항등행렬)
   - identity : = eye
   - full : 입력한 값으로 채움
   - empty : 비어있는(혹은 쓰레기 값이 있는) 배열 생성
   - linspace : 선형간격 벡터 생성
   - logspace : 로그간격 벡터 생성
   - arange : 범위안의 수치로 벡터 생성



3. indexing, slicing

   - list 사용법 참고



4. fancy indexing

   - int 나 boolean 값을 가지는 numpy 배열로 인덱싱 가능

   ```python
   a = np.array([[ 5,  6,  7,  8,  9],
                 [15, 16, 17, 18, 19],
                 [25, 26, 27, 28, 29]])
   a[[1,3,5],[0,2,4]] # [ 5, 17, 29]
   ```

   - indexing 은 원래 차원 -1차원의 데이터를 가져오지만 fancy indexing 은 원래 차원 그대로 가져온다



5. ellipsis

   - ... 이후의 모든 것

   

6. 연산



7. broadcasting

   - 연산을 위한 배열간 모양이 동일하지 않을 때 특정한 조건이 맞으면 자동으로 모양이 같게 만들어 연산하는 기능



8. axis

   - 다차원 배열을 연산할 때 기준 축
   - 



9. 배열의 조작

   - reshape
   - resize
   - split
   - stack : shape 의 크기를 증가시켜서 병합
   - concatenate : 원래 shape 크기를 그대로 유지




10. 그밖에

   - where 
      - 조건만 넣을 경우 True 인 index 를 반환한다.
      - 참, 거짓인 경우에 대한 대체값을 넣을 수 있다

