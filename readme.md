# Aprendendo MVC com DJANGO: CRUD

Estou usando Python 3.10 e sistema operacional Windows 10.

## SETUP INICIAL

- No bash:
```
python -m venv env
. env/Scripts/activate
pip install --upgrade pip
pip install django
django-admin startproject crud
cd crud
python manage.py startapp employee
```

- Crie os arquivos:
  - templates/base.html
  - employee/templates/employee/list.html
  - employee/templates/employee/create.html
  - employee/templates/employee/edit.html
  - employee/templates/employee/delete.html
  - employee/urls.py
  - employee/forms.py

- Adicione `'employee.apps.EmployeeConfig'` em `INSTALED_APPS` em *settings.py*.

- Adicione `BASE_DIR / 'templates'` em `DIRS` em *settings.py*

- Crie o model Employee em *employee/models.py*
- Registre o model no admin em *employee/admin.py*

- No bash:
```
python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

- Teste o estágio atual do projeto.

- Crie as views em *employee/views.py*. Crie as views nesse estágio do projeto apenas para renderizarem os templates, sem funcionalidades.

- Crie as urls em *employee/urls.py*

- Inclua employee.urls em urls em *crud/urls.py*

- Insira o código do template base em *templates/base.html*

## CRUD

### LIST ALL

- Insira o código do template list em *employee/templates/employee/list.html* 
- Insira as funcionalidades da view list em *employee/views.py*

### CREATE

- Crie o formulário de empregados em *employee/forms.py*
- Insira o código do template create em *employee/templates/employee/create.html* 
- Insira as funcionalidades da view create em *employee/views.py*

### EDIT
- Insira o código do template create em *employee/templates/employee/edit.html* 
- Insira as funcionalidades da view edit em *employee/views.py*

### DELETE
- Insira o código do template delete em *employee/templates/employee/delete.html* 
- Insira as funcionalidades da view delete em *employee/views.py*

## Referência

- https://python.plainenglish.io/build-a-django-application-to-perform-crud-operations-5990ee90c24a
