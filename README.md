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

The project is available as open source under the terms of the MIT License.

Copyright 2022 Vito Botta

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
