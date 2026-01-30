# Configure k8s cluster

## CNI cilium install in Russia:

```
helm repo add cilium https://helm.cilium.io/
helm repo update

helm install cilium cilium/cilium --version 1.16.5 \
  --namespace kube-system \
  --set image.repository=mirror.gcr.io/cilium/cilium \
  --set operator.image.repository=mirror.gcr.io/cilium/operator \
  --set hubble.relay.image.repository=mirror.gcr.io/cilium/hubble-relay \
  --set hubble.ui.backend.image.repository=mirror.gcr.io/cilium/hubble-ui-backend \
  --set hubble.ui.frontend.image.repository=mirror.gcr.io/cilium/hubble-ui-frontend
```


Settings for cilium:

```
helm upgrade --install cilium cilium/cilium --version 1.16.5 \
  --namespace kube-system \
  --set kubeProxyReplacement=true \
  --set hubble.enabled=true \
  --set hubble.ui.enabled=true \
  --set hubble.relay.enabled=true \
  --set image.repository=mirror.gcr.io/cilium/cilium \
  --set operator.image.repository=mirror.gcr.io/cilium/operator
```