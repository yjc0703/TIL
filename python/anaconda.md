# anaconda
> 가상의 python 개발환경을 사용할 수 있도록 함

1. 버전 확인
    ```
    conda -V 
    ```



2. 가상환경 생성
   ```
   conda create -n 가상환경이름 python=3.8.8 anaconda
   ```



3. 가상환경 조회
   ```
   conda info --envs
   ```



4. 가상환경 초기화
   ```
   conda init bash
   ```



5. 가상환경 사용
   ```
   conda activate TodoList
   ```



6. 가상환경 사용 취소
   ```
   conda deactivate
   ```




7. 가상환경 삭제
   ```
   conda remove -n 가상환경이름 --all
   ```