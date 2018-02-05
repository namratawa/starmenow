# Architecture - Tools - Frameworks 

This page is to capture high-level architecture for starMe-Now. 

![alt text](https://github.com/namratawa/starmenow/blob/architecture/slides/archtecture.png)

## Client layer

1. Mobile apps for ios and android(*phase 2*). 
   **Phonegap** will be used to create a hybrid app using the web and native APIs provided.
   
2. Desktop app for site administration and Class administrator (*phase 2 feature maybe*)
   **HTML5/JS** based web app will be created.
   
3. starMe-Now developer API (*definitely phase 2/3*). @Anirban and I discussed this long back, third-party apps can integrate for defining activities, hosting classes or rewarding children. The main idea was to centralize rewards for kids at single place. 

## Web Layer

4. **Nginx** will be used here. This layer will be used for 
    * Hosting all web assets (*HTML, CSS, JS*). 
    * Act as caching layer for all web assets, and decrease the load on downstream systems.
    * Will act as an API gateway, so that we have the flexibility to write backend services in multiple languages if need be.
    
## Service layer

5. This is where the actual API interaction starts. Planning to use **Spring Boot** for creating Restful services. In future, if we plan to use **Python** or any other language/framework for creating other services, we can simply put routing rules at **Nginx** layer.

6. **Redis** will be used for all caching needs. We'll get into use case scenarios as we move forward.

7. **Solr** will be used for any advanced search requirements. 

## Storage layer

8. **MongoDB** will be used as the primary persistent store.
9. **Amazon S3** will be used to store objects like profile pictures for users, kids, groups and background pics for dynamically generated activities/classes. 

  




