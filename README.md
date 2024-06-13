### Add the domain label to the cluster object in 'Continuous Delivery' -> Clusters -> 'clustername', this is used by the ingress

Execute:

```
IP_ADDRESS=$(kubectl -n hello-rancher get ingress hello-rancher -o jsonpath="{.status.loadBalancer.ingress[].ip}")
echo "add the label 'domain' => '${IP_ADDRESS}.sslip.io' to the cluster"
```
