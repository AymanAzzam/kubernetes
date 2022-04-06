# kubernetes
This is a small project to try kubernetes on dev environment using minikube and kubectl.

### Run
1. Create a cluster with one worker node using minikube
```
minikube start
```
2. Run the deployment file that will create 5 pods each of them contains only one container.
```
kubectl apply -f deployment.yaml
```
3. Check that there are 5 pods created
```
kubectl get pods
```
4. Run the node-port file to open traffic for the node on port 31515
```
kubectl apply -f node-port.yaml
```
5. Check that there is a service is created for the node traffic
```
kubectl get services
```
6. Run the following command to open the k8s dashboard
```
minikube dashboard
```
7. Run the following commands to check the running containers inside the minikube node using docker
```
eval $(minikube docker-env)
docker ps
```
8. Get the ip of minikube node to access the application
```
minikube ip
```
9. Open the browser on the minikube ip with port 31515
