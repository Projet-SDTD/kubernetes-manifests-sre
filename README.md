# Kubernetes manifests for monitoring

This repo contains a manifest to deploy a basic prometheus+grafana stack retrieveing data from multiple sources:
- NodeExporter (deployed along)
- cAdvisor
- Kafka
- traefik

This is highly recommended to use ansible to deploy these manifests automatically.

## Deploying locally - Lauching k3s

If k3s isn't launch, use : `k3d cluster create sdtd -p "30000-30005:30000-30005@server:0"`.

## Launch monitoring pods

To launch Prometheus and Grafana, use : `kubectl apply -f monitoring.yml`. All these pods are included in the namespace *monitoring*.

To stop it, use : `kubectl delete -f monitoring.yml`.

## Grafana access

To access to the grafanas dashboards, if you are deploying locally go to the link [here](http://localhost:30001/), else go to the link pointing to your grafana dashboard. The login are : sdtd / happy.