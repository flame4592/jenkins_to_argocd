# jenkins_to_argocd
repository for jenkins_to_argocd

In this repo we will find two Jenkinsfile :- Jenkinsfile_1 & Jenkinsfile_2 , Using these files we will run two jenkins job , first will be to checkout the code of the respective branch and then 
build the docker container and push to docker registry . ( make sure dockerfile is present to make the docker container ) 

In the 2nd job we will be editing the deployment.yaml file where the docker image tag is configured and update it to the lates image tag . 

Argocd uses polling method to detect any changes in the repoitory it is configured to watch out for and upon detecting any changes it will upadte k8 with the latest image .



1) Rename the files to just Jenkinfile . 
2) Make sure the Jenkinsfile_1 is in the main code repo in the respective branch . 
3) And Jenkinsfile_2 should be in the manifest repo , and the manifest repo should also be configured in the argocd to detect the image update change .