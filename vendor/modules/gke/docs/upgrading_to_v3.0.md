<!-- note marker start -->
NOTE: This repo contains only the documentation for the private BoltsOps repo code.
Original file: https://github.com/boltops-learn/terraspace-google-gke-registry/blob/master/vendor/modules/gke/docs/upgrading_to_v3.0.md
The docs are publish so they are available for interested subscribers.
For access to the source code, you can become a BoltOps subscriber.
See: https://learn.boltops.com

<!-- note marker end -->

# Upgrading to v3.0

The v3.0 release of *kubernetes-engine* is a backwards incompatible
release.

## Migration Instructions

### Beta Features

Beta features are enabled on the `beta-public-cluster`
submodule and the `beta-private-cluster` submodule.

To migrate from the root module to the `beta-public-cluster` submodule,
update a Terraform configuration like the following example:

```diff
 module "kubernetes_engine_private_cluster" {
-  source  = "terraform-google-modules/kubernetes-engine/google"
+  source  = "terraform-google-modules/kubernetes-engine/google//modules/beta-public-cluster"
-  version = "~> 2.0"
+  version = "~> 3.0"

   # ...
 }
```

To migrate from the old `private-cluster` submodule to the new
`beta-private-cluster` submodule, update a Terraform configuration
like the following example:

```diff
 module "kubernetes_engine_private_cluster" {
-  source  = "terraform-google-modules/kubernetes-engine/google//modules/private-cluster"
+  source  = "terraform-google-modules/kubernetes-engine/google//modules/beta-private-cluster"
-  version = "~> 2.0"
+  version = "~> 3.0"

   # ...
 }
```

### IP Masqeurade

In previous versions of this module, IP Masquerade was enabled if the
network policy addon was enabled. IP Masquerade is now managed by an
explicit toggle. To continue using IP Masquerade, update a Terraform
configuration like the following example:

```diff
 module "kubernetes_engine_private_cluster" {
   source  = "terraform-google-modules/kubernetes-engine/google"
-  version = "~> 2.0"
+  version = "~> 3.0"

+  configure_ip_masq = "true"
   # ...
 }
```

