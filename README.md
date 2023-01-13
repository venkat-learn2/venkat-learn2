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
7. IDE : Visual Studio Code [https://code.visualstudio.com/](url)

##  Framework Setup 

### Required Dependencies : 
1. Node JS - Version 14.15.4 - [Download Here](https://lumeltech-my.sharepoint.com/:u:/g/personal/sabareeshr_lumel_com/EcjYqUpf54NNiz1oR3OltdoBDdJUEBQTQxtE8p2ntL2pTA?e=MacduD)
2. Java JDK (Preferably > 1.8 ) version 
3. Allure

After installed the nodejs and Java JDK , set the enviroment variable.

**step 1 :**
 View advanced System -> Environment Variable -> Edit 
 
**step 2 :** 
Refer the Image
![envVar](https://user-images.githubusercontent.com/118034060/212315508-7492a94e-e1da-4a3c-8a53-17f9397c2dff.png)


### Steps to setup 
* Install the required dependency in the machine and set the environment path for the Java and Node JS . 
* Clone the framework from the Git-Repo. 
* Delete the file ./steps.d.ts (if present)
* Use the following npm command to install the dependency 
	> #### npm install 

* Add the `.env` file in the root directory.(for more details reach out automation team)

## codeceptjs.config.js :

* you can set the headless mode here
`const isHeadless = process.env.HEADLESS === 'true'` or `process.env.HEADLESS === 'false'`

* if you want change number of the chunks:

**code example:**

`exports.config = {
  tests: process.env.TESTNAME,
  multiple: {
    parallel: {
      **chunks: 2**,
      browsers: ['chromium']
    }
  }`
  
## Execution Commands : 
`runTest.sh`
>  Used to run the single test case at a time.

`runParallel.sh`
>  Used to run the multiple test cases in **parallel**

**edit .env file as per your needs**

**Execute all the test cases**

Example:

`TESTNAME : 'Tests/ColumnFilter/*.js'`

**note** :here * will be executed all the test cases inside the folder

**Execute all the test cases from the folder and file name start with**

Example:

`TESTNAME : 'Tests/ColumnFilter/COLFIL*.js'`

**Execute single test cases**

 Example:

`TESTNAME: 'Tests/ColumnFilter/COLFIL_01_ColumnFilter_Appears_Readingview.js'`

**All cases with the mentioned tag should be executed**

* we had set the tag name in our scenario we can also run using the tag name 

Example:

`  Scenario('ExampleCase', async ({ I }) => {
   await I.click('//div[@id='example']')
}).tag('@example')`

one test case :
`codeceptjs run --grep '@example'`

multiple test cases:
`codeceptjs run-multiple --grep '@example'`
