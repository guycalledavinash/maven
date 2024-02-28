# Preface
It is not a secret that java files have a .java extension
We can't execute .java files directly as computers only understand binary language
Java compiler (javac) compiles source code into byte code creating .class files which contains bytecode 
The .class file is executed by JVM to run the java program
JVM converts bytecode into machine understandable code
Java project contains several java programs (.java files)
The project source code should be compiled into byte code and executed, for which we use a concept called packaging
To deploy java project, we should package all .class files as JAR file or WAR file

			JAR : Java Archieve
			WAR : Web Archieve

The standalone java projects are packaged as a JAR file (a stadalone application is where the project runs only on one computer)
The web applications are packaged as a WAR file where multiple users can access a web applications at a time.
