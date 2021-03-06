# Microservices with Docker, Flask, and React

[![Build Status](https://travis-ci.org/testdrivenio/testdriven-app-2.3.svg?branch=master)](https://travis-ci.org/testdrivenio/testdriven-app-2.3)

Part 1
In this first part, you'll learn how to quickly spin up a reproducible development environment with Docker to create a RESTful API powered by Python, Postgres, and the Flask web framework. After the app is up and running locally, you'll learn how to deploy it to an Amazon EC2 instance.

Tools and Technologies: Python, Flask, Flask-SQLAlchemy, Flask-Testing, Gunicorn, Nginx, Docker, Docker Compose, Docker Machine, Postgres, Flask Blueprints, Jinja Templates

Part 2
In part 2, we'll add code coverage and continuous integration testing to ensure that each service can be run and tested independently from the whole. Finally, we'll add React along with Jest (a JavaScript test runner) and Enzyme (a testing library designed specifically for React) to the client-side.

Tools and Technologies: Code Coverage with Coverage.py, continuous integration (CI), Node, NPM, Create React App, React, Enzyme, Jest, Axios, Flask-CORS, React forms, Flask Debug Toolbar

Part 3
In part 3, we'll add database migrations along with password hashing in order to implement token-based authentication to the users service with JSON Web Tokens (JWTs). We'll then turn our attention to the client-side and add React Router to the React app to enable client-side routing along with client-side authentication.

Tools and Technologies: Flask-Migrate, Flask-Bcrypt, PyJWT, react-router-dom, Bulma, React Authentication and Authorization

Part 4
In part 4, we'll add end-to-end (e2e) tests with Cypress, form validation to the React app, a Swagger service to document the API, and deal with some tech debt. We'll also set up a staging environment to test on before the app goes into production.

Tools and Technologies: Cypress, Swagger UI

Part 5
In part 5, we'll dive into container orchestration with Amazon ECS as we move our staging and production environments to a more scalable infrastructure. We'll also add Amazon's Elastic Container Registry along with Elastic Load Balancing for load balancing and Relational Database Service (RDS) for data persistence.

Tools and Technologies: AWS, EC2, Elastic Container Registry (ECR), Elastic Container Service (ECS), Elastic Load Balancing (ELB), Application Load Balancer (ALB), Relational Database Service (RDS)

Part 6
In part 6, we'll focus our attention on adding a new Flask service, with two RESTful-resources, to evaluate user-submitted code. Along the way, we'll tie in AWS Lambda and API Gateway and spend a bit of time refactoring React and the end-to-end test suite. Finally, we'll update the staging and production environments on ECS.

Tools and Technologies: AWS Lambda and API Gateway

Part 7
In part 7, we'll refactor the AWS Lambda function to make it dynamic so it can be used with more than one exercise, introduce type checking on the client-side with React PropTypes, and update a number of components. We'll also introduce another new Flask service to manage scores. Again, we'll update the staging and production environments on ECS.

Tools and Technologies: AWS Lambda and ECS, PropTypes, and Flask