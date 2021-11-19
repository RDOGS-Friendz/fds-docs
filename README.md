# Friends. Do. Sports. Documentation


![](https://shields.io/website?down_color=red&down_message=down&up_color=success&up_message=up&style=flat-square&url=https%3A%2F%2Ffds.icheft.tech) ![](https://shields.io/badge/views-31k-red?logo=youtube&style=social)

+ [Introduction](#introduction)
+ [Demo](#demo)
+ [Development](#development)
    + [Frontend](#frontend)
    + [Backend](#backend)
        + [Database Setup](#database-setup)
        + [Test Server Setup](#test-server-setup)
+ [Usage](#usage)

## Introduction

**Friends. Do. Sports.** (FDS in short) is an online service platform built for sports events. It provides matching, joining, and bookmarking sports events so that one can find his/her sports buddy whenever needed. 

The scope of this project is now limited to University-wise only due to financial and time constraints. 

## Demo

Our application is deployed at <https://fds.icheft.tech>. Backend can be viewed at <https://fdsbe.icheft.tech/docs> (backup at <https://be.rdogs.dodofk.xyz/docs>). 

We recommend you to run this project by directly going to our site and experience our service yourself. 

#### Please visit <https://fds.icheft.tech> · <https://fds.icheft.tech> · <https://fds.icheft.tech> before you test it out locally.

IF, local deployment is still necessary,

## Development

### Frontend
![](https://shields.io/badge/platform-Linux%20%7C%20macOS-%23989898?style=flat-square) ![](https://shields.io/badge/Stars-2-lightgrey?logo=github&style=social) ![](https://shields.io/badge/node-%3E%3D%206.0.0-brightgreen?style=flat-square)

### Backend

![](https://shields.io/badge/Stars-2-lightgrey?logo=github&style=social) ![](https://shields.io/badge/python-v3.9-blue?style=flat-square)

* We have deployed our backend website on <https://fdsbe.icheft.tech/docs> (backup: <https://be.rdogs.dodofk.xyz/docs>). No need to start the server on your local environment.
* API Brainstorming Documentation can be viewed at <https://hackmd.io/@icheft/S1guJIOBY>
* Please ask develop team to get .env file. 


#### Database Setup

There two ways to set up your database.

##### 1. Connect to Our Database (Recommended)

You only have to ask developer to get the `.env` file.

##### 2. Build Your Own Database on Localhost

1. First, import `schemas.sql` to your `postgresql` server
2. Second, on your `postgresql` cmd
    ```
    # please remember to replace your path
    \COPY location(name) FROM '/path/fds-be/data_collection/location.csv' DELIMITER ',' CSV HEADER;
    \COPY category(name) FROM '/path/fds-be/data_collection/category.csv' DELIMITER ',' CSV HEADER;
    \COPY department(school, department_name) FROM '/path/fds-be/data_collection/department.csv' DELIMITER ',' CSV HEADER;
    ```
3. Finally, revise `.env` file to connect to your local database.
    ```
    PG_HOST=
    PG_PORT=5432
    PG_USERNAME=
    PG_PASSWORD=
    PG_DBNAME=
    PG_DBURL=

    APP_TITLE=FDS Backend
    APP_DOCS_URL=/docs
    APP_REDOC_URL=

    JWT_SECRET=
    JWT_ENCODE_ALGORITHM=HS256
    LOGIN_EXPIRE_DAYS=7%
    ```

#### Test Server Setup

##### 1. Requirements: Create a `python` virtual environment

You have **three** options:

1. with `conda`
    ```shell
    conda create --name <env_name> python=3.9
    conda activate <env_name>
    ```
2. with `venv`
    ```shell
    python3 -m venv <env_name>
    ./<env_name>/Scripts/activate
    ```
3. or with `pipenv` (faster and lighter)

    ```shell
    pip install pipenv
    pipenv shell
    ```

##### 2. Set up your Environment

```shell
pip install -r requirements.txt
copy .env.example .env
```

Or on Unix-based system, run

```shell
pip install -r requirements.txt
cp .env.example .env
```

Then fill out the environment variables in `.env`

##### 3. Start the server

```shell
pip install uvicorn
uvicorn main:app
```

On your terminal you should see:

```
INFO:     Uvicorn running on http://127.0.0.1:8000 (Press CTRL+C to quit)
INFO:     Started reloader process xxxx using watchgod
INFO:     Started server process xxxx
INFO:     Waiting for application startup.
INFO:     Application startup complete.
```
Now you can go to `http://127.0.0.1:8000` and test it.  
You may also turn up the auto-reload option, or change the host & port with `--host` and `--port`:
```shell
uvicorn main:app --reload --host 0.0.0.0 --port 80
```


## Usage