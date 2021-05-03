# DevOps Lab

> A kubernetes home lab deployed entirely with GitOps and defined in YAML.


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
|---- /home         :   Home applications and services
|---- /games        :   Dedicated game servers
|---- /monitoring   :   Logging, monitoring, and dashboards
|---- /kube-system  :   Internal system services
|---- /flux-system  :   GitOps/Flux operator and services
```

## The Infrastructure

The collection of helm repositories are defined in the `infrastructure` directory.


```yaml
infrastructure/:
  - kustomization.yaml
  sources/:
    - source.yaml
```
