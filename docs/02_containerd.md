
---

## ✅ `02_containerd.md`

```md
# 02. containerd 설치 및 설정

```bash
sudo apt update
sudo apt install -y containerd

# 기본 설정 파일 생성
sudo mkdir -p /etc/containerd
containerd config default | sudo tee /etc/containerd/config.toml

# systemd cgroup 설정
sudo sed -i 's/SystemdCgroup = false/SystemdCgroup = true/' /etc/containerd/config.toml

# 서비스 재시작 및 부팅 시 자동 시작
sudo systemctl restart containerd
sudo systemctl enable containerd
