<!-- note marker start -->
NOTE: This repo contains only the documentation for the private BoltsOps repo code.
Original file: https://github.com/boltops-learn/terraspace-google-gke-registry/blob/master/README.md
The docs are publish so they are available for interested subscribers.
For access to the source code, you can become a BoltOps subscriber.
See: https://learn.boltops.com

<!-- note marker end -->

# Terraspace GKE using Terraform Registry Module Example

[![BoltOps Badge](https://img.boltops.com/boltops/badges/boltops-badge.png)](https://www.boltops.com)

This contains example code that creates:

* Google GKE Cluster

It's uses the Terraform Registry module:

* [terraform-google-modules/kubernetes-engine](https://registry.terraform.io/modules/terraform-google-modules/kubernetes-engine/google/latest)

## Env Vars

You should configure these env vars:

* GOOGLE_PROJECT
* GOOGLE_REGION
* GOOGLE_SA: The google compute service account

## Deploy

To deploy:

    terraspace up gke

## Video

[![Watch the video](https://uploads-learn.boltops.com/norvrgfz24409boo19awd7gh7n4u)](https://learn.boltops.com/courses/terraspace-gcp/lessons/terraspace-gke-cluster-with-terraform-registry-module)

Note: Premium video content requires a subscription.
