# Installing kubectl on Linux
To install kubectl on Linux, follow the instructions below extracted from the official installation guide.

Download and install the latest stable kubectl binary:

```sh
curl -LO "htt‌‌ps://dl.k8s.io/release/$(curl -L -s \
htt‌‌ps://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"

sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
```

Where ht‌tps://dl.k8s.io/release/stable.txt aims to display the latest Kubernetes stable release version.

NOTE: To download and set up a specific version of kubectl (such as v1.28.3) to be aligned with the Kubernetes version of the Minikube cluster, issue the following command instead:

```sh
curl -LO ht‌‌tps://dl.k8s.io/release/v1.28.3/bin/linux/amd64/kubectl
```

The installed version can be verified with:

```sh
kubectl version --client
```

A typical helpful post-installation configuration is to enable shell autocompletion for kubectl. For bash shell it can be achieved by running the following sequence of commands:

```sh
sudo apt update && sudo apt install -y bash-completion

source /usr/share/bash-completion/bash_completion

source <(kubectl completion bash)

echo 'source <(kubectl completion bash)' >> ~/.bashrc
```
