# Postman API Automation Integration with Github Action #

The repository is a demostration for POC for integarting the postman with Github Action. The tests are written in poatman and executed in VM with help of newman and newman -reporter-htmlextra.
 GithubAction will trigger the project exection on every push to main branch. you can also execute project manually using workflow_dispatch project will execute on scheldule time with help of CRON job.

 The HTML report archived and kept in the artifacts for the team to download it.along with that they can view the report directly from github page : https://gayathiri758.github.io/Phonenix-Inwarranty-flow/
 The latest report is mailed to the team members using gmail, SMTP.
 
 ## Tech Track ##
 1.postman
 2.node js
 3.newman
 4.Newman-Report-HTMLExtra
 5.Github Action
 6.Gmail SMTP
 7.Github PAges
 8.CSV data
 9.AWS EC2 instance for selfhosted Github Runner

 ## Github Action ##
 You can directly view the latest report of postman at github page link: https://github.com/gayathiri758/Phonenix-Inwarranty-flow

 ## How to run the Project? ##
 you can run the project on your Local system for that:
 1.clone the project on local system : https://github.com/gayathiri758/Phonenix-Inwarranty-flow
 2.Install Node JS and NPM : https://www.npmjs.com/
 3.Install Newman using npm install -g newman
 4. Install Newman-reporter-htmlextra npm install -g newman-reporter-htmlextra
 5.Run the Newman Command
    ```
    newman run 'Inwarranty-flow Collection.postman_collection.json' \
          -e QA.postman_environment.json \
             testData.csv \
          -r cli,htmlextra \
          --reporter-htmlextra-export ./newman/index.html
    ```

## HTML Report ##
The Report will created in the newman folder

## Project Structure ##
```
Phoenix Inwarranty Flow Collection
├─ Inwarranty-flow Collection.postman_collection.json # collection file
├─ QA.postman_environment.json # environment file
└─ testData.csv # data driven file

```
