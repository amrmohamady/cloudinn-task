Docker Stage
---
docker build -t go-app .
docker run -d -p 8080:8080 --name go-app go-app:latest

Go to the browser and navigate to localhost:8080
-------------------
kubernetes Stage
---
Push the image to DockerHub
1- docker push amrmohamady/go-app:latest
2- Deploy to kubernetes cluster
3- kubectl create -f hello-go.yml
4- kubectl get deployments
5- kubectl get pods
6- kubectl get svc
Go to browser with kubernetes-cluster-ip:nodePort 

Now we've just deployed our go application to Kubernetes cluster

--------------
Helm Stage
---
1- Install Helm : Run The Following Command Line

wget https://get.helm.sh/helm-v3.0.2-linux-amd64.tar.gz
tar xvf helm-v3.0.2-linux-amd64.tar.gz
sudo mv linux-amd64/helm /usr/local/bin/
helm version
helm init --history-max 200

