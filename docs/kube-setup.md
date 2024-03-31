# With LoadBalancer
```
neon-master-0 $ kubeadm init --cri-socket=unix:///var/run/crio/crio.sock --control-plane-endpoint "control-plane.cluster.oliverjanka.ch:6443" --pod-network-cidr 10.85.0.0/16 --upload-certs
neon-master-* $ kubeadm join control-plane.cluster.oliverjanka.ch:6443 --token <token> --discovery-token-ca-cert-hash <discovery-token-hash> --control-plane --certificate-key <certificate-key>
neon-worker-* $ kubeadm join control-plane.cluster.oliverjanka.ch:6443 --token <token> --discovery-token-ca-cert-hash <discovery-token-hash>
```

# Without LoadBalancer
```
neon-master-0 $ kubeadm init --cri-socket=unix:///var/run/crio/crio.sock --pod-network-cidr 10.85.0.0/16 --upload-certs
neon-worker-* $ kubeadm join 192.168.1.20:6443 --token <token> --discovery-token-ca-cert-hash <discovery-token-hash>
```
# Copy admin.conf from neon-master-01 to another machine
```
$ ssh rasp-two -t 'sudo cat /etc/kubernetes/admin.conf' | ssh debian-dev -t 'tee /home/debian/.kube/config'
```
