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

* Add the `.env` file and `.npmrc` file . 

## Execution Commands : 
`runTest.sh`
>  Used to run the single test case at a time.

`runParallel.sh`
>  Used to run the multiple test cases in **parallel**

## codeceptjs.config.js :

you can set the headless mode here
`const isHeadless = process.env.HEADLESS === 'true'` or `process.env.HEADLESS === 'false'`

if you want to run all test cases from the folder and file name start with

example :

`exports.config = {
  tests: 'Tests/ColumnFilter/COLFIL*.js'
 }`
here * will be executed all the files starts with COLFIL

if you want to run single test cases from the folder and file name:
example :

`exports.config = {
  tests: 'Tests/ColumnFilter/COLFIL_01_ColumnFilter_Appears_Readingview.js'
 }`

