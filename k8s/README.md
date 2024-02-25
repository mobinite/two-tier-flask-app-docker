# Deploy two-tier flask app to K8S

## Setup k8s using kubeadm following [this.](https://github.com/mobinite/kubeadm-kubernetes-cluster)

## Setup Process

1. Clone git repo
```bash
git clone https://github.com/mobinite/two-tier-flask-app-docker.git
```
2. Navigate to the k8s directory
```bash
cd two-tier-flask-app-docker/k8s
```
3. Now execute manifest file
```bash
kubectl apply -f two-tier-flask-app-deployment.yml
kubectl apply -f two-tier-flask-app-svc.yml
kubectl apply -f mysql-pv.yml
kubectl apply -f mysql-pvc.yml
kubectl apply -f mysql-deployment.yml
kubectl apply -f mysql-svc.yml
```
### Note: Create mysqldata host path before running presistent volumne yml file