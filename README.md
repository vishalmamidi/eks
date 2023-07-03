# eks
## using ekscli tool

https://github.com/weaveworks/eksctl
https://eksctl.io/

`--dry-run` for dry run
### using command line 
```bash
eksctl create cluster --name=dev-eks-cluster01 --nodegroup-name=linux-nodes --node-type=t2.micro --region=us-east-1 --nodes=1 --tags environment=dev
```

### using yaml 
```
eksctl create cluster -f cluster.yaml
```

```
apiVersion: eksctl.io/v1alpha5
kind: ClusterConfig

metadata:
  name: basic-cluster
  region: eu-north-1

nodeGroups:
  - name: ng-1
    instanceType: m5.large
    desiredCapacity: 10
  - name: ng-2
    instanceType: m5.xlarge
    desiredCapacity: 2

```
