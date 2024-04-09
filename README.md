Learning from the Book -

Step-1 : Create sample Spring boot Application.

Step-2 : Containerize it without Dockerfile
mvn spring-boot:build-image
docker run --rm --name catalog-service -p 8080:8080 catalog-service:0.0.1-SNAPSHOT

--Successfully built image 'docker.io/library/catalog-service:0.0.1-SNAPSHOT'

Step-3 : Kubernestes setup
minikube start
kubectl get nodes

Step-4 : kubectl load image
minikube image load docker.io/library/catalog-service:0.0.1-SNAPSHOT
minikube image load catalog-service:0.0.1-SNAPSHOT

minikube docker-env
docker context use default

kubectl get deployment
kubectl get pod
kubectl get svc

Docker useful commands
docker image ls