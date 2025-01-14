# Cadence Charts

This repo contains a fork of Cadence helm chart maintained by original Cadence team @Uber.
It tries to add some features that the original repo is still missing, most notably
the k8s ingress configuration.

**What is included:**
- Cadence backend services as separate deployments: frontend, history, matching, worker.
- Customizable replica counts and resource limitations.
- Customizable dynamic config as a configmap.
- A single instance ephemeral Cassandra container. This is included so that no external dependency is required to get started. Ideally you should have your own external (hosted or managed) DB instance that you can specify in values.yaml.
- The chart comes with cadence:master-auto-setup as the default image and capable of setting up Cassandra DB schema on first installation.
- ingress config

Check the [original repo](https://github.com/cadence-workflow/cadence-charts) for more info.
