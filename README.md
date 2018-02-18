Kubernetes based hosting for your microservices! Instructions as follows:

1. Install kubectl and point it to a suitable Kubernetes provider. Minikube (https://github.com/kubernetes/minikube) is handy for local development
2. Inject the jwt secret into your Kubernetes environment. An extremely basic way to do this would be the following:
`kubectl create secret generic jwt --from-literal=jwt=supersecret`
3. Deploy the Kubernetes services with kubectl as follows: `kubectl apply -f ./k8s-services.yml`
4. Inspect the external IPs of your newly created services with `kubectl get services`

If you'd like to try the results of this without doing anything requiring effort, you can find an example prepared by yours truly earlier as follows:
auth: http://35.230.135.240/
transaction: http://35.230.151.204:80
 
