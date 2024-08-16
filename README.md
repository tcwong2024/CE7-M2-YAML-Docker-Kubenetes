# Sample-YAML

This yaml file is to deploy python application docker iamges created on the project of "Sample-Docker-Project" to deploy the images into AWS ECR.

1. Creating Kubectl pod yaml 
- kubectl apply -f nginx-pod.yaml
- kubectl get pod
- kubectl logs wtc-nginx-pod
- kubectl describe pod wtc-nginx-pod
- kubectl delete pod wtc-nginx-pod

2. Creating kubectl deployment yaml with 2 pod 
- kubectl apply -f nginx-deployment.yaml
- kubectl get deployment
- kubectl get pod
- kubectl delete pod wtc-nginx-deployment-6f48996dfc-fznxn (delete one pod with auto generated new pod)

3. Continue step 2 with added kubectl service yaml
- kubectl apply -f nginx-svc.yaml
- kubectl get deployment
- kubectl get svc
- kubectl delete -f nginx-svc.yaml
- kubectl delete deployment wtc-nginx-deployment

Note: If nginx-svc website (localhost:80) not working, apply with nginx-svc-nodePort (localhost:30080)
