# Connect to database in develop mode
https://docs.djangoproject.com/en/5.0/ref/databases/
## PostgreSQL

  ### Setting up postgreSQL
  
  #### 1. Create login/role
  ![image](https://github.com/jittakorn-ch/Knowledge-Center/assets/76931129/9050a92a-1fe4-47a1-bb33-b1dab31ba74c)
    - Named
  ![image](https://github.com/jittakorn-ch/Knowledge-Center/assets/76931129/6cb95a1f-659e-4c69-905c-67b55c8b7ac0)
    - Difind password
    ![image](https://github.com/jittakorn-ch/Knowledge-Center/assets/76931129/9dd4005e-8b43-44d3-876c-33243d8f1437)
    - Save

  #### 2. Create database
  ![image](https://github.com/jittakorn-ch/Knowledge-Center/assets/76931129/088e67ea-bda0-47cc-9cf9-f269e90ee12d)
    - Named database and select owner (login/role)
  ![image](https://github.com/jittakorn-ch/Knowledge-Center/assets/76931129/b589b05f-5692-4a9c-8baa-9d9c9d13b87c)
    - Open can login
  ![image](https://github.com/jittakorn-ch/Knowledge-Center/assets/76931129/bf03a808-c2a8-411d-a240-1d6fc140a3c6)
    - Save

  ### Setting up Django

  - install _psycogp2_ packages
  ```
  pip install psycopg2
  ```
  > Don't forget to activate environment
  - Replace
  ```
  DATABASES = {
      "default": {
          "ENGINE": "django.db.backends.sqlite3",
          "NAME": BASE_DIR / "db.sqlite3",
      }
  }
  ```
  with 
  ```
  DATABASES = {
      "default": {
          "ENGINE": "django.db.backends.postgresql",
          "NAME": "myHub",
          "USER": "forMyHub",
          "PASSWORD": "1234",
          "HOST": "127.0.0.1",
          "PORT": "5432",
      }
  }
  ```
  - run _migrations_
  ```
  python manage.py migrate
  ```


