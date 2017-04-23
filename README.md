Prerequisite for Project setup instructions
--------------------------------------------

1. Install maven in to your local environment

2. If you are using Kurento Media Server 5.1 or lower, it is strongly recommended to upgrade your KMS.

Execute the project
-----------------------

1. Clone the project to local repo.
2. Go to the pom.xml file path and execute "mvn clean install"
3. unzip target/kurento-group-call-6.6.0.zip
4. Go to the deployment folder "cd deployment/bin/"
5. Run the start script "./start.sh" to start the app

OR

cd <path>/kurento-group-call$ mvn compile exec:java