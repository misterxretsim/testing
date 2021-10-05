# CHAT-APP

With the **Chat-app**, you can use your email as a modern messenger to communicate with your friends or colleagues.

*The app has been developed to showcase relevant skills.*

Therefore, below I describe the technologies or just interesting nuances that I used in the development, as well as for what.  
Also below I will tell you how you can run it and what you need for this.

---

## Table of Contents

- [Docker](#Docker)
- [Nginx](#Nginx)
- [DataBase](#DataBase)
- [API-info(Swagger)](#API\-info)
- [Frontend](#Frontend)
- [Backend](#Backend)
- [App-dev start](#App\-dev-start)
- [App-prod start](#App\-prod-start)

---

## Docker

<p align="center">
   <img src="./dockerrr.png" width="500"/>
</p>

On the first you need [Docker](https://www.docker.com).  
**Chat-app** uses **Docker** for starting [Nginx-server](https://hub.docker.com/_/nginx).  
This is needed to connect the [Frontend](./front) and the [Backend](./back) on the develop version app.  
Also It's needed for delivery [Frontend](./front) to the Browser-client for the production version, and respectively for forwarding requests on the [Backend](./back).

In the future, I plan to switch to **Docker-compose**, because this will greatly simplify the interaction of the [Frontend](./front) with [Backend-servers](./back)(if there are more than 1) and [Backend-server](./back) with a Database (like [PostgreSQL](https://hub.docker.com/_/postgres)).

Therefore you need docker-client.

---

## Nginx

<p align="center">![image](https://user-images.githubusercontent.com/25767145/136075189-99fd4514-b593-4a3a-85c6-86b82f73485d.png)

   <img src="./nginx.png" width="300"/>
</p>

In the application, I am using an [Nginx-server](https://hub.docker.com/_/nginx).  
This is necessary so that the [Frontend](./front) and [Backend](./back) can be combined in the development version.  
Perhaps in the future I will use more than 1 [Backend-server](./back), therefore, **Nginx** will help a lot in implementing this.

[Dev-configuration](./dev/nginx_dev.conf) includes:

* starting the [Nginx-server](https://hub.docker.com/_/nginx) on :8085 port;
* issuing frontend-files for rendering them in the browser from the frontend-server;
* redirect for live-reload;
* redirect for API.

> :warning: **In development**
>
> The product version of the application also uses **Nginx**. It issues the [Frontend](./front) when requested from the browser, and also connects [Frontend](./front) to the [Backend](./back).
> 
> [Prod-configuration](./dev/nginx_prod.conf) includes:
> * starting the [Nginx-server](https://hub.docker.com/_/nginx) on :8085 port;
> * issuing build frontend-files for rendering them in the browser;
> * redirect for API.

---

## DataBase

<p align="center">
   <img src="./SQLite.png" width="300"/>
</p>

The **Chat-app** uses [SQLite](https://www.sqlite.org) as a **Database**.  
In the future, I plan to move to a more efficient **Database** like [PostgreSQL](https://hub.docker.com/_/postgres), but now everything suits me.  
In the [current configuration](./dev/db_conf/tables.conf), I have 3 tables - **Chats**, **Msgs** and **Profile** - linked together by an **one-to-many** relationships.

Also implemented the ``createDB.command`` ([see here](./dev/createDB.command)) **script** to create a **Database** with the required tables.  
**Script** starts [mini-app](./dev/db_conf) which creates clean **Database**.  
Then **script** moves it to [folder with Database-data](./back/db) for [Backend](./back).

---

## API-info

<p align="center">
   <img src="./swagger.svg" width="450"/>
</p>

You can see server API on the http://localhost:2501/api-docs/

> Created with ***Swagger***

---

## Frontend

<p align="center">
   <img src="./react.png" width="300"/>
</p>

FrontendFrontendFrontendFrontendFrontendFrontend
FrontendFrontendFrontendFrontendFrontendFrontend
FrontendFrontendFrontendFrontendFrontendFrontend
FrontendFrontendFrontendFrontendFrontendFrontend

---

## Backend

<p align="center">
   <img src="./expressss.png" />
</p>

BackendBackendBackendBackendBackendBackendBackend
BackendBackendBackendBackendBackendBackendBackend
BackendBackendBackendBackendBackendBackendBackend
BackendBackendBackendBackendBackendBackendBackend

---

<p align="center">
   <img src="./DevOps.png" width="300"/>
</p>

## App-dev start

Here you can see how to enable the **dev-version** of the **Chat-app**.
1. Exec: ``cd dev``
2. Click on the ``start_dev.command``
   
   > It changes ``ip`` in ``nginx_dev.conf`` on your actual ``ip`` and starts **Nginx** in **Docker-container** with ``nginx_dev.conf``  
   > ***Nginx*** starts on the http://localhost:8085  
   > 
   > ``start_dev.command`` [see here](./dev/start_dev.command).  
   > ``nginx_dev.conf`` [see here](./dev/nginx_dev.conf).
3. Exec: ``cd ..``
4. Now you can start backend:  
   4.1. Exec: ``cd back``   
   4.2. Exec: ``npm i``   
   4.3. Exec: ``npm start``
   
   > It starts back-server with configuration on the ``.env`` and ``nodemon`` on the http://localhost:2501
5. Exec: ``cd ..``
6. Now you can start frontend:  
   6.1. Exec: ``cd front``   
   6.2. Exec: ``npm i``   
   6.3. Exec: ``npm start``
   
   > It starts frontend-server with live-reload on the http://localhost:3000
---


## App-prod start

> :warning: **In development**
