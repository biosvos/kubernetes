docker registry를 배포한다.

### 전제 조건
- storage class가 존재해야 한다. 없다면 [여기](../storage/local/README.md) 참조
- Service에서 LoadBalancer가 가능해야 한다. 없다면, NodePort 등으로 대체

### 설치
```bash
kubectl apply -f namespace.yaml
kubectl apply -f pvc.yaml
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

### 확인 방법
```bash
curl 127.0.0.1:5000/v2/_catalog
```