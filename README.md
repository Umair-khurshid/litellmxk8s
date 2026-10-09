# LiteLLM on Kubernetes

This repository deploys LiteLLM as an OpenAI-compatible gateway with PostgreSQL,
Redis, Traefik, and Argo CD integration. 

## Validate and deploy

Render the Kustomize base:

```sh
kubectl kustomize litellm
```

Apply it directly, or create `litellm/argocd.yaml` in the Argo CD namespace after
updating its repository URL. The Application intentionally has no automated sync
policy, so changes can be reviewed before they are applied.
