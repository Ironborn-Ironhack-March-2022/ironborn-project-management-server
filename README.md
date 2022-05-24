# Project Management REST API


## About

REST API for a project management app. Built in Express + MongoDB.

- This repo implements the the server (REST API).
- A repository for with the client (React App) can be found here: https://github.com/Ironborn-Ironhack-March-2022/ironborn-project-management-client 



## Instructions

To run in your computer, follow these steps:
- clone 
- install dependencies: `npm install`
- create a `.env` file with the following environment variables
  - ORIGIN, with the location of your frontend app (example, `ORIGIN=https://mycoolapp.netlify.com`)
  - TOKEN_SECRET: used to sign auth tokens (example, `TOKEN_SECRET=ilovepizza`)
- run the application: `npm run dev` or `npm start`


## API Endpoints

<br/>

**Auth endpoints**

| HTTP verb   | Path | Request Headers | Request body  | Description |
| ------------- | ------------- | ------------- |------------- | ------------- |
| POST  | /api/auth/signup  | –  | { email: String, password: String }  | Create an account  |
| POST  | /api/auth/login  | –  | { email: String, password: String }  | Login  |
| GET  | /api/auth/verify  | Authorization: Bearer `<jwt>`  | –  | Verify jwt  |


<br/>

**Other endpoints**

| HTTP verb   | Path | Request Headers | Request body  | Description |
| ------------- | ------------- | ------------- |------------- | ------------- |
| POST  | /api/projects  | Authorization: Bearer `<jwt>`  | { title: String, description: String }  | Create new project  |
| GET  | /api/projects  | –  | –  | Get all projects  |
| GET  | /api/projects/:projectId  | –  | – | Get project details  |
| PUT  | /api/projects/:projectId  | Authorization: Bearer `<jwt>`  | { title: String, description: String, tasks: Array }  | Update a project  |
| DELETE  | /api/projects/:projectId  | Authorization: Bearer `<jwt>`  | – | Delete a project  |


## Demo

A demo of the REST API can be found here: https://ironborn-project-management.herokuapp.com/api/

