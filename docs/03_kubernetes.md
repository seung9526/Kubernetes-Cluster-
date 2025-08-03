
---

## ✅ `03_kubernetes.md`

```md
# 03. Kubernetes 설치 (kubeadm, kubelet, kubectl)

```bash
# 필수 패키지 설치
sudo apt install -y apt-transport-https ca-certificates curl gpg

# GPG 키 저장 디렉토리 생성
sudo mkdir -p -m 755 /etc/apt/keyrings

# Kubernetes GPG 키 등록
curl -fsSL https://pkgs.k8s.io/core:/stable:/v1.29/deb/Release.key \
  | sudo gpg --dearmor -o /etc/apt/keyrings/kubernetes-apt-keyring.gpg

# 공식 APT 소스 등록
echo 'deb [signed-by=/etc/apt/keyrings/kubernetes-apt-keyring.gpg] \
https://pkgs.k8s.io/core:/stable:/v1.29/deb/ /' \
| sudo tee /etc/apt/sources.list.d/kubernetes.list

# 패키지 목록 갱신 및 설치
sudo apt update
sudo apt install -y kubelet kubeadm kubectl

# 버전 고정
sudo apt-mark hold kubelet kubeadm kubectl
