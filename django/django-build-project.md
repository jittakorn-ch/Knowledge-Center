## Build Project
  - Command Prompt 
      - Create directory name _my_project_
        ```
         mkdir my-project
        ```
      - Navigate to directory to work with. In this case it is _my_project_
        ```
         cd my-project
        ```
      - Create a virtual environment named _env_
        ```
         python -m venv env
        ```
      - Activate environment _env_
        ```
         env\Scripts\activate
        ```
        > PowerShell
        ```
          env\Scripts\activate.ps1
        ```
        > If above is not working try this
        ```
          Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope Process -Force
        ```
        ```
          ./env/Scripts/activate.ps1
        ```
        >For more detail https://stackoverflow.com/questions/1365081/virtualenv-in-powershell
      - Install Django
        ```
         pip install django
        ```
      - Create Django project named _mysite_
        ```
         django-admin startproject mysite .
        ```
        > ใช้ . เพื่อบอกให้ Django สร้าง project ใน directory ปัจจุบัน ที่ใช้งานอยู่ใน Command Prompt
        ```
        my_project/
        ├── manage.py
        └── mysite/
            ├── __init__.py
            ├── asgi.py
            ├── settings.py
            ├── urls.py
            └── wsgi.py
        ```
        > ถ้าไม่ใช้ .
        ```
        my_project/
        ├── mysite/
            ├── manage.py
            └── mysite/
                ├── __init__.py
                ├── asgi.py
                ├── settings.py
                ├── urls.py
                └── wsgi.py
        ```
      - Create Django app named _myapp_
        ```
        python manage.py startapp myapp
        ```
        ```
        my_project/
        ├── manage.py
        └── mysite/
        |   ├── __init__.py
        |   ├── asgi.py
        |   ...
        └── myapp/
            ├── __init__.py
            ├── admin.py
            ...
          
        ```
      - Open text editor to develop
        ```
        code .
        ```
