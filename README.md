# Onpremnetes The Hard Way On VirtualBox

This tutorial walks you through setting up Kubernetes the hard way on a local machine using VirtualBox.
This guide is not for people looking for a fully automated command to bring up a Kubernetes cluster.
If that's you then check out [Google Kubernetes Engine](https://cloud.google.com/kubernetes-engine), or the [Getting Started Guides](http://kubernetes.io/docs/getting-started-guides/).

Kubernetes The Hard Way is optimized for learning, which means taking the long route to ensure you understand each task required to bootstrap a Kubernetes cluster.

This tutorial is a modified version of the original developed by [Kelsey Hightower](https://github.com/kelseyhightower/kubernetes-the-hard-way).
While the original one uses GCP as the platform to deploy kubernetes,  we use VirtualBox and Vagrant to deploy a cluster on a local machine. If you prefer the cloud version, refer to the original one [here](https://github.com/kelseyhightower/kubernetes-the-hard-way)

Another difference is that we use Docker instead of containerd. There are a few other differences to the original and they are documented [here](docs/differences-to-original.md)

> The results of this tutorial should not be viewed as production ready, and may receive limited support from the community, but don't let that stop you from learning!

## Target Audience

The target audience for this tutorial is someone planning to support a production Kubernetes cluster and wants to understand how everything fits together.

## Cluster Details

Onpremnetes The Hard Way guides you through bootstrapping a highly available Kubernetes cluster with end-to-end encryption between components and RBAC authentication.

* [Kubernetes](https://github.com/kubernetes/kubernetes) 1.18.0
* [Docker Container Runtime](https://github.com/containerd/containerd) 18.06
* [CNI Container Networking](https://github.com/containernetworking/cni) 0.8.6
* [Weave Networking](https://www.weave.works/docs/net/latest/kubernetes/kube-addon/)
* [etcd](https://github.com/coreos/etcd) v3.3.9
* [CoreDNS](https://github.com/coredns/coredns) v1.7.0

## Labs

* [Prerequisites](quick-start/01-prerequisites.md)
* [Provisioning Compute Resources](quick-start/02-compute-resources.md)
* [Installing the Client Tools](quick-start/03-client-tools.md)
* [Provisioning the CA and Generating TLS Certificates](quick-start/04-certificate-authority.md)
* [Generating Kubernetes Configuration Files for Authentication](quick-start/05-kubernetes-configuration-files.md)
* [Generating the Data Encryption Config and Key](quick-start/06-data-encryption-keys.md)
* [Bootstrapping the etcd Cluster](quick-start/07-bootstrapping-etcd.md)
* [Bootstrapping the Kubernetes Control Plane](quick-start/08-bootstrapping-kubernetes-controllers.md)
* [TLS Bootstrapping the Kubernetes Worker Nodes](quick-start/09-tls-bootstrapping-kubernetes-workers.md)
* [Configuring kubectl for Remote Access](quick-start/10-configuring-kubectl.md)
* [Deploy Weave - Pod Networking Solution](quick-start/11-configure-pod-networking.md)
* [Kube API Server to Kubelet Configuration](quick-start/12-kube-apiserver-to-kubelet.md)
* [Deploying the DNS Cluster Add-on](quick-start/13-dns-addon.md)
* [Smoke Test](quick-start/14-smoke-test.md)
