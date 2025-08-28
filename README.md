# 🐍 Django Setup Guide 

## 1️⃣ Create & Activate Virtual Environment
```bash
python -m venv venv
venv\Scripts\activate      # Windows
source venv/bin/activate   # Mac/Linux

2️⃣ Install Django
pip install django
django-admin --version

3️⃣ Start a Django Project
django-admin startproject myproject
cd myproject
python manage.py runserver
Visit 👉 http://127.0.0.1:8000/

4️⃣ Apply Migrations
python manage.py migrate

5️⃣ Create a Superuser (Admin Login)
python manage.py createsuperuser
# username: yourname
# password: yourpassword
Login 👉 http://127.0.0.1:8000/admin/

6️⃣ Create a Custom App (Example: notes)
python manage.py startapp notes
Add "notes" to INSTALLED_APPS in settings.py.

7️⃣ Models Example (notes/models.py)
from django.db import models

class Note(models.Model):
    title = models.CharField(max_length=200)
    content = models.TextField()
    slug = models.SlugField(unique=True)

    def __str__(self):
        return self.title
Run:
  python manage.py makemigrations
  python manage.py migrate

8️⃣ Register Model in Admin (notes/admin.py)
from django.contrib import admin
from .models import Note

admin.site.register(Note)

9️⃣ Test in Django Shell
python manage.py shell

from notes.models import Note
note = Note(title="DSA Notes", content="All syllabus for CSIT & Engineering.", slug="dsa-note")
note.save()
print(Note.objects.all())



