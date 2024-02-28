## Preface
It is not a secret that java files have a .java extension

A project has many .java files which can't be executed directly as computers only understand binary language

So, the java compiler (javac) compiles source code into bytecode creating .class files

Those .class files are organised into packages

To deploy java project, we should package all .class files as JAR file or WAR file

			JAR : Java Archive
			WAR : Web Archive

The standalone java projects are packaged as a JAR file (a stadalone application is where the project runs only on one computer)

The web applications are packaged as a WAR file where multiple users can access a web applications at a time.
## Maven
Maven is an open source build automation software developed by Apache

It is limited to java projects 

Maven can create initial project folder structure 

Typically a java project is not built using java alone, to make things easy, there are other frameworks and libraries involved like springboot, hibernate, kafka, redis, etc

They are called project dependencieswhich are to be downloaded but thanks to Maven, it does it for us.

Required dependencies are stored in "pom.xml" file where maven downloads them (pom: project object model)

The pom.xml file is created automatically, acts as an input file when we create a maven project 

Maven can compile and package the project
