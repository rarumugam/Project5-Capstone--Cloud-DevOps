# Project5-Capstone--Cloud-DevOps

About the Project : In this project a containerized python flask application which is deployed on AWS EKS
==========================================================================================================

Technologies are used in Capstone project:
=========================================

AWS

Docker

Kubernetes

Python

GitHUB

CircleCI



How i did /Steps follwed:
=========================

1) Docker file is tested using a hadolint

2) Build a Docker image for the app

3) Upload the Docker image into HUB

4) Create Kubernetes cluster in AWS 

5) Create Loadbalancer for  high availability

6) Deploy a docker container 

7) An application is deployed and running on EKS cluster

8) Now, there is an update to the webpage and it has to be re-deployed. The challenge is what type of deployment strategy needed to use
   so that the clients faces the minimal downtime. 
   
   About rolling update strategy:
   
   It is a gradual process that allows you to update your Kubernetes system with only a minor effect on performance and no downtime. 
   In this strategy, the Deployment selects a Pod with the old programming, deactivates it, and creates an updated Pod to replace it.

9) Firstly, as a best practice ensure to take a backup of old application either using version control etc
   Here I have used to tagging approach to TAG the docker image as V1,V2,V3 etc
   So in case of roll back can change the build order version and re-apply the settings
   
10)  old-application is V1 and  New-application is V2 version 

11) Once the V2 is ready, push it to docker hub with V2 tag. Modify the Kubernetes configuration to pull
    updated version, then add the rolling strategy configuration so whenvever a changes in application it uses
    rolling update strategy to redeploy a update code 
