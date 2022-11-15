The read me for the project
------------------------

Unzip the file in the email , add the folder to the Visual studio workspace.


The project require visual studio , node js 

The process to make a file is 

npm init -y
npm install @wdio/cli
npm wdio cofig for installing the folders 
npx wdio run wdio.conf.js-->run comand


once the zipped file store in the workspace

Go to file -->  add to the folder to the wrokspace  ( Project will in the the Visual studio code)

EasyFund folder (Right click on the top of the folder )---> Run in the terminal-->npx wdio run wdio.conf.js (run command to execute the project)

The run command to run the Project:npx wdio run wdio.conf.js

The three impotant files are:

1) Search.feature---> Cucumber Code

2)simpleSearchPageObject.js---> object file 

3)simpleSearchStepDef.js---> Executing file which calls all the objects and thier action


Config file
-----------
spec: I had set the path of the feature fail, the main js and made only error log to appear .

simpleSearchPageObject.js
------------------------
The geter method and the action are preformedin this file in Simplesearch class


get findCauseXpath()-->Getting the Xpath of the find the cause

get cookeXpath() -->Getting the Xpath of the Cookie appearing in the page

get sBox() --> Getting the Xpath of the Searchtextbox

get dropBox()--> Getting the Xpath of DropBox 

get xpathSubmit()--> Getting the Xpath of Submit

async openUrl() -->  Method for opening the Url in chrome browser

async findCause()--->  Method for clicking the Find a cause

async valueText() -->  Method for getting the Text 

async checkForcause()--> Method for getting the Text and Fixing the 3rd Cause

 async buttonSubmit()--> Method for clicking the Submit after finding the cause

async message()--->Checking for the Url and Displaying the Message

simpleSearchStepDef.js
------------------------

This has the cucmber step definition

A) Given ---->I am on the home page and clicking the Find the cause
  call the following in async mode which are imported from the simpleSearchPageObject.js

SimpleSearch.openUrl();
SimpleSearch.findCause();


B)When----->Enter the search and check in the list
   call the following in async mode which are imported from the simpleSearchPageObject.js

  SimpleSearch.valueText();
  SimpleSearch.checkForcause();
  SimpleSearch.buttonSubmit();


c)Then---->Confirming the Cause exists in the Search results Message
    call the following in async mode which are imported from the simpleSearchPageObject.js

SimpleSearch.message();
