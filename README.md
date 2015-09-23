# WikiaTest
#Initial Setup
Open Eclipse
Install TestNG Framework
Import the Project in Eclipse
#To Create Selenium Grid Hub and Node
Create a folder Lib on your local drive
Copy selenium-server-standalone-2.47.1.jar and chromedriver.exe in that folder
Open Command prompt on the lib folder and give the following command to initialize the hub : java -jar selenium-server-standalone-2.47.1.jar -role hub
Open aother Command prompt on the lib folder and give the following command to initialize the hub : java -Dwebdriver.chrome.driver=chromedriver.exe -jar  selenium-server-standalone-2.47.1.jar -role node -hub  http://localhost:4444/grid/register-browser browserName=chrome
#TestCase1
Launch Firefox browser, 
open the http://qm-homework.wikia.com site,
go to Sign In and login with valid credentials
#Creating TestCase2
Launch Chrome browser, 
open the http://qm-homework.wikia.com site, 
go to Sign In and login with valid credentials,
Click on the contibute button and select Add a Video, 
type video URL an add the video.
#Running the Test Suite
Save the Project.
Browser can be specified within the class : capability.setBrowserName("chrome");//Only chrome and firefox are supported.
Right click on Project and go to TestNG>Convert to TestNG.
It will create the TestNG.xml file.
Run the TestNG.xml as TestNG Suite
