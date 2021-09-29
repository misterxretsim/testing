Chat-app
=============================


- [Docker](#Docker)
- [Nginx](#Nginx)
- [DataBase](#DataBase)
- [API-info(Swagger)](#API\-info)
- [Frontend](#Frontend)
- [Backend](#Backend)
- [App-dev start](#App\-dev-start)
- [App-prom start](#App\-prom-start)

---

## Docker

On the first you need [docker](https://www.docker.com).

My app uses docker for starting [Nginx-server](https://hub.docker.com/_/nginx).
This is needed to connect the [Frontend](./front) and the [Backend](./back) on the develop version app.
Also It's needed for delivery [Frontend](./front) to the Browser-client for the production version, and respectively for forwarding requests on the [Backend](./back).

Therefore you need docker-client.

---

## Nginx

NginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginx
NginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginx
NginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginx
NginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginx
NginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginx
NginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginx
NginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginx
NginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginxNginx

---

## DataBase

Also you need a DataBase.

---

## API-info

You can see server API on the http://localhost:2501/api-docs/

>Created with <b><i>Swagger</i></b>


---

## Frontend

FrontendFrontendFrontendFrontendFrontendFrontend
FrontendFrontendFrontendFrontendFrontendFrontend
FrontendFrontendFrontendFrontendFrontendFrontend
FrontendFrontendFrontendFrontendFrontendFrontend


---

## Backend

BackendBackendBackendBackendBackendBackendBackend
BackendBackendBackendBackendBackendBackendBackend
BackendBackendBackendBackendBackendBackendBackend
BackendBackendBackendBackendBackendBackendBackend

---

## App-dev start


1. Exec: ``cd dev``
2. Click on the ``start_dev.command``

    >It changes ``ip`` in ``nginx.conf`` on your actual ``ip`` and starts <b><i>Nginx</i></b> in docker-container with ``nginx.conf``
    >
    ><b><i>Nginx</i></b> starts on the http://localhost:8085

3. Exec: ``cd ..``
4. Now you can start backend:
    4.1. Exec: ``cd back``   
    4.2. Exec: ``npm i``   
    4.3. Exec: ``npm start``

    >It starts back-server with configuration on the ``.env`` and ``nodemon`` on the http://localhost:2501

5. Exec: ``cd ..``
6. Now you can start frontend:
    6.1. Exec: ``cd front``   
    6.2. Exec: ``npm i``   
    6.3. Exec: ``npm start``

    >It starts frontend-server with live-reload on the http://localhost:3000

---

## App-prom start
