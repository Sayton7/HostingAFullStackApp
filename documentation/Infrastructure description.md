# Infrastructure description

## The application is consists of three main components:

* Database: A Postgres database that stores the data of the application.

* Back-End: A server that uses Express and node js to provide an API to handle the requests performed on the client side.

* Front-End: A client side application that uses Angular to handle user requests and get the data from the server.

# Application Deployment

## The application is deployed using AWS services as follows:

* Database: Will be hosed on RDS database running Postgres.

* Back-End: Will be hosed on Elastic Beanstalk server running Node.js.

* Front-End: Will be hosed on S3 bucket that will host the uploaded files.
