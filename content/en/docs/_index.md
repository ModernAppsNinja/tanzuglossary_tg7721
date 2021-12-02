---
title: "Tanzu Glossary"
linkTitle: "Tanzu Glossary"
weight: 20
menu:
  main:
    weight: 20
---

### About This ModernApps Guide

This page provides a short description of each Tanzu product and service, Tanzu Editions and Bundles, and a quick reference of which Tanzu procuts and services are included in each bundle. This is not a replacement for official Tanzu documentation and messaging available at [tanzu.vmware.com](https://tanzu.vmare.com). Clicking an entry name will take you to the official landing page for the product or service. Some entries have a "More detail" link--clicking that will take you to a child page for a deeper dive into the entry.

### VMware Tanzu

Portfolio of products and services targeted at developers and platform operators to help build new applications, modernize existing applications, and build modern application platforms.

### VMware Tanzu Products and Services

 * [Tanzu Application Service](https://tanzu.vmware.com/application-service) – A modern application platform supporting Java, .Net, Node, and more. Built on Cloud Foundry allowing enterprises to continuously deliver and run microservices across clouds. Provides the iconic cf push developer experience on a proven enterprise platform.
 
 * [Tanzu Application Platform](https://tanzu.vmware.com/application-platform) – A packaged set of components that helps developers and operators build, deploy, and manage apps on Kubernetes. Simplifies workflows in both the inner loop--developers' development cycle of iterating on code--and the outer loop--how operators deploy apps to production and maintain them over time. Provides a default set of components that automates pushing an app to staging and production on Kubernetes. Operators can customize the platform by replacing TAP components with other products.
 
 * [Tanzu Build Service ](https://tanzu.vmware.com/build-service)– Develop and automate containerized software workflows securely and at scale. Built on the open-source Cloud Native Buildpacks project. Creates repeatable container builds for Kubernetes and keeps images up to date.
 
 * [Tanzu Application Catalog](https://tanzu.vmware.com/application-catalog) – A customizable selection of open source software from the Bitnami collection that is continuously maintained and verifiably tested for use in production environments. Pre-packaged container images and Helm charts can be built on customer-provided security-hardened base operating system images and placed into private repositories.
 
 * [Tanzu Data Services](https://tanzu.vmware.com/data-services) – Portfolio of on-demand caching, messaging, and database software for development teams building modern applications. Products include [GemFire](https://tanzu.vmware.com/gemfire), [RabbitMQ](https://tanzu.vmware.com/rabbitmq), [SQL](https://tanzu.vmware.com/sql) and [Greenplum](https://tanzu.vmware.com/greenplum)
 
 * [Tanzu Kubernetes Grid](https://tanzu.vmware.com/kubernetes-grid) – CNCF-certified, enterprise-ready Kubernetes runtime that streamlines operations across a multi-cloud infrastructure. Offers simplified installation, automated multi-cluster operations, integrated platform service, and open source alignment. [More detail](link)
 
 * [Tanzu Kubernetes Grid Integrated Edition](https://docs.pivotal.io/tkgi/1-13/index.html) - Formerly known as Enterprise PKS. Production-grade, highly available container runtime that operates on vSphere and public clouds. Built on Kubernetes, BOSH, Operations Manager, VMware NSX-T, and Project Harbor.
 
 * [Tanzu Mission Control](https://tanzu.vmware.com/mission-control) – Centralized management platform for consistently operating and securing your Kubernetes infrastructure across multiple teams and clouds. Available as TMC Essentials, Starter, Standard, or Advanced.
 
 * [Tanzu Observability](https://tanzu.vmware.com/observability) – High-performance streaming analytics platform supporting enterprise-grade observability and analytics at scale. Monitor everything from full stack applications to cloud infrastructures with metrics, traces, counters, event logs, and analytics. 
 
 * [Tanzu Service Mesh](https://tanzu.vmware.com/service-mesh) – Enterprise-class service mesh solution that provides reliable control and security for microservices, end users, and data across all your clusters and clouds in the most demanding multi-cluster and multi-cloud environments.
 
 * [Tanzu Community Edition](https://tanzu.vmware.com/tanzu/community) - A freely-available, community-supported, fully-featured, open source Kubernetes distribution.
 
 * [Tanzu Labs](https://tanzu.vmware.com/labs) - Professional services organization that partners with you to build apps, modernize apps, build platforms, and transform data.

### VMware Tanzu Editions and Bundles

 * [Tanzu Basic Edition](https://tanzu.vmware.com/tanzu/basic) - Simplified consumption model for deploying Kubernetes to on-prem vSphere. Includes Tanzu Kubernetes Grid

 * [Tanzu Standard Edition](https://tanzu.vmware.com/tanzu/standard) - Bundle targeted at providing consistent Kubernetes infrastructure across multiple clouds. Includes Tanzu Kubernetes Grid and Tanzu Mission Control Standard. Tanzu Standard Runtime is a version of this bundle without Tanzu Mission Control Standard, available for customers that cannot consume SaaS services or for inclusion in bundles that include Tanzu Mission Control Advanced. 

 * [Tanzu Advanced Edition](https://tanzu.vmware.com/tanzu/advanced) - Operationalize containers and DevSecOps practices by accelerating development and delivery of containerized workloads, securing the container lifecycle, and simplifying operations of containers and clusters across clouds.

     Includes entitlements for Spring Runtime, Tanzu Application Catalog, Tanzu SQL, Tanzu Build Service, Tanzu Observability, Tanzu Mission Control Advanced, Tanzu Service Mesh Advanced, NSX Advanced Load Balancer Enterprise, VMware Container Networking with Antrea Advanced, and Tanzu Standard Runtime.
     
 * [Tanzu for Kubernetes Operations](ops) - Bundle of Tanzu products targeted to meet the needs of on-prem and cloud infrastructure teams. Includes Tanzu Labs services.  

     For data center and hybrid cloud deployments, this includes Tanzu Standard runtime, Tanzu Mission Control Advanced, Tanzu Observability, Tanzu Service Mesh Advanced, Antrea Advanced, and NSX Advanced Load Balancer Enterprise.

     For public cloud deployments, this includes Tanzu Standard Runtime, Tanzu Mission Control Advanced, Tanzu Observability, Tanzu Service Mesh Advanced, and Antrea Advanced.
     
 * [VMware Cloud with Tanzu services](https://blogs.vmware.com/cloud/2021/10/05/introducing-vmware-cloud-with-tanzu-services/) - Automatic entitlement to Tanzu Kubernetes Grid and Tanzu Mission Control Essentials for VMware Cloud on AWS customers, with configuration exposed via the VMware Cloud console.

### VMware Tanzu Editions and Components Mapping

The following table lists Tanzu products and services and identifies which Tanzu Editions or Bundles each is included in. Individual products and services are available separately or as add-ons to a bundle.

| | **Tanzu Basic** | **Tanzu Standard** | **Tanzu Advanced** | **Tanzu for Kubernetes Operations** | **VMware Cloud with Tanzu** |
| --- | --- | --- | --- | --- | --- |
|**Tanzu Application Service** | | | | | |
|**Tanzu Application Platform** | | | | | |
|**Tanzu Build Service** | | | Included | | |
|**Tanzu Application Catalog** | | | Included | | |
|**Tanzu Data Services** | | | Tanzu SQL | | |
|**Tanzu Kubernetes Grid** | Included | Included | Included | Included | Included |
|**Tanzu Kubernetes Grid Integrated Edition** | | | | | |
|**Tanzu Mission Control** | | Standard | Advanced | Advanced | Essentials |
|**Tanzu Observability** | | | Included | Included | |
|**Tanzu Service Mesh** | | | Included | Included | |
|**Tanzu Community Edition** | | | | | |
|**Tanzu Labs** | | | Recommended | Included | |

