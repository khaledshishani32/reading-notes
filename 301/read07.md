    # REST

---

### 1) Who is Roy Fielding?
- one of the principal authors of the HTTP specification and the originator of the Representational State Transfer (REST) architectural style. He is an authority on computer network architecture and co-founded the Apache HTTP Server project.

### 2) Why don’t the techniques that we use today work well when we need to be able to talk to all of the machines in the world?
- Because they weren't designed to be used like that. When Fielding and his colleagues started building the web, being able to talk to any machine anywhere in the world was a primary concern. But most of the techniques developers later used to get computers to talk to each other didn't have those requirements. You just needed to talk to a small group of machines.

### 3) What is the HTTP protocol that Fielding and his friends created?

- it is capable of describing the location of something anywhere in the world from anywhere in the world. It's the foundation of the web. You can think of it like GPS coordinates for knowledge and information.



    
 
### 4) What does a GET do?
- GET is used to request data from a specified resource and it is one of the most common HTTP methods.




### 5)  What does a POST do?
- POST is used to send data to a server to create/update a resource.

### 6) What does PUT do?
- PUT is used to send data to a server to create/update a resource.
- The difference between POST and PUT is that PUT requests are idempotent. That is, calling the same PUT request multiple times will always produce the same result. In contrast, calling a POST request repeatedly have side effects of creating the same resource multiple times.

 

 
### 7) What does PATCH do?
- The HTTP PATCH request method applies partial modifications to a resource.
- PATCH is somewhat analogous to the "update" concept found in CRUD (in general, HTTP is different than CRUD, and the two should not be confused).
- A PATCH request is considered a set of instructions on how to modify a resource. Contrast this with PUT; which is a complete representation of a resource.



### references :
---
[nodejs](https://nodejs.dev/learn)
[stackoverflow.](https://stackoverflow.com)
[educative](https://www.educative.io)
[flow.org](https://flow.org/en/docs/react/components/)