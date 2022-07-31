# Pipeline process:
### The pipeline workflow is setup to deploy the application with the following sequence:

## 1. Build Job:
1. Install Front-End Dependencies.
2. Install API Dependencies.
3. Front-End Lint.
4. Front-End Build.
5. API Build.

## 2. Deploy Job:
1. Deploy App
* This will run both backend and frontend deploymend scripts. Uploading the server files to the pre-configured elasticbeanstalk environment. And uploading the frontend files to the pre-configured S3 bucket.