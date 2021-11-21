<h1 align="center">
  <br>
  <a href="https://fds.icheft.tech"><img src="./logo.png" alt="fds" width="70"></a>
  <br>
  Friends. Do. Sports.
  <br>
</h1>

<h3 align="center">Official Documentation (with Instructions)</h3>
<h4 align="center">IM 3008 Midterm Project Group D</h4>

<p align="center">
  <a href="https://fds.icheft.tech">
    FE 
    <img src="https://shields.io/website?down_color=red&down_message=down&up_color=success&up_message=up&style=flat-square&url=https%3A%2F%2Ffds.icheft.tech"
         alt="website status">
  </a>
   • 
  <a href="https://be.rdogs.dodofk.xyz/docs">
    BE 
    <img src="https://shields.io/website?down_color=red&down_message=down&up_color=success&up_message=up&style=flat-square&url=https%3A%2F%2Fbe.rdogs.dodofk.xyz%2Fdocs"
         alt="website status">
  </a>
   • 
  <a href="http://rdogs-friendz.github.io/fds-docs/yt">
    <img src="https://shields.io/youtube/views/3hgSYxulWd4"
         alt="YouTube Demo">
  </a>
</p>

<p align="center">
    <img src="https://github.com/Buuntu/fastapi-react/raw/master/assets/react-logo.png" height="50"
            alt="react">
    <img src="https://github.com/Buuntu/fastapi-react/raw/master/assets/fastapi-logo.png" height="50"
         alt="fastapi">
    <img src="https://github.com/Buuntu/fastapi-react/raw/master/assets/postgres.png" height="50"
         alt="postgresql">
</p>

## Table of Contents

+ [Introduction](#introduction)
+ [Demo](#demo)
+ [Development](#development)
    + [Frontend](#frontend)
        + [Dev Environment](#dev-environment)
        + [Development](#development-1)
    + [Backend](#backend)
        + [Database Setup](#database-setup)
        + [Test Server Setup](#test-server-setup)
+ [Usage](#usage)

## Introduction <!-- omit in toc -->

**Friends. Do. Sports.** (FDS in short) is an online service platform built for sports events. It provides matching, joining, and bookmarking sports events so that one can find his/her sports buddy whenever needed. 

The scope of this project is now limited to University-wise only due to financial and time constraints. 

## Demo

Our application is deployed at <https://fds.icheft.tech>. Backend can be viewed at <https://be.rdogs.dodofk.xyz/docs> (backup at <https://fdsbe.icheft.tech/docs>). 

We recommend you to run this project by directly going to our site and experience our service yourself. 

#### ‼️ Please visit <https://fds.icheft.tech> · <https://fds.icheft.tech> · <https://fds.icheft.tech> before you test it out locally.

IF, local deployment is still necessary, instructions are shown as follows:

## Development

+ We have set up our [frontend](https://github.com/RDOGS-Friendz/fds-fe) and [backend](https://github.com/RDOGS-Friendz/fds-be) in different repositories. 
+ You can find all the instructions on this page.

### [Frontend](https://github.com/RDOGS-Friendz/fds-fe)

<img src="https://github.com/Buuntu/fastapi-react/raw/master/assets/react-logo.png" height="25"
            alt="react"> 
![](https://shields.io/badge/platform-Linux%20%7C%20macOS-%23989898?style=flat-square) [![](https://shields.io/github/stars/RDOGS-Friendz/fds-fe?style=social)](https://github.com/RDOGS-Friendz/fds-fe/tree/main)

* We have deployed our frontend website on <https://fds.icheft.tech>. No need to run this app on your local environment.
* Please ask the development team for the `.env` file. 

**🔩 For Local Development:**

#### Dev Environment

- OS: macOS / Linux 
- PM: Yarn 
- IDE: Visual Studio Code (recommended)
  - required plugins:
    - [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
    - [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
    - [Prettier ESLint](https://marketplace.visualstudio.com/items?itemName=rvest.vs-code-prettier-eslint)

#### Development 

1. Clone this repository
    ```
    git clone https://github.com/RDOGS-Friendz/fds-fe.git
    ```
2. Open the directory in your favorite text editor (**VS Code** is highly recommended). If you are using VS Code, please make sure you have the mentioned plugins installed.
4. In terminal, use `yarn` to install the [dependencies](package.json).
5. Before you run our app, please [connect to a backend server (either ours or yours)](#connecting-to-our-server)
6. Run `yarn start` to run the app in the development mode. 

##### Connecting to Our Server

You have two options:

1. Please contact us for the `.env` file. Our present data are all stored in our server.
2. If you want to replicate this app, please also consider to clone our [`fds-be` repository](https://github.com/RDOGS-Friendz/fds-be), and follow the instructions there.
  
    In your `.env`, you should put in:

    ```
    REACT_APP_API_ROOT="http://127.0.0.1:8000"
    CHOKIDAR_USEPOLLING=true
    FAST_REFRESH=false
    ```

    That'll do it. 



### [Backend](https://github.com/RDOGS-Friendz/fds-be)

<img src="https://github.com/Buuntu/fastapi-react/raw/master/assets/fastapi-logo.png" height="25"
         alt="fastapi"> <img src="https://github.com/Buuntu/fastapi-react/raw/master/assets/postgres.png" height="25"
         alt="postgresql">
![](https://shields.io/badge/python-v3.9-blue?style=flat-square) [![](https://shields.io/github/stars/RDOGS-Friendz/fds-be?style=social)](https://github.com/RDOGS-Friendz/fds-be/tree/main) 

* We have deployed our backend website on <https://be.rdogs.dodofk.xyz/docs> (backup: <https://fdsbe.icheft.tech/docs>). No need to start the server on your local environment.
* API Brainstorming Documentation can be viewed at <https://hackmd.io/@icheft/S1guJIOBY>
* Please ask the development team for the `.env` file. 

**🪛 For local development:**

Please clone our BE repository first:

```
git clone https://github.com/RDOGS-Friendz/fds-be.git
```
#### Database Setup

There two ways to set up your database.

##### 1. Connect to Our Database (Recommended)

You only have to ask developer to get the `.env` file.

##### 2. Build Your Own Database on Localhost

1. First, import [`schemas.sql`](https://github.com/RDOGS-Friendz/fds-be/blob/main/schemas.sql) to your `postgresql` server

    ```
    psql -U your_user_name -d your_dbname -f schemas.sql
    ```
2. Second, on your `postgresql` cmd
    ```
    # please remember to replace your path
    \COPY location(name) FROM '/path/fds-be/data_collection/location.csv' DELIMITER ',' CSV HEADER;
    \COPY category(name) FROM '/path/fds-be/data_collection/category.csv' DELIMITER ',' CSV HEADER;
    \COPY department(school, department_name) FROM '/path/fds-be/data_collection/department.csv' DELIMITER ',' CSV HEADER;
    ```

    or in your postgresql cmd:

    ```
    \i import_data.sql
    ```
3. Finally, revise `.env` file to connect to your local database.
    ```
    PG_HOST=postgresql://localhost
    PG_PORT=5432
    PG_USERNAME=your_username
    PG_PASSWORD=your_password
    PG_DBNAME=your_dbname
    PG_DBURL=postgresql://your_username:your_password@localhost/your_dbname

    APP_TITLE=Local Backend
    APP_DOCS_URL=/docs
    APP_REDOC_URL=

    JWT_SECRET=
    JWT_ENCODE_ALGORITHM=HS256
    LOGIN_EXPIRE_DAYS=7%
    ```

#### Test Server Setup

After finishing your setups, to run your own test server, please follow the following steps:

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
