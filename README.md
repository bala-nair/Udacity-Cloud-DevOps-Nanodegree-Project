# k8s-green-blue-deploy-minikube

<h1> Prerequisites </h1>

<h3> A running instance of Minikube with an account on dockerhub is required </h3>

Install minikube https://kubernetes.io/docs/tasks/tools/install-minikube/

Install docker https://docs.docker.com/install/

Create an account in dockerhub https://hub.docker.com/

<h3> Steps </h3>

#./run_docker.sh (For the blue image)

#./upload_docker.sh (upload the blue image to docker hub)

#./run_docker.sh (For the green image)

#./upload_docker.sh (upload the green image to docker hub)

ensure minikube is running 

#kubectl apply -f ./blue-controller.json (create replication controller for blue)

#kubectl apply -f ./green-controller.json (create replication controller for green)

#kubectl apply -f ./blue-green-service.json (create the service)

#minikube service bluegreenlb --url (get the url)

Update the service to redirect to green by changing the selector to app=green

#kubectl apply -f ./blue-green-service.json (after making the above changes)

#minikube service bluegreenlb --url (now the color of index page should have changed)



