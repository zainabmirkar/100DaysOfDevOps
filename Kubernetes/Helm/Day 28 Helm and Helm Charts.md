# Helm Charts
- Bundle of yaml files.
- Create your own helm charts.
- Push them to helm repository.
- Download and use the existing ones.


## 'helm search': Finding Charts

- eg :  helm search hub wordpress <br/>
The above searches for all wordpress charts on Artifact Hub.

- Once you have found a package you want to install, you can use helm install to install it.

- To keep track of a release's state, or to re-read configuration information, you can use helm status
- When it is time to uninstall a release from the cluster, use the helm uninstall command
- You can see all of your currently deployed releases with the helm list command
- The helm list --all flag will show you all release records that Helm has retained, including records for failed or deleted items (if --keep-history was specified)


## Creating Your Own Charts
- helm create command

<br/>
<br/>
<br/>
<br/>



#### References <br/>
https://helm.sh/docs/intro/using_helm/  <br/>
https://www.youtube.com/watch?v=-ykwb1d0DXU
