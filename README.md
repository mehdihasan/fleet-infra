# GitOps Playground

## Looking for answer for the following questions

- how to deploy for multiple namespaces?
- how to deploy for multiple versions?
- how to deploy for multiple versions into multiple namespaces?

## Handy commans

export GITHUB_TOKEN=<your-token>
export GITHUB_USER=<your-username>

Check you have everything needed to run Flux by running the following command:

```bash
flux check --pre
```

Install Flux onto your cluster. Run the bootstrap command:

```bash
flux bootstrap github \
  --owner=$GITHUB_USER \
  --repository=fleet-infra \
  --branch=main \
  --path=./flux-system \
  --personal
```

helm-charts/fluxcd-demo


```bash
flux get kustomizations --watch

k get GitRepository -n flux-system

k get Kustomization -n flux-system

k get HelmRelease -n flux-system
```

