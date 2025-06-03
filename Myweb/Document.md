STEP1:
Firstly we have to build "docker build -t my-web-app ."It will build an image from a dokcerfile . Forwarding to next step.
STEP2:
 In this step we run command "docker run -p 5000:5000 my-web-app".It will create a new container.
STEP3:
After that we can create a tag "docker tag my-web-app:latest nithin1227/nithin1227:latest".It will  Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE.
STEP4:
And then Create an account in dockerhub and create a repository/registry.
STEP5:
Then configure the client with docker credentials.Using the command "docker login" ,it will ask the username and password.
STEP6:
After entering the credentials.Then push the image to dockerhub ,it will upload an image to registry.Use the command "docker push nithin1227/nithin1227:latest".
STEP7:
Then go to K8s/ folder and update the image in the deployment.yml file with the dockerhub image.
STEP8:
Install minikube and then start the minikube cluster.Use the command "minikube start" it will start the minikube.
STEP9:
Then apply the deployment and service files.
It will create the new path "cd k8s/".
STEP10:
It will create the deployment to my-web-app "kubectl apply -f deployment.yml".
It will create the service to my-web-app "kubectl apply -f svc.yml"
STEP11:
Then check the status of the pods and services.
Then expose the pod on the minikube ip.
Using the commands:
  kubectl get pods
  kubectl get svc
  It will get the pods to the deployment.
STEP12:
In this step we will forward port from a service running cluster to local machine "kubectl port-forward service/my-web-app 5000:5000"
STEP13:
After forwarding the port we can access it on port 5000.
http://localhost:5000


These are the steps innvolved in creating a deployment of a web or any application using Docker and Kubernetes.


```