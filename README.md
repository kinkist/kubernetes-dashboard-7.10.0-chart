# kubernetes-dashboard-7.10.0 Helm chart for namespace
  - fixed generating template : add namespace when `helm tempalte -namespace dashboard`

# Source
  - Original : https://github.com/kubernetes/dashboard
  - Modified Source : https://github.com/kinkist/dashboard

# Use
```
helm template kubernetes-dashboard kubernetes-dashboard --dependency-update --include-crds \
  --namespace dashboard \
  --repo https://raw.githubusercontent.com/kinkist/kubernetes-dashboard-7.10.0-chart/refs/heads/main/ \
  --set kong.proxy.type=LoadBalancer \
  --set kong.proxy.http.enabled=true
```
