# Vicroads_Assessment
Framework: selenium-cucumber-java
This framework is created based on Selenium, Cucumber and Java to execute functional UI tests on VicRoads website

Installation (pre-requisites)
JDK 1.8+ (Note: Java class path is set correctly)
Maven (Note:.m2 class path is set correctly)

Eclipse is installed
and all Eclipse Plugins for Maven, Cucumber is also installed

Browser driver (Note: Only chrome browser has been set for executing the tests. Other browsers can be added as enhancements)
Note: if when executing tests, the browser opens up and nothing happens, it’s likely the browser and driver versions mismatch. Make sure to download compatible 
driver version and replace it with the existing one

Downloading project and executing tests:
Fork / Clone repository from here or download zip and set it up in your local workspace.

Run Some Sample Tests
Open terminal (MAC OSX) or command prompt / power shell (for windows OS) and navigate to the project directory type mvn clean test command to run features. With this command it will invoke the default Chrome browser and will execute the tests.
From the feature file: Right click in the feature file and click run

To run specific feature if you have multiple feature files use, mvn test -Dcucumber.options="classpath:features/my_first.feature"
Note: As there is only one feature file in this current project, it has been setup in 'runner class' to be executed by default.

Framework setup: 
This project is setup as a BDD cucumber project, using Maven for build and dependency management, Java for coding the logic and selenium for interacting with the browser
Page Object Model (POM) is utilised here for structuring the project.

The project is divided in to 5 core parts
Pages (Page Objects): This is where all the page classes relevant to the web pages in the project are defined. This is where all the elements and methods relevant to each page are defined. Base Call is the super class for all the pages
Features: This is where the features are defined
Step Definitions: This is where the logic for executing the features will reside. 
Runner Class: Here we can define the various parameters for features execution
Utility: This class will contain any generic methods that will be used in the project
