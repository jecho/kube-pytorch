# kube-pytorch examples

Trains a single fully-connected layer to fit a 4th degree polynomial.

```
kubectl create -f reg-cm.yaml
helm install --name sample1 --set configMap=reg-cm bitnami/pytorch --set entrypoint.file=main.py
```