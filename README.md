# metric-server-k8s
#Requirements:  
- Metrics Server must be reachable from kube-apiserver  
- The kube-apiserver must be correctly configured to enable an aggregation layer  
- Nodes must have kubelet authorization configured to match Metrics Server configuration  
- Container runtime must implement a container metrics RPCs  
