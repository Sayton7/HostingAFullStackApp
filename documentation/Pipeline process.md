# Pipeline process:
### The pipeline workflow is setup to deploy the application with the following sequence:

## 1. Build Job:
1. Install Front-End Dependencies.
    * Installs the needed dependencies for the front-end.

2. Install API Dependencies.
    * Installs the needed dependencies for the back-end.

3. Front-End Lint.
    * Checks the front-end code for errors.

4. Front-End Build.
    * Uses angular prebuilt scripts to build the front-end into www folder.
5. API Build.
    * Cleans the www folder if existing, compiling the code from typescript to javascript and finally copying necessary files to www folder.
## 2. Deploy Job:
1. Deploy App
    * This will run both backend and frontend deploymend scripts.
        * Front-End deply script: copies the front-end built folder (www) to the preconfigured S3 bucket on AWS.
        * Back-End deploy script: lists avialable environments, select the preconfigured envidonment, setting up the environment variables which are preset in circleci, moving into the build folder (www) and finally deploying the app using elasticbeanstalk cli.