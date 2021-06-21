# CRUD

---

### 1) In your own words, describe what each group of status code represents :
- 100’s = Information responses
- 200’s = Successful responses
- 300’s = Redirection messages
- 400’s = Client error responses
- 500’s = Server error responses

### 2) What is a status code 202?
-   The 202 response is intentionally non-committal. Its purpose is to allow a server to accept a request for some other process (perhaps a batch-oriented process that is only run once per day) without requiring that the user agent's connection to the server persist until the process is completed.

### 3) What is a status code 308?
- The HyperText Transfer Protocol (HTTP) 308 Permanent Redirect redirect status response code indicates that the resource requested has been definitively moved to the URL given by the Location headers.



    
 
### 4) What code would you use if an update didn’t return data to a client?

- 200 OK 






### 5) What code would you use if a resource used to exist but no longer does?

-  410 Gone client error response




### 6) What is the ‘Forbidden’ status code?
- The HTTP 403 Forbidden client error status response code indicates that the server understood the request but refuses to authorize it.

---

### 1) Why do we need to pull our MongoDB database string out of our server and put it into our .env?
- some times we have a private info like passwaord , the ID number .

### 2) What is a realational database?

- Middleware (also called pre and post hooks) are functions which are passed control during execution of asynchronous functions. Middleware is specified on the schema level and is useful for writing plugins.
 


### 3) What does app.use(express.json()) do?
- express. json() is a method inbuilt in express to recognize the incoming Request Object as a JSON Object.
- 


### 4) What is the difference beween PUT and PATCH?
- The main difference between the PUT and PATCH method is that the PUT method uses the request URI to supply a modified version of the requested resource which replaces the original version of the resource, whereas the PATCH method supplies a set of instructions to modify the resource.


### 5) What does a 500 error status code mean?
- The HyperText Transfer Protocol (HTTP) 500 Internal Server Error server error response code indicates that the server encountered an unexpected condition that prevented it from fulfilling the request. This error response is a generic "catch-all" response.
 


### 6) What is the difference between a status 200 and a status 201?

- The 200 status code is by far the most common returned. It means, simply, that the request was received and understood and is being processed. A 201 status code indicates that a request was successful and as a result, a resource has been created (for example a new page).




---
### references :
---
[Google](https://www.google.com)
[stackoverflow.](https://stackoverflow.com)
[educative](https://www.educative.io)
[flow.org](https://flow.org/en/docs/react/components/)