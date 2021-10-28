# Assignment - Wishlist

## Goal:

The goal for this assignment is to deploy a sample application im order to demonstrate how microservices run in **Kubernetes** with containers.

## Precedure:

1. Create a cluster using the command line.
	
```
$ k3d cluster create wishlist-cluster -p “8081:8081@loadbalancer” -p “8082:8082@loadbalancer”  -p “8083:8083@loadbalancer”
```

2. Run the [yaml](https://github.com/ibrahima1289/kura-wishlist-hw/blob/main/wishlist-deployment.yaml) file.

```
$ kubectl apply -f wishlit.yml
```

3. Check the services

```
$ kubectl get services
```		

4. Check on the web browser by typing the below command.

```
localhost:8080
```

## Note: <br>
For k3d, only run one container in a pod.
	
