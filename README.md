# metric-server-k8s
# Requirements:  
- Metrics Server must be reachable from kube-apiserver  
- The kube-apiserver must be correctly configured to enable an aggregation layer  
- Nodes must have kubelet authorization configured to match Metrics Server configuration  
- Container runtime must implement a container metrics RPCs  
# Enable an aggregation layer  
Enable the aggregation layer via the following kube-apiserver flags. They may have already been taken care of by your provider.  
-  --requestheader-client-ca-file=<path to aggregator CA cert>
-  --requestheader-allowed-names=front-proxy-client
-  --requestheader-extra-headers-prefix=X-Remote-Extra-
-  --requestheader-group-headers=X-Remote-Group
-  --requestheader-username-headers=X-Remote-User
-  --proxy-client-cert-file=<path to aggregator proxy cert>
-  --proxy-client-key-file=<path to aggregator proxy key>
