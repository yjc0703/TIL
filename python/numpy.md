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



8. axis



9. 배열의 조작

   - reshape
   - resize
   - split
   - stack

