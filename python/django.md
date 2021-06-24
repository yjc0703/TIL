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



### EMAIL 모듈
1. setting.py
```python
EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
EMAIL_HOST = '' # SMTP 서버 주소
EMAIL_HOST_USER = '' # SMTP 사용자명
EMAIL_HOST_PASSWORD = '' # SMTP 사용자 비밀번호
EMAIL_PORT = 0 # SMTP 포트번호
EMAIL_USE_TLS = True # TLS 프로토콜 사용여부
DEFAULT_FROM_EMAIL = '' # 기본 이메일 발송 주소
```




2. 템플릿 처리
```python
from django.template.loader import render_to_string
msg_html = render_to_string('이메일 템플릿 HTML 파일 위치', 템플릿 랜더링 데이터)
```




3. 발송
``` python
from django.core.mail import send_mail, EmailMessage
msg = EmailMessage(subject = 제목, body=내용, bcc=수신자리스트)
msg.content_subtype = 'html'
msg.send()
```