<h1 align="center">Hi there, I'm <a href="https://daniilshat.ru/" target="_blank">Kate Ezhova</a> 
<img src="https://github.com/blackcater/blackcater/raw/main/images/Hi.gif" height="32"/></h1>
<h3 align="center">Computer science student </h3>
<h3 align="center">Здесь будет вся информация о проекте: </h3>  

---

## Project set up
1. git clone in terminal: 
`git clone https://github.com/morebeautifulthandoriangray/friends_service.git`
2. then open project with IDE(I used Pycharm)
3. then open terminal in IDE and run the server: `python3 manage.py runserver`
4. server is running on `http://127.0.0.1:8000/` 

---

## Endpoints description
1. profiles
    `http://127.0.0.1:8000/`  + 
    ```python
   
   'swagger/' - this endpoint describes REST interface with OpenApi
   
   '/' - empty path is initial endpoint for the app
   
   '/profiles/myprofile/' - shows my profile
   
   '/profiles/' - shows all profiles that exist in o the app
   
   '/profiles/my-invites/' - shows invites that were sent by other users
   
   '/profiles/<slug>/' - shows other user's profile
   
   '/profiles/to-invite/' - shows users that we can invite
   
   '/profiles/send-invite/' - this endpoint is used to send invites to other users
   
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
    ```
