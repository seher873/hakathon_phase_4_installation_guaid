🚀 Phase-4 Tooling Installation & Verification (WSL / Linux)

This document verifies all required CLI tools for Phase-4 (Kubernetes, Helm, Minikube, kubectl-ai).

🧰 Required Tools

Chocolatey (optional / Windows check)

kubectl

Helm

Minikube

kubectl-ai plugin

🔍 Version Check Commands

Run each command separately in terminal:

choco --version || echo "Chocolatey not installed (OK on WSL)"

kubectl version --client

helm version

minikube version

kubectl ai --help

📦 Installation (If Missing)
1️⃣ kubectl
curl -LO "https://dl.k8s.io/release/$(curl -Ls https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
chmod +x kubectl
sudo mv kubectl /usr/local/bin/


Verify:

kubectl version --client

2️⃣ Helm
curl https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3 | bash


Verify:

helm version

3️⃣ Minikube
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
chmod +x minikube-linux-amd64
sudo mv minikube-linux-amd64 /usr/local/bin/minikube


Verify:

minikube version

4️⃣ kubectl-ai Plugin (NO krew needed)
curl -L https://github.com/GoogleCloudPlatform/kubectl-ai/releases/latest/download/kubectl-ai-linux-amd64 -o kubectl-ai
chmod +x kubectl-ai
sudo mv kubectl-ai /usr/local/bin/


Verify:

kubectl ai --help

▶️ Start Minikube (Required for Phase-5)
minikube start --driver=docker


Check cluster:

kubectl get nodes

✅ Phase-5 Ready Checklist

 kubectl working

 helm installed

 minikube running

 kubectl-ai responding

 Docker driver active

🧠 Notes (Important)

Chocolatey is NOT required in WSL

krew is optional — kubectl-ai works without it

Phase-5 uses:

Docker images (from Phase-4)

Kubernetes manifests / Helm charts

Minikube as local cluster



BY
 💙SEHER KHAN
