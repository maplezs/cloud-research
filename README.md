# Coud Research File
misscellaneous file for cloud research group
## 1. Setup Prometheus Operator
```bash
kubectl create -f https://raw.githubusercontent.com/prometheus-operator/prometheus-operator/main/bundle.yaml
```
## 2. Apply RBAC pada namespace yang sama dengan Prometheus Operator
```bash
kubectl apply -f rbac.yaml
```
## 3. Apply Prometheus CRDs untuk melakukan deploy prometheus
```bash
kubectl apply -f prom.yaml
```
## 4. Apply Service Monitor CRDs agar endpoints prometheus termonitor
```bash
kubectl apply -f svcmon.yaml
```
## 6. Apply Pod Monitor CRDs untuk melakukan monitoring metrics dari RabbitMQ Server
```bash
kubectl apply -f podmon.yaml
```
## 6. Akses prometheus web dengan port-forward dan cek Status --> Target
```bash
kubectl port-forward svc/prometheus-operated 9090:9090 &
```
