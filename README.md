Prerequisite for Project setup instructions
--------------------------------------------

1. Install maven in to your local environment

2. If you are using Kurento Media Server 5.1 or lower, it is strongly recommended to upgrade your KMS. To do that, first you need to uninstall KMS as follows:

sudo apt-get remove kurento-media-server
sudo apt-get purge kurento-media-server
sudo apt-get autoremove

3. The references to the Kurento Media Server in the APT sources should be removed:

# Delete any file in /etc/apt/sources.list.d folder related to kurento
sudo rm /etc/apt/sources.list.d/kurento*
# Edit sources.list and remove references to kurento
sudo vi /etc/apt/sources.list

4. Install the latest stable Kurento Media Server version (6.6.0) using the following commands:

echo "deb http://ubuntu.kurento.org trusty kms6" | sudo tee /etc/apt/sources.list.d/kurento.list
wget -O - http://ubuntu.kurento.org/kurento.gpg.key | sudo apt-key add -
sudo apt-get update
sudo apt-get install kurento-media-server-6.0

5. Use the following commands to start and stop it respectively:

sudo service kurento-media-server-6.0 start
sudo service kurento-media-server-6.0 stop


Execute the project
-----------------------

1. Clone the project to local repo.
2. Go to the pom.xml file path and execute "mvn clean install"
3. unzip target/kurento-group-call-6.6.0.zip
4. Go to the deployment folder "cd deployment/bin/"
5. Run the start script "./start.sh" to start the app

OR

cd <path>/kurento-group-call$ mvn compile exec:java