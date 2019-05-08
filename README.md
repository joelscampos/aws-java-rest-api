# aws-java-rest-api
Project to demonstrate how to create an endpoint using Amazon Lambda with Java

## Install Pre-requisites

  * NPM
  * Java JDK
  * Maven


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
