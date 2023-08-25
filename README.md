# Bootstrap User Registration

## Création d'un projet

- mkdir (folder) && cd (folder)
- django-admin startproject (website)
- cd (website)

### ou plus simple

- django-admin startproject (website) .
- ./manage.py startapp (main)

#### Création de l'environnement

- python -m venv env

#### Installation de pip

- py -m ensurepip --upgrade
- python.exe -m pip install --upgrade pip
- pip install django

#### Connexion du terminal à la source du projet

- source env/Scripts/activate
- source env/Scripts/deactivate

- Si deactivate n'éxiste pas créer le dans le même répértoire que activate,
- puis mettez ceci en éditant le fichier:

- #!/bin/bash
- deactivate

#### Création de la migration

- python manage.py makemigrations
- python manage.py migrate
- python manage.py collectstatic

#### Création du Super User

- python manage.py createsuperuser

#### Créer un fichier requirements.txt

#### s'il n'existe pas pour ajouter les extensions ou api à ajouter dans le projet

- pip freeze > requirements.txt
- pip freeze -r requirements.txt

#### Générer un SECRET KEY

- python -c 'from django.core.management.utils import get_random_secret_key; print(get_random_secret_key())'

##### ou avec cette commande

- python -c "import secrets; print(secrets.token_urlsafe())"

##### ou avec l'interpreteur python

##### Console python

- import secrets
- length = 50
- chars = 'abcdefghijklmnopqrstuvwxyz0123456789!@#$%^&*(-_=+)'
- secret_key = ''.join(secrets.choice(chars) for i in range(length))
- print(secret_key)

###### Normal (16), (64), (128)

- >>> import secrets
- >>> secrets.token_bytes(16)
- >>> secrets.token_hex(16)
- >>> token_urlsafe(16)
