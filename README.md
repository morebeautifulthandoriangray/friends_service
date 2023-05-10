<h1 align="center">Hi there, I'm <a href="" target="_blank">Kate Ezhova</a> 
<img src="https://github.com/blackcater/blackcater/raw/main/images/Hi.gif" height="32"/></h1>
<h3 align="center">Computer science student </h3>
<h3 align="center">Здесь будет вся информация о проекте: </h3>  

---

## Project set up
### Some install commands can be different on some OS!
1. git clone in terminal: 
`git clone https://github.com/morebeautifulthandoriangray/friends_service.git`
2. choose the place where you want to store the project
3. open  IDE(I used Pycharm): `file -> open -> friends_service`
4. then open terminal in IDE and install next: 
   ```
   pip3 install django
   
   pip3 install django-allauth -- for login/logout
   
   pip install drf-yasg -U   -- for Swagger
   
   pip install django-rest-swagger
    ```
   
5. run server with:
    ```
   python manage.py runserver -- Win
   python3 manage.py runserver -- Mac
   ```
6. server is running on `http://127.0.0.1:8000/` 

---

## Endpoints description
1. profiles
    `http://127.0.0.1:8000/`  + 
    ```python
   
   'swagger/' - this endpoint describes REST interface with OpenApi
   
   '/' - empty path is initial endpoint for the app
   
   '/profiles/myprofile/' - shows my profile and here we can see how many friends we have 
   
   '/profiles/' - shows all profiles that exist in o the app
   
   '/profiles/my-invites/' - shows invites that were sent by other users
   
   '/profiles/<slug>/' - shows other user's profile
   
   '/profiles/to-invite/' - shows users that we wait them to invite us
   
   '/profiles/send-invite/' - this endpoint is used to send invites to other users
   
   *when we send invite clicking on button, 'waiting for invite' appers*
   *when we received an invitation, in navbar we can see how many people sent invitations '*
   
   '/profiles/remove-friend/' - this endpoint is used to remove user from a friend list

    '/profiles/my-invites/accept/' - is used to accept the invitation from a user
   
    '/profiles/my-invites/reject/' - is used to reject the invitation from a user
   ```
2. posts
   
    ```python
   'posts/' - shows posts from other users
   ```

3. login and logout

    ```python
    /accounts/login/ - login into a system
   
    /accounts/logout/ - logout from a system
   
   to log in system use this:
   - login: alastuer@gmail.com
   - password: 1111
   
   or 
   - login: test@mail.com
   - password: 123asd456dfg
   
    ```
4. admin
-
    ```python
    /admin/ - admin panel for regulating profiles,
    users, relationships between users
   
   to get admin panel use this:
   - login: keito
   - password: 1111

    ```
5. Dockerfile

   - я не успела реализовать докерфайл, но я бы сделала следующее:
     
     - сделала бы Dockerfile для серверной части (будет внутрений/внешний порт)
     - сделала бы Dockerfile для клиентской части (будет внутрений/внешний порт)
     - сделала бы Dockerfile для базы данных (будет внутрений порт - чтобы обезопасить нашу бд)
     - упаковала в docker-compose.yml и запустила
   
   в дополнение создала бы .env файл, чтобы складывать туда параметры бд и поставила бы этот файл в .gitignore
