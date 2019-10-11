# Udacity-Cloud-DevOps-Nanodegree-Project

<h1> Prerequisites </h1>

<h3> A running instance of EKS with an account on dockerhub is required </h3>

Install Jenkis https://linuxize.com/post/how-to-install-jenkins-on-ubuntu-18-04/

Install EKS https://docs.aws.amazon.com/eks/latest/userguide/getting-started.html

Install Docker https://docs.docker.com/install/

Create an account in dockerhub https://hub.docker.com/

Add dockerhub credentials to Jenkins https://medium.com/@gustavo.guss/jenkins-building-docker-image-and-sending-to-registry-64b84ea45ee9

Add AWS Credentials to Jenkins https://medium.com/faun/ci-cd-pipeline-with-jenkins-and-aws-s3-c08a3656d381


<h3> Steps </h3>

#./run_docker.sh (For the blue image)

#./upload_docker.sh (upload the blue image to docker hub)

#./run_docker.sh (For the green image)

#./upload_docker.sh (upload the green image to docker hub)

ensure EKS is running 

#kubectl apply -f ./blue-controller.json (create replication controller for blue)

#kubectl apply -f ./green-controller.json (create replication controller for green)

#kubectl apply -f ./blue-green-service.json (create the service)

#kubectl get svc

Update the service to redirect to green by changing the selector to app=green

#kubectl apply -f ./blue-green-service.json (after making the above changes)

#kubectl get svc (now the color of page should have changed)



