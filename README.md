# Postman API Automation Integration with Github Actions #
This repository is a demonstration for POC for integrating postman
tests with github actions.
The Tests are written in Postman and they are executed on the VM with the help of newman and newman-reporter-htmlextra.
Github Actions will trigger the project execution on every push to the main branch. You can also execute the project manually using workflow_dispatch. The Projects runs on a scheduled time with the help of the cron job
The HTML report is archieved and kept in the artifact section for the team to download it. Along with that they can view the report directly from the github page: [https://jatin99.github.io/Phoenix-Inwarranty-Flow/](https://narkaromkar.github.io/Phoenix-Inwarranty-flow/).
The latest report is mailed to the team members using GMAIL SMTP.

## Tech Stack ##
1. Postman
2. Nodejs 22v
3. Newman
4. Newman-Reporter-Htmlextra
Github Actions
6. Gmail SMTP
7. Github Pages
8. CSV for Data Driven Testing
9. AWS-EC2 instance for Self hosted github runner.

## Github Pages ##
You can directly view the latest test report of the Postman Test at the Github Page Link: https://narkaromkar.github.io/Phoenix-Inwarranty-flow/

## How to run the Project? #F
You can run the project on your local system for that:
1. Clone the Project on Local System: https://github.com/narkaromkar/Phoenix-Inwarranty-flow.git
2. Install Nodejs and NPM from https://nodejs.org/en
3. Install Newman using np install -g newman
4. Install Newman-reporter-htmlextra npm install -g newman-reporter-htmlextra
5. Run the Newman Command:

   ```
             newman run "Inwarranty-flow Collection.postman_collection.json
             -e QA-postman_environment.json \
             -d testdata. csv \
             -r cli, htmlextra
             --reporter-htmlextra-export ./newman/index.html
   ```
## HTML report ##
Below report would be created in newman folder and can be access via github or email

   <img width="1196" height="932" alt="image" src="https://github.com/user-attachments/assets/34b67d63-a1e2-4631-808b-28f9805b2c98" />

## Testing Coverage ##

Happy Flow Testing
Negative Testing and Edge Case Testing
Token Testing
Data Driven Testing with CSV
Schema Validation
Secrets Management with Github Secrets

## Project Structure ##
```
Phoenix Inwarranty Flow Collection
  ├─ In Warrenty Flow.postman_collection.json
  ├─ DEV.postman_environment.json
  └─ test data.csv
```
