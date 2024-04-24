## Preface
It is not a secret that java files have a .java extension

A project has many .java files which can't be executed directly as computers only understand binary language

So, the java compiler (javac) compiles source code into bytecode creating .class files, which are organised into packages

![process](https://github.com/guycalledavinash/maven/assets/90386560/057cc7ec-221e-4cad-acbf-acfa3219d9c2)

To deploy java project, we should package all .class files (bytecode) to JAR file or WAR file

			JAR : Java Archive
			WAR : Web Archive

The standalone java projects are packaged as a JAR file (a stadalone application is where the project runs only on one computer)

The web applications are packaged as a WAR file where multiple users can access a web applications at a time.
## Maven
Maven is an open source build automation software developed by Apache

It is limited to java projects 

Maven can create initial project folder structure 

Typically a java project is not built using java alone, to make things easy, there are other frameworks and libraries involved like springboot, hibernate, kafka, redis, etc

They are called project dependencies which are to be downloaded but thanks to Maven, it does it for us.

Required dependencies are stored in "pom.xml" file where maven downloads them (pom: project object model)

The pom.xml file is created automatically, acts as an input file when we create a maven project 

Maven compiles and packages the project code 

![maven](https://github.com/guycalledavinash/maven/assets/90386560/f265e767-3100-4619-ad7b-f3d9f35baed6)
# Pre-requisite
Since maven is java based, jre & jdk should be installed locally, along with maven of course

Once the installation is done, it is mandatory to set the environment variables for jdk and maven

1. Go to Environment Variables from search bar and click on 'Environvent Variables' option:
   ![1](https://github.com/guycalledavinash/maven/assets/90386560/3e5600dd-ed12-4cce-b3cf-f84e2ee3daf9)

2. Select JAVA_HOME from the system variables, edit that:
   ![2](https://github.com/guycalledavinash/maven/assets/90386560/8ea8e745-7a27-4e42-80f9-b4b0584761ce)

3. Change variable name and value
   ![3](https://github.com/guycalledavinash/maven/assets/90386560/a34b520b-cdb7-4212-8464-781a3d53aadf)

4. Now its time to set the path of bin directory. Select path and click edit:
   ![4](https://github.com/guycalledavinash/maven/assets/90386560/8e13c7e3-b345-41f1-ad8f-cc33d92b2d5d)

5. Click new, add the path of bin directory of jdk
   ![5](https://github.com/guycalledavinash/maven/assets/90386560/f852f5b7-bc1f-4fba-a9d5-d541168acf3f)

6. Open cmd, check the java version to confirm `java -version`
   
7. Download maven from official source, extract and paste in the C drive

8. Set environment variables and path for maven like we did to java

# Maven project:
To create a standalone appliaction:
```
mvn archetype:generate -DgroupId=in.JohnySins -DartifactId=01-Maven-App -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false
```
To create a web application:
```
mvn archetype:generate -DarchetypeArtifactId=maven-archetype-webapp -DgroupId=in.Donaldtrump -DartifactId=01-maven-web-app -DinteractiveMode=false
```
This creates a project folder structure which includes `src` folder and `pom.xml` file like this:

![str](https://github.com/guycalledavinash/maven/assets/90386560/031d931f-846f-4a66-a9dc-086c3c85f985)

Now, to execute commands, make sure to do it where there's pom.xml file, so change `pwd` 

To compile the project, do this from project folder:
```
mvn compile
```
This creates a target folder where multiple .class files are created. 

In production environment there're many .class files, which are to be packaged
```
mvn package
```
All the bytecode is packaged to jar or war files (jar in this case) 
![jar](https://github.com/guycalledavinash/maven/assets/90386560/1943352e-e6a1-4bd2-9a08-9a6f1c07fb84)

This is the outcome:
![jaar](https://github.com/guycalledavinash/maven/assets/90386560/d59da5e0-c20f-47a8-ab16-d7ff8303ba06)
## Maven goals

clean: deletes target folder

compile: compiles source code

test: executes Junit tests (unit test code)

package: packages bitecode to jar or war

install: installs project in repo

deploy: deploys the 

package = compile + test + package

install = compile + test + package + install

deploy = compile + test + package + install + deploy

## Dependencies
Maven will download dependencies using a repository

-There are 3 types of repositories

1) Central Repository

2) Remote Repository

3) Local Repository

Central repository is maintaining by apache organization

Every company will maintain their own remote repository

Local repository is created in the system (Location : C://users/<uname>/.m2)

When the maven goals are executed, the system will search for dependencies, for which it will search in local repo first, if not central. 

In production, remote repositories are used to store artifacts. 

To know more about them, checkout [Nexus Repository](https://github.com/guycalledavinash/nexus-repository) 
