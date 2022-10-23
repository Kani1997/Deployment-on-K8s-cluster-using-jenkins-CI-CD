<div align="center">

## Deployment-on-Kubernetes-cluster-using-jenkins-CI-CD-Project

![Kubernetes final image (9)](https://user-images.githubusercontent.com/58173938/197371041-c63a95d6-9905-4beb-833b-cc9e1ac6562f.png)

</div>
<br>



We will have a deployment over a Kubernetes cluster using Jenkins CI/CD pipeline,  <br>
in this project, we are taking the help of various DevOps tools like GitHub, Jenkins,  <br>
and regular Kubernetes cluster.

We will also learn about Kubernetes to know about this deployment and services and we  <br>
will write Ansible playbooks with it, we will also write Dockerfile.

## Agenda 

When the developer writes a Docker file, he pushes it to the GitHub repository  <br>
so whenever there is a new commit to the GitHub repo When the new code arrives it  <br>
 
 - Notifies Jenkins via a webhook, and Jenkins starts a build

 - Jenkins pulls all the code from the GitHub repository Once it's completed, it will <br>
  ssh to the ansible server so when a developer pushes a docker file it accesses the  <br>
  Ansible server and starts running the image.

 - When it gets the docker file it starts building the image based on the docker file It  <br>
  tags it, and once tagged it pushes to the Docker hub and the second task of the Ansible  <br>
  Server is, it will ssh to our Kubernetes cluster server, which will evaluate here and ansible  <br>
  will execute a playbook.

 - It runs the kubectl command on our Kubernetes cluster web app and it tries to get the  <br>
  latest image.It will pull from the docker hub and it will start building the image,   <br>
  it will build a container and that container should be available to us using an IP and a port

 - We're going to start by writing service.yaml and handit over to the Kubernetes cluster <br>
  So this is the whole scenario in simple terms was going to achieve a Kubernetes deployment

 - I will tell you what are the prerequisites along with using Jenkins CI /CD by using various tools  <br>
  We use Linux commands, Jenkins, and Docker, and you need to have a Dockerhub account, so once  <br>
  Ansible Server builds a Docker image based on the Docker file, we push it to Docker Hub.

 - So we need to log in to Docker Hub here so we can easily push the latest image so what we're trying  <br>
  to accomplish here is we have the latest image and we also maintain a version based on the build

 - It builds v1, it contains a fresh image

 - If the second time it builds another image v2, so that the second contains the latest  <br>
  image, we are performing a version, also, we have to separate the latest image

 - So what are the necessary pre-requisites to follow:

 - first, create a Dockerhub account, along with we should have ansible Kubernetes and for this project  <br>
  we are going to set up a minikube cluster So basically we need two instances of Jenkins and Ansible  <br>
  and one for the Kubernetes cluster for the web app.

 - To install Kubernetes(minikube) were using AWS EC2

## Project is divided into 6 parts

- [Server Setup](https://github.com/Krishnamohan-Yerrabilli/Deployment-on-K8s-cluster-using-jenkins-CI-CD/tree/main/Server%20Setup) 
- [Dockerfile - Configure Webhook - Trigger Jenkins Job - git](https://github.com/Krishnamohan-Yerrabilli/Deployment-on-K8s-cluster-using-jenkins-CI-CD/tree/main/Dockerfile%20-%20Configure%20Webhook%20-%20Trigger%20Jenkins%20Job%20-%20git) 
- [Transfer & Execute files on remote server using SshAgent](https://github.com/Krishnamohan-Yerrabilli/Deployment-on-K8s-cluster-using-jenkins-CI-CD/tree/main/Transfer%20%26%20Execute%20files%20on%20remote%20server%20using%20SshAgent)
- [Build docker Images using Dockerfile - Tag docker images](https://github.com/Krishnamohan-Yerrabilli/Deployment-on-K8s-cluster-using-jenkins-CI-CD/tree/main/Build%20docker%20Images%20using%20Dockerfile%20-%20Tag%20docker%20images)
- [Complete Declarative CI/CD Pipelines in Jenkins Project - Push Images to DockerHub](https://github.com/Krishnamohan-Yerrabilli/Deployment-on-K8s-cluster-using-jenkins-CI-CD/blob/main/Complete%20Declarative%20CI-CD%20Pipelines%20in%20Jenkins%20Project%20-%20Push%20Images%20to%20DockerHub/README.md)
- Complete Real-time Deployment on Kubernetes cluster using jenkins CI/CD

I will update my learnings of each part, This is going to be awesome. 
