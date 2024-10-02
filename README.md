# CapstoneProject-DevOps-CICDpipeline Group 1
_______________________________________________________________________________________
## Company Profile
SKVJ is a traditional company that specializes in  office. 
_______________________________________________________________________________________
## The Team Consist of:
- VVenila
- Kerenp
- Jyoti
- Saravanan.B
_______________________________________________________________________________________
## Getting started

To host a simple HTML enquiry form to collect customer details and triggers a lambda function to send an email using AWS SES with the customer details. 

_______________________________________________________________________________________
## Tools and Technologies used:

- npm
- AWS S3 bucket
- Snyk
- Terraform
- ECR
- ECS
- Route 53
- Lambda
- SES
- Serverless
- Docker
_______________________________________________________________________________________
## Explanation of CICD Workflow

**on: pull_request & push:** The workflow is triggered by pull requests and push events on the dev and main branches.
jobs:

**test:** This job runs tests to ensure the code is ready for deployment. It installs dependencies and executes the test suite.

**deploy-staging:** This job is triggered when the dev branch is updated. If the tests pass, the application is deployed to the staging environment.

**deploy-production:** This job is triggered when the main branch is updated, deploying the application to production after passing tests.

### Branch Permissions
To enforce branch protection, you can configure GitHub branch protection rules:

**Main Branch (main):**

Require status checks (tests) to pass before merging.
Require PR approval (at least one reviewer).
Prevent direct pushes to the branch.

**Development Branch (dev):**

Similar restrictions as the main branch.
Use required status checks for running tests.
You can configure these protections in the repository's Settings Branches.

### Deploy Scripts

For the actual deployment to staging or production, you can add SSH or cloud deployment commands (e.g., AWS CLI, GCP CLI, etc.) depending on your infrastructure.






:-) Happy Coding !