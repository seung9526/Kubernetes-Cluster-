
---

## ✅ `06_worker-join.md`

```md
# 06. Worker 노드 조인

```bash
# 마스터 노드에서 출력된 명령어를 Worker 노드에서 실행

sudo kubeadm join <Master_IP>:6443 --token <TOKEN> \
  --discovery-token-ca-cert-hash sha256:<HASH>
