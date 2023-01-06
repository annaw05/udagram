# Pipeline description
using CircleCI 

## Configuration file
.circleci/config.yml

### orbs
configuring pipeline

instruct the server to setup below software on the server
```
node: circleci/node@5.0.2
eb: circleci/aws-elastic-beanstalk@2.0.1
aws-cli: circleci/aws-cli@3.1.1
```

### jobs
commands which will run to install, build and deploy the application.


```
jobs:
  build:
    docker:
      - image: "cimg/node:14.15"
    steps:
      - node/install:
          node-version: '14.15'         
      - checkout
      - run:
          name: Install Front-End Dependencies
          command: |
            npm run frontend:install    
      - run:
          name: Install API Dependencies
          command: |
           npm run api:install
      - run:
          name: Front-End Build
          command: |
            echo "TODO: Build the frontend app"
            npm run frontend:build
      ....
  deploy:
    docker:
      - image: "cimg/base:stable"
    steps:
      - node/install:
          node-version: '14.15' 
      - eb/setup
      - aws-cli/setup
      - checkout
      - run:
          name: Deploy App
          command: |
             npm run deploy
```

### workflows
 instructions about the order of the jobs

 first run build, wait for approval, then run deploy
```
 workflows:
  udagram:
    jobs:
      - build
      - hold:
          filters:
            branches:
              only:
                - master
          type: approval
          requires:
            - build
      - deploy:
          requires:
            - hold
```