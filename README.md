# Velero Notifications Controller

![Latest workflow](https://img.shields.io/github/workflow/status/simoncaron/velero-notifications/Push%20image%20of%20latest%20main?logo=github&style=for-the-badge])
[![Latest release](https://img.shields.io/github/v/tag/simoncaron/velero-notifications?label=Latest%20Release)](https://github.com/simoncaron/velero-notifications/releases/tag/1.0.0)
[![GitHub license](https://img.shields.io/github/license/simoncaron/velero-notifications?label=Licence)](https://github.com/simoncaron/velero-notifications/blob/main/LICENSE)
[![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/velero-notifications)](https://artifacthub.io/packages/helm/velero-notifications/velero-notifications)

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
