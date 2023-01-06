# Infrastracture description
The diagram Includes the different AWS services used for hosting the API, Frontend, and the DB. 
![infrastructure-diagram](/documents/infrastracture.png)
## Elastic Beanstalk: hosting Backend API
- hosts backend RESTful API - Node-Typescript application
- use a web server that to serve HTML files
- platform Node.js 14

## S3: hosting frontend application
- hosts Frontend - Angular web application built with Ionic framework
- web hosting: serve static files 

## RDS: Database to store the application data
- RDS (or Relational Database Service) is a service that aids in the administration and management of databases.
- Database Engine: PostgreSQL 12
- public

