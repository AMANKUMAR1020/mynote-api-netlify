# Mynote Server
### In this, we are used many modules ans library of javascript and node.js

 *Let discuss the features and working structure of Mynote Server*
    
# Working
---
## Routing :- 
### authroutes :-it handle authentication of user 
- **login**  required username and password, this create =="accessToken" and "refreshToken"== token. Finally token send to client.
- **refresh** :- it execute autometically after expire of refresh token and then token send to client.
- **logout** :- terminate the refresh token.
        
### userRoutes :- it handle user
- **getAllUsers** :- provide all users from mongodb.
- **createNewUser** :- after authentication and autherisation , it allow to create ==new user in database==.
- **updateUser** :- only autherise person is required.
- **deleteUser** :- Admin and maanger are allow to delete user.
    
### notesRoutes :- it handle notes
- **getAllNotes** :- provide all notes along users from mongodb
- **createNewNote** :- create a new notes or assignment
- **updateNote** :- only autherise person is required. 
- **deleteNote** :-  Admin and maanger are allow to delete user.
---
   
# Schema 
### User
```
{
    username: {usernane},
    password: {string},
    roles: [{default: "Employee"}],
    active: {Boolean}
}
```

### Note
```
{
    user: {userId},
    title: {string},
    text: {string },
    completed: { boolean }
    {date:time}
}
```
---


# Modules used
- **bcrypt** : to encrypt and decrept password,
- **cookie-parser** : To handle cookie on server and client side,
- **date-fns** : nodejs modules used in logging,
- **dotenv** : Keep safe important uri, passwords, etc,
- **express** : routing path in server,
- **express-async-handler** : handling async routing,
- **jsonwebtoken**: used for authentication and authrisation purpose,
-  **mongoose** : to communicate with mongodb database,
-  **uuid** : create unique id, which is used in log writing 
---
## Installation

Dillinger requires [Node.js](https://nodejs.org/) v10+ to run.
Install the dependencies and devDependencies and start the server.

```sh
cd mynote-api-netlify

MONGO_URI=Your_uri
ACCESS_TOKEN=xxxx
REFRESH_TOKEN=xxxx

npm i
npm run dev
```

For production environments...

```sh
npm install --production
NODE_ENV=production node app
MONGO_URI=Your_uri
ACCESS_TOKEN=xxxx
REFRESH_TOKEN=xxxx
```
---
## Helps and links

Instructions on how to use them in your own application are linked below.

| Name | LINKS |
| ------ | ------ |
| mongoDb | [https://www.mongodb.com/][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Grave Dave | [https://www.youtube.com/@DaveGrayTeachesCode/playlists][PlGd] |
| digitalocean | [https://www.digitalocean.com/][PlOd] |
| freecodecamp | [https://www.freecodecamp.org/][PlMe] |
| render .com | [https://dashboard.render.com/static/srv-cjm24o8cfp5c73e23l10][PlGa] |
---

