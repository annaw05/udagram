# Hosting a Full-Stack Application

Task: learn how to take a newly developed Full-Stack application built for a retailer and deploy it to a cloud service provider so that it is available to customers. 

## Udagram Overview

The project application, Udagram - an Image Filtering application, allows users to register and log into a web client, post photos to the feed, and process photos using an image filtering service. 

It has two components:
- Frontend - Angular web application built with Ionic framework
- Backend RESTful API - Node-Typescript application

This application was used as starter project to deploy an existing NodeJS application to AWS cloud. 


## Dependencies

```
- Node v14.15.5 (LTS) or more recent. While older versions can work it is advisable to keep node to latest LTS version

- npm 6.14.11 (LTS) or more recent, Yarn can work but was not tested for this project

- AWS CLI v2, v1 can work but was not tested for this project

- A RDS database running Postgres.

- A S3 bucket for hosting uploaded pictures.

- A Elastic Beanstalk for backend API.

- CircleCi pipeline to achieve continuous integration and continuous deployment.

```

## Links

1. S3:  [https://udagram284361803578.s3-website-us-east-1.amazonaws.com/](https://udagram284361803578.s3-website-us-east-1.amazonaws.com/)
1. EB: [https://udagram-api-dev22222222222222.us-east-1.elasticbeanstalk.com/api/v0/feed](https://udagram-api-dev22222222222222.us-east-1.elasticbeanstalk.com/api/v0/feed)

## Screenshots


## Built With

- [Angular](https://angular.io/) - Single Page Application Framework
- [Node](https://nodejs.org) - Javascript Runtime
- [Express](https://expressjs.com/) - Javascript API Framework

## License

[License](LICENSE.txt)
