# numpy

> 과학 계산을 위한 파이썬 패키지



1. import

   ```python
   import numpy as np
   ```

   numpy 약어는 관례상 np로 사용



2. 생성

   - array : 리스트를 배열로 생성
      ```python
      # 1차원
      np.array([1,2,3,4,5])
      
      out: 
      array([1, 2, 3, 4, 5])
      ```
      ```python
      # 2차원
      np.array([[1,2],[3,4]])
      
      out:
      array([[1, 2],
             [3, 4]])
      ```
      ```python
      # 3차원
      np.array([[[1,2],[3,4],[5,6]]])
      
      out:
      array([[[1, 2],
              [3, 4],
              [5, 6]]])
      ```
   - zeros : 0으로 채워진 배열 생성
      ```python
      np.zeros([2,3])
      
      out:
      array([[0., 0., 0.],
             [0., 0., 0.]])
      ```
   - ones : 1로 채워진 배열 생성
      ```python
      np.ones([2,3])
      
      out:
      array([[1., 1., 1.],
             [1., 1., 1.]])
      ```
   - identity : 단위행렬 생성
      - 단위행렬 : 주대각선의 원소가 모두 1이며 나머지는 모두 0(=항등행렬)
      ```python
      # 3 * 3
      np.identity(3)

      out:
      array([[1., 0., 0.],
             [0., 1., 0.],
             [0., 0., 1.]])
      ```
   - eye : = identity. column 갯수 설정 가능
      ```python
      np.eye(3, 2)

      out:
      array([[1., 0.],
             [0., 1.],
             [0., 0.]])
      ```
   - full : 입력한 값으로 채움
      ```python
      # 3 * 2 배열을 5로 채우기
      np.full([3, 2], 5)

      out:
      array([[5, 5],
             [5, 5],
             [5, 5]])
      ```
   - empty : 비어있는(혹은 쓰레기 값이 있는) 배열 생성
      ```python
      # 2개짜리 1차원 배열
      np.empty(2)

      out:
      array([2.12199579e-314, 0.00000000e+000])
      ```
   - linspace : 선형간격 벡터 생성
      ```python
      # 0 ~ 10 까지 3개
      np.linspace(0, 10, 3)

      out:
      array([ 0.,  5., 10.])
      ```
   - logspace : 로그간격 벡터 생성
      ```python
      np.logspace(0, 10, 3)

      out:
      array([1.e+00, 1.e+05, 1.e+10])
      ```
   - arange : 범위안의 수치로 벡터 생성
      ```python
      # 0 ~ (10 - 1) 
      np.arange(10)

      out:
      array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])
      ```



3. indexing, slicing

   - list 사용법 참고



4. fancy indexing

   - int 나 boolean 값을 가지는 numpy 배열로 인덱싱 가능

   ```python
   a = np.array([[ 5,  6,  7,  8,  9],
                 [15, 16, 17, 18, 19],
                 [25, 26, 27, 28, 29]])
   a[[1,2,0],[0,2,4]]
   
   out:
   array([15, 27,  9])
   ```

   - indexing 은 원래 차원 -1차원의 데이터를 가져오지만 fancy indexing 은 원래 차원 그대로 가져온다
   ```python
   # 원래 차원 - 1
   a = np.array([[ 5,  6,  7,  8,  9],
                 [15, 16, 17, 18, 19],
                 [25, 26, 27, 28, 29]])
   a[0]

   out:
   array([5, 6, 7, 8, 9])
   ```
   ```python
   # 원래차원 그대로
   a = np.array([[ 5,  6,  7,  8,  9],
                 [15, 16, 17, 18, 19],
                 [25, 26, 27, 28, 29]])
   a[[0]]

   out:
   array([[5, 6, 7, 8, 9]])
   ```



5. ellipsis

   - ... 이후의 모든 것

   

6. 연산



7. broadcasting

   - 연산을 위한 배열간 모양이 동일하지 않을 때 특정한 조건이 맞으면 자동으로 모양이 같게 만들어 연산하는 기능



8. axis *(추가공부 필요)*

   - 다차원 배열을 연산할 때 기준 축
   - 



9. 배열의 조작 *(추가공부 필요)*

   - reshape : shape 을 조정
      ```python
      np.arange(12).reshape(3,4)
   
      out:
      array([[ 0,  1,  2,  3],
             [ 4,  5,  6,  7],
             [ 8,  9, 10, 11]])
      ```

   - resize : reshape 와 비슷하지만 return 이 없고 shape 의 사이즈가 배열의 아이템 갯수와 맞지 않아도 됨
      ```python
      a = np.arange(12)
      a.resize(3,4)
      a
   
      out:
      array([[ 0,  1,  2,  3],
             [ 4,  5,  6,  7],
             [ 8,  9, 10, 11]])
      ```
      ```python
      b = np.arange(12)
      b.resize(2,2)
      b
   
      out:
      array([[0, 1],
             [2, 3]])
      ```

   - split : 배열을 분할
      ```python
      a = np.arange(12)
      np.split(a, 3)

      out:
      [array([0, 1, 2, 3]), array([4, 5, 6, 7]), array([ 8,  9, 10, 11])]
      ```

   - stack : shape 의 크기를 증가시켜서 병합
      ```python
      a = np.arange(4)
      b = np.arange(4, 8)
      np.stack((a, b))

      out:
      array([[0, 1, 2, 3],
             [4, 5, 6, 7]])
      ```
      ```python
      a = np.arange(4)
      b = np.arange(4, 8)
      np.stack((a, b), axis = 1)

      out:
      array([[0, 4],
             [1, 5],
             [2, 6],
             [3, 7]])
      ```

   - vstack : 
      ```python
      a = np.arange(4)
      b = np.arange(4, 8)
      np.vstack((a, b))

      out:
      array([[0, 1, 2, 3],
             [4, 5, 6, 7]])
      ```

   - hstack : 
      ```python
      a = np.arange(4)
      b = np.arange(4, 8)
      np.hstack((a, b))

      out:
      array([0, 1, 2, 3, 4, 5, 6, 7])
      ```

   - concatenate : 원래 shape 크기를 그대로 유지
      ```python
      a = np.arange(4)
      b = np.arange(4, 8)
      np.concatenate((a, b))

      out:
      array([0, 1, 2, 3, 4, 5, 6, 7])
      ```



10. 그밖에

   - where 
      - 조건만 넣을 경우 True 인 index 를 반환한다.
      - 참, 거짓인 경우에 대한 대체값을 넣을 수 있다
   - newaxis

