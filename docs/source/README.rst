**README**
==========


## Requirements

- Docker
- python3 (=> 3.6 version)
- pip command
- Flask Framework
- Vue and Node Js
- Dart and Flutter

## Setup

First, You need to install `Docker <https://hub.docker.com/search?offering=community&q=&type=edition&operating_system=linux%2Cwindows%2Cmac>`_

Then run the command below in the root directory:

```sh
docker-compose up --build or docker-compose up -d
```

## Back-end

#### API description

Architecture

.

├── about.json

├── app.json

├── app.py

├── creds.json

├── docker-compose.yml

├── DockerfileNginx

├── DockerfilePython

├── img

├── LICENSE

├── nginx.conf

├── Procfile

├── readme.md

├── requirements.txt

├── routes

│   ├── about.py

│   ├── auth_code.html

│   ├── auth.py

│   ├── connect_oauth2.py

│   ├── github

│   │   ├── get_repositorie.py

│   ├── global_var.py

│   ├── gmail.py

│   ├── oauth2_callback.py

│   ├── oauth2_function.py

│   ├── required_packages.py

│   ├── send_mail.py

│   └── service.py

├── static

│   └── swagger.json

├── swagger.png

├── tests

│   └── app_test.py

└── unit_test.py

API used is Flask. To run manually Flask: 

```bash
cd Back-end
pip install -r requirements.txt
python3 app.py
```

- #### Swagger UI

![swagger.png](swagger.png)

Hosted Locally
http://127.0.0.1:8080/swagger/

It's composed of three parts:

* [x]  Authentification requests
   
    Authentification requests includes registration, login, account confirmation, registration or login with google and logout

* [x]  Google Authentification

    Includes login via google and requests for Drive and Gmail

* [x]  Services 
    Services Include all the services we need for developing AREA project

When you run the docker command, it runs the APi, the web and mobile parts.


## Frontend : Web and Mobile

#### WEB : Vue js
Architecture
.

├── assets

├── client.apk

├── DockerfileNpm

├── index.html

├── package.json

├── playwright.config.js

├── public

│   └── favicon.ico

├── README.md

├── src

│   ├── App.vue

│   ├── assets

│   ├── components

│   │   ├── Footer.vue

│   │   ├── Header.vue

│   │   ├── icons

│   ├── main.js

│   ├── router

│   │   └── index.js

│   ├── stores

│   │   └── counter.js

│   └── views

│       ├── AboutView.vue

│       ├── callback

│       │   └── github.vue

│       ├── Dashboard.vue

│       ├── Google_auth.vue

│       ├── Google_request.vue

│       ├── HomeView.vue

│       ├── link_connect.vue

│       ├── Login.vue

│       ├── Profile.vue

│       ├── Register.vue

│       └── verified_account.vue

└── vite.config.js

- The **public** directory contains public files that are accessible by the application, such as the index.html.
- The **src** directory contains the source code of the application.
- The **assets** directory contains files such as images and fonts used in the application.
- The **components** directory contains reusable components of the application.
- The **views** directory contains views which are the pages of the application.
- The **App.vue** file is the root component of the application and defines the general structure of the user interface.
- The **main.js** file is the entry point of the application and configures Vue.js to use components and views.
- The **package.json** file defines the project dependencies and npm scripts used to run and build the application.

To run manually the web :

.. code-block:: console

$ cd frontend/area-frontend-web
$ npm install
$ npm run dev


The web url: http://172.18.0.1:8081/

It must display like this:

![web.png](web.png)

#### MOBILE : Dart and Flutter

To run manually the mobile :

Make sur to connect your phone before continue

```
cd frontend/area-frontend-mobile/area_mobile
flutter pub get
flutter run
```

It must display like this:

![mob_1.jpeg](mob_1.jpeg)
![mob_2.jpeg](mob_2.jpeg)
![mob_3.jpeg](mob_3.jpeg)
![mob_4.jpeg](mob_4.jpeg)