# Kubernetes Dashboard

## Requirements

- Existing Kubernetes cluster
- Local Kubernetes installation

## Installation

1. Install the Kubernetes Dashboard

   ```sh
   kubectl apply --filename=https://raw.githubusercontent.com/kubernetes/dashboard/v2.7.0/aio/deploy/recommended.yaml
   ```

2. Allow the dashboard to access all namespaces

   ```sh
   kubectl apply --filename=clusterrolebinding-dashboard-admin.yaml
   ```

3. Open dashboard in browser

4. Copy the token and paste it into the dashboard login screen

   ```sh
   kubectl --namespace kubernetes-dashboard describe secret (kubectl --namespace kubernetes-dashboard get secret | grep kubernetes-dashboard-token |  awk '{print $1}')
   ```

## Usage

```sh

```

## Related Links

- [Deploy and Access the Kubernetes Dashboard](https://kubernetes.io/docs/tasks/access-application-cluster/web-ui-dashboard/)
- [`kubernetes/dashboard`](https://github.com/kubernetes/dashboard)
