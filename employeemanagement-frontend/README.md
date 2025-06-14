----------------------------------------   frontend ------------------------------------------------------
### connect to frontend instance install below dependencies 
```
sudo apt-get update 
#Install Java 17
sudo apt install openjdk-17-jdk openjdk-17-jre -y
#Install Nodejs
curl -fsSL https://deb.nodesource.com/setup_current.x | sudo -E bash - &&\
sudo apt-get install -y nodejs 
sudo ufw allow 3000
sudo ufw allow 22    #allow incoming traffic on SSH
 ```
-------------------- clone the git repo in frontend and update the backend server details------------------
```
git clone https://github.com/CloudTechDevOps/fullstack-employee-application.git

cd fullstack-employee-application/employeemanagement-frontend
cd src/service
vi EmployeeService.js
### update the  backend public ip value here

const BASE_URL = "http://52.87.237.51:8080/employee";

#BUILD FrontEnd APP gi to frontned directory then install and start 
cd ../../
npm install

nohup npm start > app.log 2>&1 &
```
----------------frontend part is completed -----------------------------------
