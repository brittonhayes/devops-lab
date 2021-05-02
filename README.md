# DevOps Lab

> A kubernetes home lab deployed entirely with GitOps and defined in YAML.

## The Cluster

All deployed applications are defined in the `cluster` directory. nested 
into the folder that matches their namespace.

```yaml
cluster/:
  namespace/:
    project/:
      - project_resource.yaml
```

## The Infrastructure

```yaml
infrastructure/:
  - kustomization.yaml
  sources/:
    - source.yaml
```
