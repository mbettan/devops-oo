# devops-oo

DevOps Framework for HPE Operations Orchestration

With this project, you should easily be able de add some continous integration to your flow devolopement and deploying process.
This project aims to offer a lightweight, extandable ans easy to deploy DevOps Framework for HPE Operations Orchestration based on docker containers.


## Prerequisites

You need to have a docker engine on your work enviroment network to be able to use the framework.



## Deployment

On your docker engine issue the following commands

`docker run -d --name Jenkins_CI --hostname jenkins.lab.local -p 36980:8080 -p 36922:22 -p 36950:50000 hppocfactory/jenkins_hack_img`

`docker run -d --hostname gitlab.lab.local --name Gitlab_CI -p 33380:33380 -p 33322:22 -p 33443:443 hppocfactory/gitlab_hack_img /usr/local/sbin/start-proc.sh`

`docker run -d --hostname nexus.lab.local --name Nexus_CI -p 8081:8080 hppocfactory/nexus_hack_img`

 Make sure the containers are deployed by entring the following URL into your prefered browser.
 
 Jenkins UI : http://<DOCKER_ENGINE_IP>:36980 
 GitLab UI : http://<DOCKER_ENGINE_IP>:33380
 Nexus UI : http://<DOCKER_ENGINE_IP>:8081
 
 Credentials:
	Jenkins (ssh): root/HP1nvent
	GitLab (WebUI): HPDev/HP1nvent
	Nexus (WebUI): admin/admin123
 
## Setting up

1)	First you need to create a project on GitLab or, you can use precreated project "MyContent".

2)	Configure Studio to use GitLab.

3)	Issue an SCM Update on OO Studio, (if you are using the MyContent project you should have the StandaloneStackato Project added to your project list).

4)	Open Jenkins project Hackathon-Hook-Oosha, make sure the IP of the git repository (Source Code Management) corresponds to your Docker IP address.

<img src="https://github.com/mbettan/devops-oo/blob/master/img/nexus.png" />

5)	Make the necessary changes on the IP addresses and project name writen in the execute shell build steps to correspond to your enviroment.
      	  
<img src="https://github.com/mbettan/devops-oo/blob/master/img/ooprint.png"/>


<img src="https://github.com/mbettan/devops-oo/blob/master/img/nexus.png" />