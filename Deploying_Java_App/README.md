### Workflow

1. Build java application using Maven

export MAVEN_HOME=/usr/share/maven
cd shopfront # where pom.xml is 
mvn clean install
docker build -t docker_user_id/image_name:latest .
docker login
docker push docker_user_id/image_name:
docker logout
cd kubernetes 
kubectl apply -f shopfront.yaml
kubectl get deployments,pods,services
minikube service shopfront 

2. Containerize the app and push the image to docker hub 
3. deploy the app into kubernetes cluster and access it using a web browser



