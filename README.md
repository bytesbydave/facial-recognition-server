# Facial Recognition App

The Facial Recognition App uses the Clarifai API to locate a face on a picture. It also keeps track of the amount of entries the user has searched. This project uses React on the frontend. The backend API uses Node.js, Express.js, and Postgres. Designs are done with Semantic UI and custom CSS. The purpose of this application was to gain familiarity with using Node on the backend. 

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development. 

### Installing

Run the following to install on your local environment


Clone the repo
```
git clone https://github.com/dvdlin214/facial-recognition-server.git
```


Install packages
```
npm install
```

Create and connect a postgres database in the server.js file

Create user and login tables
```
CREATE TABLE users (id SERIAL PRIMARY KEY, name VARCHAR(100), email TEXT UNIQUE NOT NULL, entries BIGINT DEFAULT 0, joined TIMESTAMP NOT NULL );
```
```
CREATE TABLE login ( id serial PRIMARY KEY, hash varchar(100) NOT NULL, email text UNIQUE NOT NULL);
```


Run the app
```
npm start
```

## Built With

### NPM Packages
- bcrypt
- postgresql
- knex
- body parser
- cors
- express

### APIs
- [Clarifai](https://www.clarifai.com/)

