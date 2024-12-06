grep -E --color 'vmx|svm' /proc/cpuinfo
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube_linux_amd64
sudo install minikube_linux_amd64 /usr/local/bin/minikube && rm minikube-linux-amd64

minikube start --driver=virtualbox
minikube status
minikube stop
minikube delete

