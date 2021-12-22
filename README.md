# DevOps Project - 2021

This project consists in 8 tasks that aim at using the devOps tools discovered during lab sessions over the fall semester.                            
For this project, we created one branch for each feature that we were asked to implement (except for Docker and Docker-compose which were done on the same branch). WHen the feature was working and the development wass finished, we would merge it into the main branch and base each new branch created on the main (as it was the "working" and "clean" one).


## Usage

*how to start and use the application, run the tests, ...*

* Clone this repository, from your local machine:
  ```
  git clone https://github.com/laure-a/audouy-poulain-devops.git devops-project
  cd devops-project
  ```
* Go to folder iac (cd iac)

  If you need to install vagrant guest additions for virtual box:
  ```
  vagrant plugin install vagrant-vbguest
  ```
  To create or start your VM, run the command:
  ```
  vagrant up
  ```
  You can access the web application at : 20.20.20.2:3000
  
*rajouter toutes les infos nécessaires pour installer les logiciels, les commandes pour lancer, etc*

## Authors

This project was carried out by:
* Laure AUDOUY: laure.audouy@edu.ece.fr
* Thomas POULAIN: thomas.poulain@edu.ece.fr        
                                                                                                                                                          
*Group 3 - SI Inter*

## Features

### 1. Enriched web application with automated tests	
For this part, we used the draft application located in the lab4 folder (continuois testing), and we enriched it by completing the sections that were marked "TO DO". This web application displays a message at localhost:3000, "Hello world!" and we implemented a few tests/completed the given code in the userapi folder of our project. You can see on the screenshot below that all tests work fine.  

![Userapi tests](images/userapi.png)

### 2. Continuous Integration and Continuous Delivery (and Deployment)
We used GitHub Actions for CI and Heroku for CD. However, Heroku deployment platform required credit card information to use their database service. Therefore, we were not able to use it, but our application still is deployed and displays the Hello world message on the web page. You can find the related code in the .github folder of our project.
* GitHub Actions
We followed the steps indicated in the CI/CD lab. We created a workflow:

![workflow](images/workflow.png)

After creating our workflow (see hidden folder .githbub in our project), we made some tests by creating a pull request for merging the CI/CD branch into the main (as our CI checks are conducted when merging code into the main branch). You might see this, but we did not merge every pull request as we had some unsuccessful try outs at first (we also wanted to finish the CD part before merging the branch).

![CI](images/ci.png)

* Deployment with Heroku

To deploy our app, we added some commands in our workflow and created an Heroku account. We ran our code and deployed our app to Heroku by following the lab steps (+ tests with github pull requests). We can see on the picture below that our project is present on the Heroku platform:

![Heroku](images/heroku.png)

Also, our web app can be accessed via this link (which we get by clicking on the "open app" button on Heroku:
https://project-audouy-poulain.herokuapp.com/
And here is a screenshot of what is displayed: this is our app, we do get the same result as when running our app locally on localhost:3000 with "npm start".

![Deployment](images/deployment.png)

Finally, we created one last pull request for merging our ci-cd branch into the main branch and got the following successful results: 

![Final workflow](images/workflowTest.png)

### 3. Infrastructure as code using Ansible
### 4. Containerisation with Docker
### 5. Orchestration with Docker Compose
### 6. Orchestration with Kubernetes
### 7. Service mesh using Istio
### 8. Monitoring

