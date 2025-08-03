# 🧩 Kubernetes Cluster 구성 

Ubuntu 22.04 환경에서 'kubeadm'과 'containerd, 'Calico'를 이용해서 Kubernetes 클러스터를 직접 구축 후 실습

---

## ✅ 구성 내용

- Master & Worker NOde 직접 구성
- containerd를 CRI 사용
- Calico CNI 설치 및 네트워크 구성
- kubeadm을 통한 클러스터 초기화 및 조인

---

## 🛠️ 환경 정보
| 항목              | 내용                       |
|------------------|----------------------------|
| OS               | Ubuntu 22.04 (VirtualBox)  |
| Kubernetes       | v1.29.x                    |
| Container Runtime| containerd                 |
| CNI              | Calico v3.27.2             |

---

## 📂 설치/구성 문서

1. [필수 설정 (swap, sysctl)](./docs/01_prerequisites.md)
2. [containerd 설치](./docs/02_containerd-setup.md)
3. [Kubernetes 설치 (kubeadm)](./docs/03_kubernetes-install.md)
4. [Master Node 초기화](./docs/04_cluster-init.md)
5. [Calico 설치](./docs/05_cni-calico.md)
6. [Worker Node 조인](./docs/06_node-join.md)

---

## 🪄 회고 및 느낀 점

- 다양한 에러 상황에서 직접 로그 분석 및 해결 시도
- 클러스터 구성의 전반적인 흐름과 컴포넌트 역할에 대한 이해 향상
- Calico를 통한 네트워크 구성 개념 정리

---
## 🔖 참고

- [공식 kubeadm 설치 가이드](https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/)
- [Calico 공식 설치 문서](https://docs.tigera.io/calico/latest/getting-started/kubernetes/)
