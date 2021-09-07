#  What is JSON Web Token?
---
#### JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.



### JSON Web Tokens are useful: on :
- Authorization: This is the most common scenario for using JWT. Once the user is logged in, each subsequent request will include the JWT
- Information Exchange: JSON Web Tokens are a good way of securely transmitting information between parties. 


### JSON Web Token structure :
- Header
- Payload
- Signature

### how it's work :

#### In authentication, when the user successfully logs in using their credentials, a JSON Web Token will be returned. Since tokens are credentials, great care must be taken to prevent security issues. In general, you should not keep tokens longer than required.

---
## Use JWT Authentication with Django REST Framework

#### The JWT is just an authorization token that should be included in all requests:
```
curl http://127.0.0.1:8000/hello/ -H 'Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ0b2tlbl90eXBlIjoiYWNjZXNzIiwiZXhwIjoxNTQzODI4NDMxLCJqdGkiOiI3ZjU5OTdiNzE1MGQ0NjU3OWRjMmI0OTE2NzA5N2U3YiIsInVzZXJfaWQiOjF9.Ju70kdcaHKn1Qaz8H42zrOYk0Jx9kIckTn9Xx7vhikY'
```
- The JWT is acquired by exchanging an username + password for an access token and an refresh token.

- The access token is usually short-lived (expires in 5 min or so, can be customized though).

- The refresh token lives a little bit longer (expires in 24 hours, also customizable). It is comparable to an authentication session. After it expires, you need a full login with username + password again.

### Installation & Setup

```
pip install djangorestframework_simplejwt
```
### settings.py
```
REST_FRAMEWORK = {
    'DEFAULT_AUTHENTICATION_CLASSES': [
        'rest_framework_simplejwt.authentication.JWTAuthentication',
    ],
}
```
### urls.py
```
from django.urls import path
from rest_framework_simplejwt import views as jwt_views

urlpatterns = [
    # Your URLs...
    path('api/token/', jwt_views.TokenObtainPairView.as_view(), name='token_obtain_pair'),
    path('api/token/refresh/', jwt_views.TokenRefreshView.as_view(), name='token_refresh'),
]
```

### Point of The Refresh Token :

#### refresh token may look pointless, but in fact it is necessary to make sure the user still have the correct permissions. If your access token have a long expire time, it may take longer to update the information associated with the token. 

--- 
## Django Runserver Is Not Your Production Server
#### You’ve been running your app locally with python manage.py runserver. That’s a fine command, built for development convenience, but it’s not meant to be used as part of a production setup.

### A Production Stack :
#### When a request arrives at your server, it should be passed to a dedicated web server. Nginx is an example for a good web server.

#### The next component is an application server. It gets those fancy requests and uses them to construct Python objects which are usable by Django.

### How Does Django Fit In? 

#### Your Django app does not actually run as you would think a server would - waiting for requests and reacting to them. Your project provides a uwsgi.py file .

#### This function calls your code, and produces a response object which is passed to the WSGI server. 

### Conclusion : 
#### to run Django in production, be sure to use a production-ready web server like Nginx, and let your app be handled by a WSGI application server like Gunicorn.

#### If you plan on running on Heroku, a web server is provided implicitly. You don’t have to take care of it. You just need to specify a command to run your application server ..

