# install jenkins
```
kubectl create -f serviceaccount.yaml
helm install --name jenkins --set rbac.create=true,master.runAsUser=1000,master.fsGroup=1000 stable/jenkins
```

#Neeraj Steps
Step 1. Get the Jenkins values file for configuring our Jenkins installation
First get the Jenkins Helm values file for configuring our Jenkins installation.

wget https://raw.githubusercontent.com/helm/charts/master/stable/jenkins/values.yaml -O jenkins-values.yaml

Change

  serviceType: ClusterIP 
to
  serviceType: LoadBalancer
We don’t want to expose Jenkins directly via a LoadBalancer and use an ingress instead (Not covered in this blog)

Step 2. Install Jenkins
Run the below command:

helm install stable/jenkins --name=jenkins --namespace=jenkins -f jenkins-values.yaml
