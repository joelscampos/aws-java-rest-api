# aws-java-rest-api
Project to demonstrate how to create an endpoint using Amazon Lambda with Java

## Install Pre-requisites

* [Node and NPM](https://www.npmjs.com/get-npm)
* [Java JDK](https://www.oracle.com/technetwork/java/javase/downloads/index.html)
* Set up your JAVA_HOME environment variable. Example: JAVA_HOME=C:\Program Files\Java\jdk1.8.0_144
* [Maven](https://maven.apache.org/download.cgi)
* Add the apache-maven-x.x.x/bin folder to the path environment variable.
* [Serverless Framework](https://serverless.com/)
* [Set up credential for AWS, and set it up to be used with Serverless Framework.](https://serverless.com/framework/docs/providers/aws/guide/credentials/)

## Testing Pre-requisites
Teste Java installation:
    **java -version**
```
    C:\Users\JoelSCampos>java -version
    java version "1.8.0_211"
    Java(TM) SE Runtime Environment (build 1.8.0_211-b12)
    Java HotSpot(TM) 64-Bit Server VM (build 25.211-b12, mixed mode)
```
  
Test Mavan installation:
    **mvn -v**
```
C:\Users\JoelSCampos>mvn -v
    Apache Maven 3.6.1 (d66c9c0b3152b2e69ee9bac180bb8fcc8e6af555; 2019-04-04T16:00:29-03:00)
    Maven home: C:\maven-3.6.1\bin\..
    Java version: 1.8.0_144, vendor: Oracle Corporation, runtime: C:\Program Files\Java\jdk1.8.0_144\jre
    Default locale: pt_BR, platform encoding: Cp1252
    OS name: "windows 10", version: "10.0", arch: "amd64", family: "windows"
```

Test Serverless Framework:
**serverless -version**
```
    C:\Users\JoelSCampos>serverless -version
    1.42.2
```

Both commands should display the versions of the Java and Maven, respectively.

## Create the AWS Serverless Project

Create a new folder for your project:

![image](https://user-images.githubusercontent.com/2295468/57201700-ddd21b80-6f72-11e9-9658-e7712e47aaa5.png)

Command to create an AWS Serverless project:
![image](https://user-images.githubusercontent.com/2295468/57201735-8c765c00-6f73-11e9-84e6-f7ea0913eccb.png)
    
The above command created these files:

![image](https://user-images.githubusercontent.com/2295468/57201751-a0ba5900-6f73-11e9-89ce-6bc250ed9367.png)

In the pom.xml, change value of these two tags:

![image](https://user-images.githubusercontent.com/2295468/57355057-8df67e80-7143-11e9-9520-a7c6943955e3.png)

Now, build the Java project:

![image](https://user-images.githubusercontent.com/2295468/57355111-a8305c80-7143-11e9-9d9b-ceb99f0bcc56.png)


You will notice the java project was built into the "/target/" folder:

![image](https://user-images.githubusercontent.com/2295468/57355151-baaa9600-7143-11e9-96d9-4a28ff273891.png)


### Now we have to ajuste the file "serverless.yml".

Change the values of these two properties, so the serverless framework will be able to find the "aws-java-rest-project-dev.jar":

![image](https://user-images.githubusercontent.com/2295468/57355186-d150ed00-7143-11e9-8ebf-20522dc9d05c.png)


Now, map an event to an handler:

![image](https://user-images.githubusercontent.com/2295468/57355224-e62d8080-7143-11e9-9af4-6c524ac035be.png)
![image](https://user-images.githubusercontent.com/2295468/57355238-ee85bb80-7143-11e9-948e-aa7d28e96ab6.png)

Now we just have to run the "serverless deploy" command, to see everything goes up to the Amazon servers:

![image](https://user-images.githubusercontent.com/2295468/57355259-ffcec800-7143-11e9-80bc-054e41805777.png)


And there we have the endpoint working:

![image](https://user-images.githubusercontent.com/2295468/57355277-0c532080-7144-11e9-993d-a6faa311cf6a.png)
