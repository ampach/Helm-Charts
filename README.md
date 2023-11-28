# Sitecore Helm Charts

This GitHub repository represents a source for a helm repo and serves to optimize, improve and simplify a Sitecore deployment to Kubernetes. 

## Charts

### Charts to provision an infrastructure

- [cluster-init](charts/cluster-init) - chart to setup and configure all required dependencies such as NGINX ingress controller and CSI Secrets Store Provider for Azure Key Vault

- [cert-manager](charts/cert-manager) - chart to install and configure a [certtificate manager](https://cert-manager.io/) which is serves to generate, sign and assign corresponding certificates to application running in the cluster.

- [sitecore-dev](charts/sitecore-dev) - chart to install MSSQL Server, Sorl and Redis. Usually used for Non-Production environmets. 

### Charts to deploy a single Sitecore roles

- [sitecore-xm1-init](charts/sitecore-xm1-init) - chart to initialize Sitecore XM1 environment with all required data such as SQL databases and Solr indaxes

- [sitecore-cd-role](charts/sitecore-cd) - chart to install a Sitecore CD role.

- [sitecore-cm-role](charts/sitecore-cm) - chart to install a Sitecore CM role.

- [sitecore-id-role](charts/sitecore-id) - chart to install a Sitecore Identity Server Helm chart for Kubernetes 

- [sitecore-rendering-role](charts/sitecore-rendering) - chart to install a [next.js based Sitecore Rendering Host ](https://github.com/sitecorelabs/xmcloud-foundation-head-dev/tree/main/src/sxastarter)

### Charts to deploy a hole Sitecore XM1 environment

- [sitecore-xm1](charts/sitecore-xm1) - A Helm chart which combines all Sitecore XM1 roles as sub-charts.

## Installation

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

    helm repo add [alias] https://ampach.github.io/Sitecore.Helm-Charts

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages.  You can then run `helm search repo
[alias]` to see the charts.

To install the [chart-name] chart:

    helm install my-[chart-name] [alias]/[chart-name]

To uninstall the chart:

    helm delete my-[chart-name]
