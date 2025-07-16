# Django_setup
D:\Django>python -m venv python

D:\Django>python\Scripts\activate

(python) D:\Django>pip install Django
Collecting Django
  Downloading django-5.2.4-py3-none-any.whl.metadata (4.1 kB)
Collecting asgiref>=3.8.1 (from Django)
  Downloading asgiref-3.9.1-py3-none-any.whl.metadata (9.3 kB)
Collecting sqlparse>=0.3.1 (from Django)
  Using cached sqlparse-0.5.3-py3-none-any.whl.metadata (3.9 kB)
Collecting tzdata (from Django)
  Using cached tzdata-2025.2-py2.py3-none-any.whl.metadata (1.4 kB)
Downloading django-5.2.4-py3-none-any.whl (8.3 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 8.3/8.3 MB 1.3 MB/s eta 0:00:00
Downloading asgiref-3.9.1-py3-none-any.whl (23 kB)
Using cached sqlparse-0.5.3-py3-none-any.whl (44 kB)
Using cached tzdata-2025.2-py2.py3-none-any.whl (347 kB)
Installing collected packages: tzdata, sqlparse, asgiref, Django
Successfully installed Django-5.2.4 asgiref-3.9.1 sqlparse-0.5.3 tzdata-2025.2

[notice] A new release of pip is available: 25.0.1 -> 25.1.1
[notice] To update, run: python.exe -m pip install --upgrade pip

(python) D:\Django>django-admin --version
5.2.4

(python) D:\Django>django-admin startproject firstDjangoProject

(python) D:\Django>cd firstDjangoProject

(python) D:\Django\firstDjangoProject>py manage.py runserver  
Watching for file changes with StatReloader
Performing system checks...

System check identified no issues (0 silenced).

You have 18 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
Run 'python manage.py migrate' to apply them.
July 11, 2025 - 08:39:53
Django version 5.2.4, using settings 'firstDjangoProject.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CTRL-BREAK.

WARNING: This is a development server. Do not use it in a production setting. Use a production WSGI or ASGI server instead.
For more information on production servers see: https://docs.djangoproject.com/en/5.2/howto/deployment/
[11/Jul/2025 08:39:56] "GET / HTTP/1.1" 200 12068
Not Found: /favicon.ico
[11/Jul/2025 08:39:56] "GET /favicon.ico HTTP/1.1" 404 2220

now to check admin:
http://127.0.0.1:8000/admin/login/?next=/admin/

<img width="523" height="427" alt="image" src="https://github.com/user-attachments/assets/18c7297e-6c3e-4fad-b0e6-df3420de95cf" />


make notes for app
python manage.py startapp notes

admin panel
<img width="657" height="574" alt="image" src="https://github.com/user-attachments/assets/59603222-33ea-4203-8ba6-b1f6de50a3ce" />
-> python manage.py createsuperuser
user-mingmasherpa
pass-text@123

<img width="1920" height="472" alt="image" src="https://github.com/user-attachments/assets/6621aa3e-c3f5-4f1a-95e6-90d41b464f3f" />


