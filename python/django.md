# Django
> 파이썬 웹 어플리케이션 개발을 위한 프레임워크

### 설치(아나콘다)
```
conda install django
```



### 프로젝트 생성
```
django-admin startproject 프로젝트명
```



### 서버 실행
```
python manage.py runserver
```



### app 추가
```
python manage.py startapp my_to_do_app
```



### model 추가 후 마이그레이션 데이터 생성

```
python manage.py makemigrations
```



### 마이그레이션 내용 반영

```
python manage.py migrate
```



### db 접속(sqlite3 만 확인됨)

```
python manage.py dbshell
```



### MVC 와의 차이점
| Model    | Controller | View     |
| -------- | ---------- | -------- |
| model.py | views.py   | template |

