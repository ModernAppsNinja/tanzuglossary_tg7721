---
title: "Tanzu Glossary"
linkTitle: "Tanzu Glossary"
weight: 20
menu:
  main:
    weight: 20
---

### About This ModernApps Ninja Guide

This page provides a glossary of a number Tanzu related terms and links to more resources where applicable.

### Products

 * [Tanzu Application Service](https://tanzu.vmware.com/application-service) – A modern runtime for Java, .NET and Node apps
 * [Tanzu Build Service ](https://tanzu.vmware.com/build-service)– Build containers from source code for Kubernetes
 * [Tanzu Application Catalog](https://tanzu.vmware.com/application-catalog) – Curated container catalog
 * [Tanzu Data Services](https://tanzu.vmware.com/data-services) – Cloud native data and messaging including [GemFire](https://tanzu.vmware.com/gemfire), [RabbitMQ](https://tanzu.vmware.com/rabbitmq), [SQL](https://tanzu.vmware.com/sql) and [Greenplum](https://tanzu.vmware.com/greenplum)
 * [Tanzu Kubernetes Gris](https://tanzu.vmware.com/kubernetes-grid) – Enterprise Ready Kubernetes runtime
 * [Tanzu Mission Control](https://tanzu.vmware.com/mission-control) – Centralized cluster management
 * [Tanzu Observability](https://tanzu.vmware.com/observability) – Enterprise observability for multi-cloud environments
 * [Tanzu Service Mesh](https://tanzu.vmware.com/service-mesh) – Enterprise-class service mesh

### Tanzu Kubernetes Grid

[**Tanzu Kubernetes Grid**](https://docs.vmware.com/en/VMware-Tanzu-Kubernetes-Grid/1.3/vmware-tanzu-kubernetes-grid-13/GUID-index.html) - is the high-level name for the upstream compatible Kubernetes runtime from VMware and is also referred to its abbreviation TKG.

**Tanzu Kubernetes Grid Instance** - This a full deployment of a TKG cluster and services. If you deployed a cluster to Azure, and then a separate cluster to AWS, these would be two separate instances.

**Management Cluster** - This is the first element you will deploy to create your TKG Instance, providing management and operations for your instance. This runs Cluster-API which is used to create your TKG workload clusters, as well as creating shared services for all your clusters within the instance. A management cluster can be deployed using the Tanzu CLI tool, using the CLI and a configuration file or running an installer interface. It is not recommended to run any application workloads in this cluster.

**Tanzu Kubernetes Clusters** / **Workload Cluster** - Tanzu Kubernetes Clusters, also referred to as Workload Clusters when in the context of TKG, are deployed by the management cluster. These are deployed by using the Tanzu CLI only. These clusters will be used by your developers to run your applications. You can deploy multiple numbers of clusters as per your needs, also at the Kubernetes versions you need. You can have a different version of workload clusters from one another, and from your management clusters

[**Cluster API**](https://tanzu.vmware.com/content/blog/the-what-and-the-why-of-the-cluster-api) - Cluster API is a Kubernetes project to bring declarative, Kubernetes-style APIs to cluster creation, configuration, and management. It provides optional, additive functionality on top of core Kubernetes. By making use of the structured nature of Kubernetes APIs, it is possible to build higher-level cloud agnostic tools that improve user experience by allowing for greater ease of use and more sophisticated automation.

**Tanzu Kubernetes Cluster Plans** - A cluster plan is the blueprint that describes the configuration with which to deploy a Tanzu Kubernetes cluster. It provides a set of configurable values that describe settings like the number of control plane machines, worker machines, VM types, and so on.

**Shared and In-Cluster Services** - Shared and in-cluster services are services that run in the Tanzu Kubernetes Grid instance, to provide authentication and authorization of Tanzu Kubernetes clusters, logging, and ingress control.

**Bootstrap Machine** - The bootstrap machine is the laptop, host, or server on which you download and run the Tanzu CLI. This is where the initial bootstrapping of a management cluster occurs, before it is pushed to the platform where it will run.

### vSphere with Tanzu

[**vSphere with Tanzu**](https://docs.vmware.com/en/VMware-vSphere/7.0/vmware-vsphere-with-tanzu/GUID-152BE7D2-E227-4DAA-B527-557B564D9718.html) - at a high level is the ability to provide a platform for running Kubernetes workloads natively on the ESXi hosts, side by side with virtual machines. This feature within vCenter is called Workload Management. 

**Tanzu Kubernetes Grid Service** - vSphere with Tanzu introduces the Tanzu Kubernetes Grid Service (TKGS), providing the ability for Tanzu Kubernetes Clusters to be deployed and run natively with vSphere. Managed by the Supervisor Cluster. 

**Supervisor Cluster** - This is a special Kubernetes cluster that uses ESXi as its worker nodes instead of Linux. A 3-node virtual machine Supervisor Cluster is deployed when workload management is enabled, which act as the control plane. The supervisor cluster achieved by integrating the Kubernetes worker agents, Spherelets, directly into the ESXi hypervisor. This cluster uses vSphere Pod Service to run container workloads natively on the vSphere host, taking advantage of the security, availability, and performance of the ESXi hypervisor.

[**vSphere Namespace**](https://docs.vmware.com/en/VMware-vSphere/7.0/vmware-vsphere-with-tanzu/GUID-3E4E6039-BD24-4C40-8575-5AA0EECBBBEC.html#vsphere-namespace-0) - A vSphere Namespace is a logical object that is created on the vSphere Kubernetes supervisor cluster. This object tracks and provides a mechanism to edit the assignment of resources (Compute, Memory, Storage & Network) and access control to Kubernetes resources, such as containers or virtual machines. You may also see some documentation refer to this object as a supervisor namespace.

[**Tanzu Kubernetes Cluster**](https://docs.vmware.com/en/VMware-vSphere/7.0/vmware-vsphere-with-tanzu/GUID-DC22EA6A-E086-4CFE-A7DA-2654891F5A12.html) - (TKC) is the name used for a Tanzu Kubernetes deployment deployed and managed by the Tanzu Kubernetes Grid Service, with the virtual machine objects deployed inside of a vSphere Namespace. This is a full conformant Kubernetes cluster, and within the cluster it operates like that of TKG. This may also be referred to as a Tanzu Guest Cluster.

[**vSphere Pod**](https://docs.vmware.com/en/VMware-vSphere/7.0/vmware-vsphere-with-tanzu/GUID-276F809D-2015-4FC6-92D8-8539D491815E.html?hWord=N4IghgNiBcIG4GUAOALApgJzQAgAoHsATAZxAF8g) - this is the equivalent of a Kubernetes pod. A vSphere Pod is a VM with a small footprint that runs one or more Linux containers. Each vSphere Pod is sized precisely for the workload that it accommodates and has explicit resource reservations for that workload. It allocates the exact amount of storage, memory, and CPU resources required for the workload to run. vSphere Pods are only supported with Supervisor Clusters that are configured with NSX-T Data Center as the networking stack.

[**VM Service**](https://docs.vmware.com/en/VMware-vSphere/7.0/vmware-vsphere-with-tanzu/GUID-1BAB6DBF-0EEE-44BD-ADCC-7499E4444020.html) - vSphere with Tanzu offers a VM Service functionality that enables DevOps engineers to deploy and run VMs, in addition to containers, in a common, shared Kubernetes environment. Both, containers and VMs, share the same vSphere Namespace resources and can be managed through a single vSphere with Tanzu interface.

[**Cloud Native Storage (CNS)**](https://blogs.vmware.com/virtualblocks/2019/08/14/introducing-cloud-native-storage-for-vsphere/) - a vSphere and Kubernetes (K8s) feature that makes K8s aware of how to provision storage on vSphere on-demand, in a fully automated, scalable fashion as well as providing visibility for the administrator into container volumes through the CNS UI within vCenter.

**Image Service** - The Image Service is responsible for contacting the container image registry and staging the container image on a VMDK that will be attached to the vSphere Pod by the Spherelet. It leverages Harbor and each team gets their own project to share.

**vSpherelet** - An additional process called Spherelet is created on each host. It is a kubelet that is ported natively to ESXi and allows the ESXi host to become part of the Kubernetes cluster. 

**Container Runtime Executive (CRX)** - CRX is similar to a VM from the perspective of Hostd and vCenter Server. CRX includes a paravirtualized Linux kernel that works together with the hypervisor. CRX uses the same hardware virtualization techniques as VMs and it has a VM boundary around it. A direct boot technique is used, which allows the Linux guest of CRX to initiate the main init process without passing through kernel initialization. This allows vSphere Pods to boot nearly as fast as containers.

[**TKG Extensions**](https://docs.vmware.com/en/VMware-vSphere/7.0/vmware-vsphere-with-tanzu/GUID-00A2BB49-DBDE-4E2B-B9EE-38C36E261185.html) - This is a set of services available to deploy into your cluster to provide additional functionality

### Kubernetes Glossary

For a standardised, comprehensive glossary for Kubernetes, please visit [this Kubernetes.io web page](https://kubernetes.io/docs/reference/glossary/?fundamental=true). 

[**Container Storage Interface (CSI)**](https://kubernetes-csi.github.io/docs/) - CSI was developed as a standard for exposing arbitrary block and file storage storage systems to containerized workloads on Container Orchestration Systems (COs) like Kubernetes.

[**Container Network Interface**](https://github.com/containernetworking/cni) - a Cloud Native Computing Foundation project, consists of a specification and libraries for writing plugins to configure network interfaces in Linux containers, along with a number of supported plugins.

Kind - [Kubernetes in Docker](https://kind.sigs.k8s.io/) - This is one of the services used to bootstrap and deploy a TKG management cluster.