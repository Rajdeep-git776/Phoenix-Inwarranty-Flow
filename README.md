# Postman API Automation integration with GitHub Actions #

This repository is a demonstration for POC for integrating postman wih Github Action. The test are written using postman and will be running in VM with newman and newman-reporter-htmlextra.
Github Action will trigger the execution automatically on trigger on the main branch. You can also execute the project using workflow dispatch. The project runs on a scheduled time with the help of cron jobs.

The HTML Report is archived and is kept in the artifact section for the team to download.  Along with that they can view the report directly from GitHub Pages: https://rajdeep-git776.github.io/Phoenix-Inwarranty-Flow/

The latest report is mailed to the Team Members using SMTP.

## Testing Coverage ##
1. Positive Testing
2. Data driven Testing
3. Schema Validation
4. Negative Testing
5. Token Testing


## Tech Stack ##
1. Postman
2. Newman
3. Newman-reporter-htmlextra
4. node.js 22v
5. GitHub Actions
6. Gmail SMTP
7. GitHub Pages
8. CSV for data driven testing
9. AWS-EC2 instance for self hosted GitHub Runner

## GitHub Pages ##
You can directly view the latest test report of postman test at the GitHub Page: 
```
https://rajdeep-git776.github.io/Phoenix-Inwarranty-Flow/
```

![Postman Report](https://github.com/Rajdeep-git776/Phoenix-Inwarranty-Flow/blob/static-page/HTML_report.png)

## How to run the project ##
You can run the project on your local system for that:
1. Clone the project on local system: https://github.com/Rajdeep-git776/Phoenix-Inwarranty-Flow.git
2. Install node.js and npm from: https://nodejs.org/en/download
3. Install newman using npm install -g newman
4. Install newman-reporter-htmlextra using npm install -g newman-reporter-htmlextra
5. Run the command using:

   ```
         newman run 'Inwarranty-flow Collection.postman_collection.json' \
             -e QA.postman_environment.json \
             -d testdata.csv \
             -r cli,htmlextra \
             --reporter-htmlextra-export ./newman/index.html
   ```

## HTML Report ##
The HTML Report will be created in the newman folder

## Project Structure ##

```
Phoenix Inwarranty Flow Collection
├─ Inwarranty-flow Collection.postman_collection.json
├─ QA.postman_environment.json
└─ testData.csv

```


