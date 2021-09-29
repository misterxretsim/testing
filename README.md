For start dev-version
=============================


- [Docker](#Docker)
- [DataBase](#DataBase)
- [API-info](#API\-info)
- [App start](#App-start)

* [On the first you need docker](#Docker)
* [Also you need a DataBase](#DataBase)
* [API-info here](#API-info)
* [Then follow the steps:](#App start)

---

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


## You can see server API on the http://localhost:2501/api-docs/

---

Created with <b><i>Swagger</i></b>

---

# Docker

# DataBase

# API-info

# App start
