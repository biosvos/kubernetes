rancher에서 제공하는 방법이다.

### 설치
아래 명령 수행시, local-path-storage namespace에 배포되며, local-path StorageClass가 생성된다.
```bash
https://raw.githubusercontent.com/rancher/local-path-provisioner/master/deploy/local-path-storage.yaml
```

### 동작 확인
pod 배포가 잘되는지만 확인하면 된다.
```bash
kubectl create -f https://raw.githubusercontent.com/rancher/local-path-provisioner/master/examples/pvc/pvc.yaml
kubectl create -f https://raw.githubusercontent.com/rancher/local-path-provisioner/master/examples/pod/pod.yaml
```
