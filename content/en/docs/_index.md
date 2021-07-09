---
title: "Tanzu Glossary"
linkTitle: "Tanzu Glossary"
weight: 20
menu:
  main:
    weight: 20
---

### About This ModernApps Guide

This page provides a glossary of a number Tanzu related terms and links to more resources where applicable.

### Products

 * [Tanzu Application Service](https://tanzu.vmware.com/application-service) – A modern runtime for Java, .NET, Node, and more
 * [Tanzu Build Service ](https://tanzu.vmware.com/build-service)– Build containers from source code for Kubernetes
 * [Tanzu Application Catalog](https://tanzu.vmware.com/application-catalog) – Curated container catalog of supported open source applications
 * [Tanzu Data Services](https://tanzu.vmware.com/data-services) – Cloud native data and messaging including [GemFire](https://tanzu.vmware.com/gemfire), [RabbitMQ](https://tanzu.vmware.com/rabbitmq), [SQL](https://tanzu.vmware.com/sql) and [Greenplum](https://tanzu.vmware.com/greenplum)
 * [Tanzu Kubernetes Grid](https://tanzu.vmware.com/kubernetes-grid) – Enterprise Ready Kubernetes runtime
 * [Tanzu Mission Control](https://tanzu.vmware.com/mission-control) – Global and fleet-wide Kubernetes and policymanagement
 * [Tanzu Observability](https://tanzu.vmware.com/observability) – Enterprise observability for multi-cloud environments
 * [Tanzu Service Mesh](https://tanzu.vmware.com/service-mesh) – Enterprise-class service mesh

### Tanzu Kubernetes Grid

[**Tanzu Kubernetes Grid**](https://docs.vmware.com/en/VMware-Tanzu-Kubernetes-Grid/1.3/vmware-tanzu-kubernetes-grid-13/GUID-index.html) - is the high-level name for the upstream compatible Kubernetes runtime from VMware and is also referred to its abbreviation, TKG.

**Tanzu Kubernetes Grid instance** - This a full deployment of a TKG cluster and services. If you deployed a cluster to Azure, and then a separate cluster to AWS, these would be two separate instances.

**Management Cluster** - This is the first element you will deploy to create your TKG Instance, providing lifecycle management for your instance. [Cluster API](https://cluster-api.sigs.k8s.io/) is installed on the management cluster as a Kubernetes [custom resource](https://kubernetes.io/docs/concepts/extend-kubernetes/api-extension/custom-resources/). A management cluster can be deployed using the Tanzu CLI, the CLI and a configuration file, or the installer interface. Application workloads are not intended for this cluster. The management cluster is responsible for lifecycle management of all of its workload clusters.

**Tanzu Kubernetes Clusters** / **Workload Cluster** - Tanzu Kubernetes clusters, also referred to as workload clusters in the context of TKG, are deployed by the management cluster. These are deployed by using the Tanzu CLI, kubectl when using vSphere with Tanzu, or Tanzu Mission Control. These clusters will be used to run your Kubernetes deployments. Any number of workload clusters can be created as needed. The operator can specify the Tanzu Kubernetes Release which will define Kubernetes version to use in a workload cluster. Every cluster is operated independently, meaning workload clusters can run a mix of Kubernetes versions. 

[**Cluster API**](https://tanzu.vmware.com/content/blog/the-what-and-the-why-of-the-cluster-api) - Cluster API is a Kubernetes project to bring declarative, Kubernetes-style APIs to cluster creation, configuration, and management. It provides optional, additive functionality on top of core Kubernetes. By making use of the structured nature of Kubernetes APIs, it is possible to build higher-level cloud agnostic tools that improve user experience by allowing for greater ease of use and more sophisticated automation.

**Tanzu Kubernetes Cluster Plans** - A cluster plan is the blueprint that describes the configuration with which to deploy a Tanzu Kubernetes cluster. It provides a set of configurable values that describe settings like the number of control plane machines, worker machines, VM types, and so on.

**Shared and In-Cluster Services** - Shared and in-cluster services are services that run in the Tanzu Kubernetes Grid instance, to provide authentication and authorization of Tanzu Kubernetes clusters, logging, ingress control, and more. These are also considered [Tanzu Kubernetes Grid Extensions](https://docs.vmware.com/en/VMware-vSphere/7.0/vmware-vsphere-with-tanzu/GUID-30C87DC5-51B1-4696-A624-CEA9CF54B63A.html). 

**Bootstrap Machine** - The bootstrap machine is the laptop, host, or server on which you download and run the Tanzu CLI. This is where the initial bootstrapping of a management cluster occurs, before it is pushed to the platform where it will run. The bootstrap machine requires Docker to be running.

### vSphere with Tanzu

[**vSphere with Tanzu**](https://docs.vmware.com/en/VMware-vSphere/7.0/vmware-vsphere-with-tanzu/GUID-152BE7D2-E227-4DAA-B527-557B564D9718.html) - A feature of vSphere 7 that brings a native Kubernetes API to vSphere and turns it into a platform for running Kubernetes workloads natively in and on the ESXi hosts, side by side with virtual machines. This feature within vCenter is called Workload Management. 

**Tanzu Kubernetes Grid Service** - vSphere with Tanzu introduces the Tanzu Kubernetes Grid Service (TKGS), providing the ability for Tanzu Kubernetes Clusters to be deployed and run natively with vSphere. Managed by the Supervisor Cluster. 

**Supervisor Cluster** - This is a special Kubernetes cluster that uses ESXi as its worker nodes instead of Linux. A 3-node virtual machine Supervisor Cluster is deployed when workload management is enabled, which act as the control plane and as a TKG management cluster. The supervisor cluster is achieved by integrating the Kubernetes worker agents (Spherelets) directly into the ESXi hypervisor. This cluster uses vSphere Pod Service to run container workloads natively on the vSphere host, taking advantage of the security, availability, and performance of the ESXi hypervisor. The VM Service also runs here where virtual machines can be created in the same manner as TKG clusters using a Kubernetes style manifest.

[**vSphere Namespace**](https://docs.vmware.com/en/VMware-vSphere/7.0/vmware-vsphere-with-tanzu/GUID-3E4E6039-BD24-4C40-8575-5AA0EECBBBEC.html#vsphere-namespace-0) - A vSphere Namespace is a logical object that is created on the vSphere Kubernetes supervisor cluster. This object tracks and provides a mechanism to edit the assignment of resources (Compute, Memory, Storage & Network) and access control to Kubernetes resources, such as containers or virtual machines. You may also see some documentation refer to this object as a supervisor namespace.

[**Tanzu Kubernetes Cluster**](https://docs.vmware.com/en/VMware-vSphere/7.0/vmware-vsphere-with-tanzu/GUID-DC22EA6A-E086-4CFE-A7DA-2654891F5A12.html) - (TKC) is the name used for a Tanzu Kubernetes deployment deployed and managed by the Tanzu Kubernetes Grid Service, with the virtual machine objects deployed inside of a vSphere Namespace. This is a full conformant Kubernetes cluster, and within the cluster it operates like that of TKG. This may also be referred to as a Tanzu Guest Cluster or workload cluster.

[**vSphere Pod**](https://docs.vmware.com/en/VMware-vSphere/7.0/vmware-vsphere-with-tanzu/GUID-276F809D-2015-4FC6-92D8-8539D491815E.html?hWord=N4IghgNiBcIG4GUAOALApgJzQAgAoHsATAZxAF8g) - this is the equivalent of a Kubernetes pod. A vSphere Pod is a VM with a small footprint that runs one or more Linux containers. Each vSphere Pod is sized precisely for the workload that it accommodates and has explicit resource reservations for that workload. It allocates the exact amount of storage, memory, and CPU resources required for the workload to run. vSphere Pods are only supported with Supervisor Clusters that are configured with NSX-T Data Center as the networking stack.

[**VM Service**](https://docs.vmware.com/en/VMware-vSphere/7.0/vmware-vsphere-with-tanzu/GUID-1BAB6DBF-0EEE-44BD-ADCC-7499E4444020.html) - vSphere with Tanzu offers a VM Service functionality that enables DevOps engineers to deploy and run VMs, in addition to containers, in a common, shared Kubernetes environment. Both, containers and VMs, share the same vSphere Namespace resources and can be managed through a single vSphere with Tanzu interface.

[**Cloud Native Storage (CNS)**](https://blogs.vmware.com/virtualblocks/2019/08/14/introducing-cloud-native-storage-for-vsphere/) - a vSphere and Kubernetes (K8s) feature that makes K8s aware of how to provision storage on vSphere on-demand, in a fully automated, scalable fashion as well as providing visibility for the administrator into container volumes through the CNS UI within vCenter.

**Image Service** - The Image Service is responsible for contacting the container image registry and staging the container image on a VMDK that will be attached to the vSphere Pod by the Spherelet. It leverages Harbor and each team gets their own project to share. Image service is only only supported with Supervisor Clusters that are configured with NSX-T Data Center as the networking stack.

**Spherelet** - An additional process called Spherelet is created on each host. It is a kubelet that is ported natively to ESXi and allows the ESXi host to become part of the Kubernetes cluster. 

**Container Runtime Executive (CRX)** - CRX is similar to a VM from the perspective of Hostd and vCenter Server. CRX includes a paravirtualized Linux kernel that works together with the hypervisor. CRX uses the same hardware virtualization techniques as VMs and it has a VM boundary around it. A direct boot technique is used, which allows the Linux guest of CRX to initiate the main init process without passing through kernel initialization. This allows vSphere Pods to boot nearly as fast as containers.

[**TKG Extensions**](https://docs.vmware.com/en/VMware-vSphere/7.0/vmware-vsphere-with-tanzu/GUID-00A2BB49-DBDE-4E2B-B9EE-38C36E261185.html) - This is a set of services available to deploy into your cluster to provide additional functionality

### Kubernetes Glossary

For a standardised, comprehensive glossary for Kubernetes, please visit [this Kubernetes.io web page](https://kubernetes.io/docs/reference/glossary/?fundamental=true). 

[**Container Storage Interface (CSI)**](https://kubernetes-csi.github.io/docs/) - CSI was developed as a standard for exposing arbitrary block and file storage storage systems to containerized workloads on Container Orchestration Systems (COs) like Kubernetes.

[**Container Network Interface**](https://github.com/containernetworking/cni) - a Cloud Native Computing Foundation project, consists of a specification and libraries for writing plugins to configure network interfaces in Linux containers, along with a number of supported plugins.

Kind - [Kubernetes in Docker](https://kind.sigs.k8s.io/) - This is one of the services used to bootstrap and deploy a TKG management cluster.
