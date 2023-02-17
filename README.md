dashboard token登录\token过期时间更改
- vim recommend.yaml
- :/containers
- --token-ttl=604800
- kubectl -n kubernetes-dashboard describe secret $(kubectl -n kubernetes-dashboard get secret | grep admin-user | awk '{print $1}')

git push 
- ssh-keygen -t rsa -C "your.email@example.com" -b 4096

grafana
- 更改prometheusAdapter-deployment.yaml中镜像为willdockerhub/prometheus-adapter:v0.9.1
- 更改kubeStateMetrices-deployment.yaml中镜像为bitnami/kube-state-metrics:2.5.0
