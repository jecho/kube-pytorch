# kube-pytorch examples

Examples from `https://github.com/pytorch/examples`

Trains a single fully-connected layer to fit a 4th degree polynomial.

```
kubectl -n pytorch create -f reg-cm.yaml
helm install --name=pytorch-sample1 --namespace=pytorch --set configMap=reg-cm --set persistence.enabled=false \
    --set entrypoint.file=main.py bitnami/pytorch 
```

Basic MNIST Example

```
kubectl -n pytorch create -f mnist-cm.yaml
helm install --name=pytorch-sample2 --namespace=pytorch --set configMap=mnist-cm --set persistence.enabled=false \
    --set securityContext.runAsUser=0 --set entrypoint.file=main.py bitnami/pytorch  
```