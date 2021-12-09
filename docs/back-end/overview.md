---
sidebar_position: 1
---

# Overview

I have a [Kubernetes](https://kubernetes.io/) cluster set up for us using [AKS](https://azure.microsoft.com/en-us/services/kubernetes-service/). I will post some details soon - as I have it configured. So there will be some infrastructure in place, including load balancing (if and when we need it), and an Ingress. It uses the [Nginx Ingress](https://kubernetes.github.io/ingress-nginx/).

My plan is to have some hand-crafted deployments in each of the repos to start, and then we will create our own [Helm](https://helm.sh) charts for repetitive deployments. We are going to have _lots_ of little services for this.
