# k8s

## Cluster

Initialize cluster:
```
$ ./setup_cluster.sh
```

Reset cluster:
```
$ ./setup_cluster.sh reset
```

## Deploy metrics-server
```
$ ./deploy_metrics-server.sh
```

## Deploy kube-prometheus
```
$ ./deploy_kube-prometheus.sh
```
Note that if you already have `metrics-server`, you can't deploy `kube-prometheus`

## Install helm
```$ ./install_helm.sh```

## Deploy metalLB
```$ ./deploy_metallb.sh```

## Install Istio
Install and deploy istio using `helm`
```
$ ./install_istio.sh
```
Note: istio deployment requires a lot cpu resource, on my 2 node, 2vcpu per node cluster, I have to delete previously deployed `kube-prometheus` to free cpu resource in order to deploy `Istio`.

Deploy the `bookinfo` example:
