# Cluster-init Helm chart

## Configuration
The following table lists the configurable parameters of the `cluster-init` chart and their default values.

| Name  | Description | Default value |
| ------------- | ------------- | ------------- |
| envNamespace  |   | default |
| serviceAccpuntName  |  | sitecore-default-sa  |
| keyvault.clientID  |   |  |
| keyvault.keyvaultName  |  |  |
| keyvault.tenantId  |   |   |
| csi-secrets-store-provider-azure.enabled  | Install azure keyvault provider | true |
| csi-secrets-store-provider-azure.secrets-store-csi-driver.enableSecretRotation  | Enable secret rotation feature | true  |
| csi-secrets-store-provider-azure.secrets-store-csi-driver.linux.crds.enabled  | Driver CRDs Linux image enabled | false  |
| csi-secrets-store-provider-azure.secrets-store-csi-driver.syncSecret.enabled  | Enable rbac roles and bindings required for syncing to Kubernetes native secrets | true  |
| ingress-nginx.enabled  |   |   |
| ingress-nginx.controller.replicaCount  |   |  2 |
| ingress-nginx.controller.nodeSelector.kubernetes.io/os |   | linux  |
| ingress-nginx.controller.admissionWebhooks.patch.nodeSelector.kubernetes.io/os  |   | linux |
| ingress-nginx.controller.service.externalTrafficPolicy  |   | Local |
| ingress-nginx.controller.service.loadBalancerIP  |   |  "" |
| ingress-nginx.controller.service.annotations.service.beta.kubernetes.io/azure-dns-label-name  |   | staticip  |
| ingress-nginx.defaultBackend.nodeSelector.kubernetes.io/os  |   | linux  |
