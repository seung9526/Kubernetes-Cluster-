
---

## ✅ `04_cluster-init.md`

```md
# 04. 클러스터 초기화 (Master 노드에서 실행)

```bash
# 클러스터 초기화
sudo kubeadm init --pod-network-cidr=192.168.0.0/16

# kubeconfig 설정
mkdir -p $HOME/.kube
sudo cp /etc/kubernetes/admin.conf $HOME/.kube/config
sudo chown $(id -u):$(id -g) $HOME/.kube/config
