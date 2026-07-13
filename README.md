# Stellwerk Platform Orchestrator Images

This repository is the public catalog for the container images required to run
the Stellwerk Platform Orchestrator. We are publishing the existing images
first while we prepare their source repositories for open source publication.

| Component | Image | Source release |
| --- | --- | --- |
| Control plane | [`ghcr.io/stellwerk-labs/platform-orchestrator-cp:v1.0.1`](https://github.com/orgs/stellwerk-labs/packages/container/package/platform-orchestrator-cp) | `platform-orchestrator-cp@v1.0.1` |
| Data plane | [`ghcr.io/stellwerk-labs/platform-orchestrator-dp:v1.0.1`](https://github.com/orgs/stellwerk-labs/packages/container/package/platform-orchestrator-dp) | `platform-orchestrator-dp@v1.0.1` |
| Console | [`ghcr.io/stellwerk-labs/platform-orchestrator-frontend:v1.0.1`](https://github.com/orgs/stellwerk-labs/packages/container/package/platform-orchestrator-frontend) | `platform-orchestrator-frontend@v1.0.1` |
| IAM | [`ghcr.io/stellwerk-labs/platform-orchestrator-iam:v1.0.0`](https://github.com/orgs/stellwerk-labs/packages/container/package/platform-orchestrator-iam) | `platform-orchestrator-iam@v1.0.0` |
| Deployment runner | [`ghcr.io/stellwerk-labs/platform-orchestrator-runner:v1.0.0`](https://github.com/orgs/stellwerk-labs/packages/container/package/platform-orchestrator-runner) | `platform-orchestrator-runner@v1.0.0` |

The images target `linux/amd64` and `linux/arm64`. They are licensed under the
[EUPL-1.2](LICENSE). The license applies to the Stellwerk image distribution;
bundled third-party software remains under its respective license.

Source links and build automation will be added here as each component source
repository is published.

## Helm chart

The Kubernetes agent runner is available as the
[`platform-orchestrator-kubernetes-agent-runner`](https://github.com/orgs/stellwerk-labs/packages/container/package/charts%2Fplatform-orchestrator-kubernetes-agent-runner)
OCI chart:

```shell
helm install platform-orchestrator-kubernetes-agent-runner \
  oci://ghcr.io/stellwerk-labs/charts/platform-orchestrator-kubernetes-agent-runner \
  --version 0.1.1
```

Chart `0.1.1` uses runner image `v1.0.0`.
