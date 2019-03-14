# API WRITEUP

In Progress

### Signup.php

*Expects*

  {
    "username": "example",
    "password": "example"
  }

*Returns*

On Success: 

  {
    "error": ""
  }
 
Otherwise, returns some error message

### Login.php

*Expects*

  {
    "username": "example",
    "password": "example"
  }
  
*Returns*

On Success:
  {
    "token": (some JWT),
    "error": ""
  }

Token is a Json Web Token which you will use for further API requests. 
When decoded the body of the token will contain the following:     

{
  "username" : $username,
  "displayname" : $displayName,
  "user_id" : $id
  "profile_pic_url": $url
 }
  
Otherwise, returns some error message and no token

To test JWT on your own, https://jwt.io/ is great. 