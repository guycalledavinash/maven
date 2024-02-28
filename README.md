## Preface
It is not a secret that java files have a .java extension\n
We can't execute .java files directly as computers only understand binary language\n
Java compiler (javac) compiles source code into byte code creating .class files which contains bytecode\n
The .class file is executed by JVM to run the java program\n
JVM converts bytecode into machine understandable code\n
Java project contains several java programs (.java files)\n
The project source code should be compiled into byte code and executed, for which we use a concept called packaging\n
![pic](https://github.com/guycalledavinash/maven/assets/90386560/4e3b97a0-3a0d-4219-b11f-4c2cdc2ea63c)
To deploy java project, we should package all .class files as JAR file or WAR file

			JAR : Java Archive
			WAR : Web Archive

The standalone java projects are packaged as a JAR file (a stadalone application is where the project runs only on one computer)\n
The web applications are packaged as a WAR file where multiple users can access a web applications at a time.\n

## Maven
