# Kubernetes manifests for monitoring

## Lauching k3s
If k3s isn't launch, use : `k3d cluster create sdtd -p "30000-30005:30000-30005@server:0"`.

## Launch monitoring pods

To launch Prometheus and Grafana, use : `kubectl apply -f monitoring.yml`. All these pods are included in the namespace *monitoring*.

To stop it, use : `kubectl delete -f monitoring.yml`.


## Grafana access

To access to the grafanas dashboards go to he link [here](http://localhost:30001/). The login are : sdtd / happy.