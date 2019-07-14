# kubectl documentation

You can use the -v option to bind the kubeconfig.yaml file locally to your container.

```bash
docker run -it -v ${PWD}/kubeconfig.yaml:/root/.kube/config asforge/kubectl
```
