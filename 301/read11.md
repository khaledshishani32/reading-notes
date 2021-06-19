# Authentication

---

### 1) What is OAuth?
- OAuth is an open-standard authorization protocol or framework that describes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing the initial, related, single logon credential. In authentication parlance, this is known as secure, third-party, user-agent, delegated authorization.

### 2) Give an example of what using OAuth would look like.
-   example of OAuth is when you go to log onto a website and it offers one or more opportunities to log on using another website’s/service’s logon. You then click on the button linked to the other website, the other website authenticates you, and the website you were originally connecting to logs you on itself afterward using permission gained from the second website.

### 3) How does OAuth work? What are the steps that it takes to authenticate the user?
-  The User Shows Intent.
-  The Consumer Gets Permission.
-  The User Is Redirected to the Service Provider.
- The User Gives Permission
-  The Consumer Obtains an Access Token
-  The Consumer Accesses the Protected Resource



    
 
### 4) What is OpenID?
- OpenID allows you to use an existing account to sign in to multiple websites, without needing to create new passwords.





--- 
### 1) What is the difference between authorization and authentication?

-  Authentication and authorization might sound similar, but they are distinct security processes in the world of identity and access management (IAM). Authentication confirms that users are who they say they are. Authorization gives those users permission to access a resource.




### 2) What is Authorization Code Flow?
- The OAuth 2.0 authorization code flow is described in section 4.1 of the OAuth 2.0 specification. It's used to perform authentication and authorization in the majority of app types, including single page apps, web apps, and natively installed apps.
 

 
### 3) What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?
- The Authorization Code Flow + PKCE is an OpenId Connect flow specifically designed to authenticate native or mobile application users. This flow is considered best practice when using Single Page Apps (SPA) or Mobile Apps. PKCE, pronounced “pixy” is an acronym for Proof Key for Code Exchange. 

### 4) What is Implicit Flow with Form Post?

- Implicit Flow with Form Post flow uses OIDC to implement web sign-in that is very similar to the way SAML and WS-Federation operates. The web app requests and obtains tokens through the front channel, without the need for secrets or extra backend calls.

### 5) What is Client Credentials Flow?
- The Client Credentials flow is a server to server flow. There is no user authentication involved in the process. ... Since there is no user authorization, the flow only interacts with the Token endpoint.
- 


### 6) What is Device Authorization Flow?
- The OAuth 2.0 Device Authorization Grant (formerly known as the Device Flow) is an OAuth 2.0 extension that enables devices with no browser or limited input capability to obtain an access token.


### 7) What is Resource Owner Password Flow?
- The Resource Owner Password Credentials flow allows exchanging the username and password of a user for an access token and, optionally, a refresh token. The primary difference is that the user's password is accessible to the application.
 


---
### references :
---
[Google](https://www.google.com)
[stackoverflow.](https://stackoverflow.com)
[educative](https://www.educative.io)
[flow.org](https://flow.org/en/docs/react/components/)