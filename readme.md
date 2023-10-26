### DEPLOYING A CONTAINERIZED PYTHON USING DOCKER AND KUBERNETES
 Prerequistes for this process is
    1.installed docker and its running
    2.installed kubernetes

## Explantion for the app code and the files
The app folder has the code that creates a fastAPI instance stores it as a variable and invokes a read_root function when a user visits the root url.
The method return a json object viewable from the browser
Requirements.txt installs required dependencies

## Containerizing the application
The Dockerfile basically defines the image we are buillding and uses an ASGI, asynchronous server gateway interface server to run the application.
We need to  build the image and tag it to your dockerhub account. 

## Deploying to kubernetes
The yaml file in the manifests folder desribes the deployment, service used, type of loadbalancer used and the ports exposed as well as the number of replicas
 
##Deplyoing the application
use the command " kubectl apply  -f k8s-and-docker.yml "
To confirm the deployment is working, run the "kubectl get deployments" command

