# Velero Notifications Controller

## Overview

This is a simple Kubernetes controller written in Ruby that sends Email/Slack/Webhook notifications when backups or restores are performed by [Velero](https://velero.io/) in a [Kubernetes](https://kubernetes.io/) cluster.

## Installation

Begin by adding and updating the grafana Helm chart repo:
```
helm repo add velero-notifications https://simoncaron.github.io/velero-notifications/
helm repo update
```
Next, install the chart:
```
helm install my-release velero-notifications/velero-notifications
```
Replace my-release with your desired release name.

## Configuration

If you want to modify the default parameters, you can create a values.yaml file and pass it in to helm install:

```
helm install my-release velero-notifications/velero-notifications -f values.yaml
```
A list of configurable template parameters can be found in the [Helm chart repository](https://github.com/simoncaron/velero-notifications/tree/main/charts/velero-notifications).

## License

[MIT License](https://github.com/simoncaron/velero-notifications/blob/main/LICENSE)
