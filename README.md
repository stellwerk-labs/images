# Stellwerk Platform Orchestrator Images

This repository is the public catalog for the container images required to run
the Stellwerk Platform Orchestrator. Each published source release below is
linked to the matching image release.

| Component | Image | Source release |
| --- | --- | --- |
| Control plane | [`ghcr.io/stellwerk-labs/platform-orchestrator-cp:v1.0.2`](https://github.com/orgs/stellwerk-labs/packages/container/package/platform-orchestrator-cp) | [`platform-orchestrator-cp@v1.0.2`](https://github.com/stellwerk-labs/platform-orchestrator-cp/tree/v1.0.2) |
| Data plane | [`ghcr.io/stellwerk-labs/platform-orchestrator-dp:v1.0.2`](https://github.com/orgs/stellwerk-labs/packages/container/package/platform-orchestrator-dp) | [`platform-orchestrator-dp@v1.0.2`](https://github.com/stellwerk-labs/platform-orchestrator-dp/tree/v1.0.2) |
| Console | [`ghcr.io/stellwerk-labs/platform-orchestrator-frontend:v1.0.2`](https://github.com/orgs/stellwerk-labs/packages/container/package/platform-orchestrator-frontend) | [`platform-orchestrator-frontend@v1.0.2`](https://github.com/stellwerk-labs/platform-orchestrator-frontend/tree/v1.0.2) |
| IAM | [`ghcr.io/stellwerk-labs/platform-orchestrator-iam:v1.0.1`](https://github.com/orgs/stellwerk-labs/packages/container/package/platform-orchestrator-iam) | [`platform-orchestrator-iam@v1.0.1`](https://github.com/stellwerk-labs/platform-orchestrator-iam/tree/v1.0.1) |
| Deployment runner | [`ghcr.io/stellwerk-labs/platform-orchestrator-runner:v1.0.3`](https://github.com/orgs/stellwerk-labs/packages/container/package/platform-orchestrator-runner) | [`platform-orchestrator-runner@v1.0.3`](https://github.com/stellwerk-labs/platform-orchestrator-runner/tree/v1.0.3) |

The images target `linux/amd64` and `linux/arm64`. They are licensed under the
[EUPL-1.2](LICENSE). The license applies to the Stellwerk image distribution;
bundled third-party software remains under its respective license.

The deployment runner source is public. Remote runners must explicitly set
`REMOTE_URL`; the runner refuses to connect and logs an error when it is
missing. Image and chart releases are intentionally separate: a chart is
released manually only after its default image versions are updated as a
coherent set.

## Helm charts

The self-hosted Platform Orchestrator chart is maintained in the public
[`platform-orchestrator-helm-chart`](https://github.com/stellwerk-labs/platform-orchestrator-helm-chart)
repository and published at `oci://ghcr.io/stellwerk-labs/charts/platform-orchestrator`.

The Kubernetes agent runner is available as the
[`platform-orchestrator-kubernetes-agent-runner`](https://github.com/orgs/stellwerk-labs/packages/container/package/charts%2Fplatform-orchestrator-kubernetes-agent-runner)
OCI chart:

```shell
helm install platform-orchestrator-kubernetes-agent-runner \
  oci://ghcr.io/stellwerk-labs/charts/platform-orchestrator-kubernetes-agent-runner \
  --version 0.1.1
```

Chart `0.1.1` uses runner image `v1.0.0`.
