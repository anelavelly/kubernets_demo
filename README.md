```cd kubernetes/```

launch cluster including control plain:
https://docs.aws.amazon.com/eks/latest/userguide/getting-started-console.html#eks-create-cluster

deploying dashboard:
https://docs.aws.amazon.com/eks/latest/userguide/getting-started-console.html#eks-create-cluster

Deploying an Nginx deployment:
```cat nginx-deployment.yaml|k create -f -```

to get the description of a pod:
```kubectl describe pod pod-name```

exposing to a service:
```kubectl expose deployment nginx-deployment --port=80 --type LoadBalancer```

demo of a pod logs:
```kubectl create -f pod-log.yaml```

Jenkins:
https://8gwifi.org/docs/kube-jenkins.jsp

creating a persistent volume:
```Kubectl create -f jenkins-pv.yaml```

creating a volume claim:
```kubectl create -f jenkins-pvc.yaml```

launching all the resources for jenkins:
```helm install jenkins --set persistence.existingClaim=jenkins-pvc stable/jenkins```

uninstall jenkins:
```helm uninstall jenkins```
