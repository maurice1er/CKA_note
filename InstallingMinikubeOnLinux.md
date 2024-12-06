```sh
grep -E --color 'vmx|svm' /proc/cpuinfo

curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube_linux_amd64

sudo install minikube_linux_amd64 /usr/local/bin/minikube && rm minikube-linux-amd64

minikube start --driver=virtualbox

minikube status

minikube stop

minikube delete

minikube version

minikube node list
```

Advanced Minikube Features

```sh
minikube profile list

minikube start --kubernetes-version=v1.27.10 --driver=podman --profile minipod

minikube start --nodes=2 --kubernetes-version=v1.28.1 --driver=docker --profile doubledocker

minikube start --driver=virtualbox --nodes=3 --disk-size=10g \
  --cpus=2 --memory=6g --kubernetes-version=v1.27.12 --cni=calico \
  --container-runtime=cri-o -p multivbox

minikube start --driver=docker --cpus=6 --memory=8g \
  --kubernetes-version="1.27.12" -p largedock

minikube start --driver=virtualbox -n 3 --container-runtime=containerd \
  --cni=calico -p minibox

minikube profile list  # Once multiple cluster profiles are available

minikube profile minibox # The target cluster can be set to minibox
```

List the nodes of a cluster

```sh
minikube node list
```

Auto Completion

```sh
sudo apt install bash-completion

source /etc/bash_completion

source <(minikube completion bash)

minikube completion bash
```
