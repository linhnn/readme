# ShopBack: Node.js Code Challenge

Author: Linh Nguyen <linhvt22@gmail.com>

## Mission
Our online shopping web application runs on many devices and we need an API package to perform some authentication functions. “Users” of this API package are developers like you.

Run
-----------------------

```sh
npm install
npm start
```

Test
-----------------------
```sh
npm test
```

URL: http://localhost:8080/api/

### API List
* Sign Up:
    * POST /api/signup/
* Log In:
    * POST /api/login/
* Log Out:
    * GET /api/logout/      
* Search:
    * GET /api/search/    
    
    
### POST /api/signup/

Allow users to register a new account

Request body:

    [
        {
            "name": "admin",
            "email": "admin@email.com",
            "password": "12345678",
        }
    ]
    
### POST /api/login/

Account login by "email" and "password"

Request body:

    [
        {
            "email": "admin@email.com",
            "password": "12345678",
        }
    ]    


### GET /api/logout

Send uuid in request header

Response body:

{
    "message": "Log out suceess!"
}

### GET /api/search

Send uuid in request header

Response body:

```
{
    "data": [
        {
            "email": "admin@email.com",
            "name": "linh",
            "password": "1234567",
            "created_at": 1530105558937,
            "latest_access": 1530105696777
        },
        {
            "email": "user@email.com",
            "name": "linh",
            "password": "123456789",
            "created_at": 1530105558937,
            "latest_access": 1530105558946
        }
    ]
}
```


