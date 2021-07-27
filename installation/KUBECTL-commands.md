#

- kubectl version
- kubectl create -h

# Nodes

- kubectl get nodes

# Deployment

- kubectl get deployment
- Deploy pods - using deployments with an image name
  - kubectl create deployment [DEPLOYMENT-NAME] --image=nginx
    - kubectl create deployment nginx-depl --image=nginx
  - kubectl edit deployment [DEPLOYMENT-NAME]
    - kubectl edit deployment nginx-depl
      - This opens the deployment in vi editor and we can change the config of a running pod. After the save the old pod will get reminated and new pod will ve deployed by k8s.
  - kubectl delete deployment [DEPLOYMENT-NAME]
    - kubectl delete deployment nginx-depl
  - kubectl get deployment [DEPLOYMENT-NAME] -o yaml
    - kubectl get deployment nginx-deployment -o yaml
      - prints the config that saved in etcd

# Pods

- kubectl get pod
- kubectl get pod -o wide
- kubectl describe pod [POD-NAME]

# Replicaset

- kubectl get replicaset

# Services

- kubectl get services
- kubectl describe service [SERVICE-NAME]
  - kubectl describe service nginx-service
- minikube service [SERVICE-NAME]
  - minikube service mongo-express-service
  - This assigns an external IP address to the service and start the application in a browser

# Namespace

- kubectl get ns

# Other commands

- kubctl logs [POD-NAME]
- kubectl exec -it [POD_NAME] -- bin/bash
  - kubectl exec -it mongo-depl-5fd6b7d4b4-wbxcs -- bin/bash
- kubectl apply -f [FILE_NAME]
- kubectl delete -f [FILE_NAME]
- kubectl get all
- kubectl get secret
- kubectl get all | grep mongodb
- kubectl get configmap
