# Jenkins-Project
Terraform deployment through jenkins

## Step - 01
Use the Dockerfile to create a docker image to run jenkins locally if using a windows host the file I provided would work otherwise please refer to "On mac and linux" section on this page: https://www.jenkins.io/doc/book/installing/docker/.

## Step - 02
Start up a container using the jenkins image we just created. By typing this in your cmd or terminal.
On Linux or Mac:
docker run --name jenkins -v /var/run/docker.sock:/var/run/docker.sock --privileged --user root -p 50000:50000 -p 8080:8080 -d jenkins:lts-docker
On Windows:
docker run --name jenkins -v //var/run/docker.sock:/var/run/docker.sock  --privileged --user root -p 50000:50000 -p 8080:8080 -d jenkins:lts-docker

## Step - 03
Open up localhost:8080/ and you will be asked to login into jenkins using admin password which can be found by typing this into your cmd or terminal.
docker exec jenkins cat /var/jenkins_home/secrets/initialAdminPassword

## Step - 04
Install suggested plugins and create your admin credentials when asked.

