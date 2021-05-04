<h1 align="center">DevOps Lab 🧪</h1>

<p align="center">
<image width="84px" alt="logo" src="https://cncf-branding.netlify.app/img/projects/helm/stacked/color/helm-stacked-color.png"></image><image width="84px" alt="logo" src="https://info.container-solutions.com/hs-fs/hubfs/GITOPS_icon.png?width=628&height=628&name=GITOPS_icon.png"></image><image width="84px" alt="logo" src="https://sdtimes.com/wp-content/uploads/2017/01/0118.sdt-kubernetes.png"></image>
</p>

> A Kubernetes home lab deployed entirely with GitOps and defined in YAML.


## The Cluster

All deployed applications are defined in the `cluster` directory. Each project is nested
into the folder that matches their namespace.


```yaml
cluster/:
  namespace/:
    project/:
      - project_resource.yaml
```

```text
|-- /cluster
|---- /default      :   A catch-all namespace
|---- /dev          :   Development tools
|---- /home         :   Home applications and services
|---- /games        :   Dedicated game servers
|---- /monitoring   :   Logging, monitoring, and dashboards
|---- /kube-system  :   Internal system services
|---- /flux-system  :   GitOps/Flux operator and services
|---- /openfaas     :   Open faas serverless resources
```

## The Infrastructure

The collection of helm repositories are defined in the `infrastructure` directory.


```yaml
infrastructure/:
  - kustomization.yaml
  sources/:
    - source.yaml
```
