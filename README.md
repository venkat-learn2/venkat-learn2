# Codecept JS - Playwright helper Framework 

## Important Links : 
[Framework Documentation Link](https://codecept.io/helpers/Playwright/)

## Framework Details : 
1. Framework Used : Codecept JS
2. Automation Tool : Playwright
3. Language : Javascript
4. Reporting Tool : Allure 
5. Logging Tool : Log4js
6. Assertions Tool : Codecept JS Assert Library 

##  Framework Setup 

### Required Dependencies : 
1. Node JS - Version 14.15.4 - [Download Here](https://lumeltech-my.sharepoint.com/:u:/g/personal/sabareeshr_lumel_com/EcjYqUpf54NNiz1oR3OltdoBDdJUEBQTQxtE8p2ntL2pTA?e=MacduD)
2. Java JDK (Preferably > 1.8 ) version 

### Steps to setup 
* Install the required dependency in the machine and set the environment path for the Java and Node JS . 
* Clone the framework from the Git-Repo. 
* Delete the file ./steps.d.ts (if present)
* Use the following npm command to install the dependency 
	> #### npm install 


* Replace the contents in directory `./node_modules/codeceptjs/ ` with the [this codecept js contents](https://lumeltech-my.sharepoint.com/:f:/g/personal/sabareeshr_lumel_com/EjRNN5-xBMRJpMhcx0wsrPsBtOJSjJsjsSdHnmwSmCwKKQ?e=NA6X7L)
* Add the `.env` file and `.npmrc` file . 

## Execution Commands : 
`npx codeceptjs run --steps --plugins allure`
>  Used to run the test cases in **sequence**

`npx codeceptjs run-multiple --steps --all --plugins allure`
>  Used to run the test cases in **parallel **

` allure serve output/allure-results`
>Used to create an **allure report** in Temp Directory 

`rm -r output`
>Used to remove **output** directory
