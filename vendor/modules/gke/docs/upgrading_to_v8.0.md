<!-- note marker start -->
NOTE: This repo contains only the documentation for the private BoltsOps repo code.
Original file: https://github.com/boltops-learn/terraspace-google-gke-registry/blob/master/vendor/modules/gke/docs/upgrading_to_v8.0.md
The docs are publish so they are available for interested subscribers.
For access to the source code, you can become a BoltOps subscriber.
See: https://learn.boltops.com

<!-- note marker end -->

# Upgrading to v8.0

The v8.0 release of *kubernetes-engine* is a backwards incompatible
release.

## Workload Identity (beta)
Beta clusters now have Workload Identity enabled by default. To disable Workload Identity, set `identity_namespace = null`

## Shielded Nodes (beta)
Beta clusters now have shielded nodes enabled by default. To disable, set `enable_shielded_nodes = false`
