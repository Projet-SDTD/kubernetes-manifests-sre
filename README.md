# Kubernetes manifests for monitoring

## Lauching k3s
To launch k3s, use : `k3d cluster create sdtd -p "30000-30005:30000-30005@server:0"`.

## Launch monitoring pods

To launch Prometheus and Grafana, use : `kubectl apply -f monitoring.yml`. All these pods are included in the namespace *monitoring*.
