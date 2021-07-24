# To install on Mac using home brew

- brew install minikube
- brew install hyperkit

# start minikube

- using a hypervison
  - minikube start --vm-driver=hyperkit
- using profile
  - minikube start --profile=minikube
- additional resources
  - minikube start --cpus 6 --memory 8192

# stop minikube

- minicube stop

# delete minikube

- minikube delete --profile=minikub

# minikube status

- minikube status

# minikube - external service

- minikube service mongo-express-service -- provides an external ip address to the service
