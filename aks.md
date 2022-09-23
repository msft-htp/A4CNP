# Azure Kubernetes whiteboard design session

## Introduction

Contoso insurance is building a new claims application. The application is going to be built in Go, packaged in containers and run on Kubernetes. The goal of the new application is to make it easier for customers to upload an insurance claim using a mobile app.

The development team at Contoso insurance has limited experience with Kubernetes and is looking at you to help them solve some of their technical requirements as well as answer some questions they have.

## Technical requirements

The Contoso insurance team has done their initial research into Kubernetes and how to run Kubernetes on Azure. They believe AKS will meet their needs, but are not entirely sure. It is your job to guide them along their decision and ensure their deployment on Azure will be a success.

### Application requirements

The new insurance claims application will be written in Go. It is a microservices application, where each service can scale independently. Some of the application requirements are:

1. Different services have different requirements for CPU/memory. To optimize costs, the team wants to host the CPU-intensive microservices on different VMs than the memory-intensive microservices. How can they do this?
1. The team is planning to make frequent updates to the microservices and wants to deploy them automatically into the Kubernetes cluster. How do you recommend they implement the deployment automation?
1. The team will also need an environment to do testing of new functionality. What are the different options and what do you recommend?

### Network requirements

1. The application running in Azure will need to make back-end calls to an Oracle database running in Contoso's on-prem datacenter. How can an application running in Kubernetes connect to this database?
1. Customer will connect to the application using a mobile app, connecting to a public facing API. The security team has expressed concern about SQL injections and cross-site scripting. How do you recommend Contoso deal with these potential vulnerabilities? What is the impact on the network design?
1. The network team at Contoso wants to ensure that services only communicate with other services based on an allow-list (also known as micro-segmentation). How can contoso ensure services running on Kubernetes can only communicate with predefined other services?

## Questions

* We have heard that Kubernetes makes it easy to scale our application. How does AKS handle autoscaling of the workload and the cluster?
* We've heard that in AKS the API server endpoint can be made private. If we decide to make this private, how does this impact the developer connectivity to AKS; as well as our CI/CD connection to the AKS endpoint?

## The goal

Please present a solution architecture of how you recommend Contoso Insurance build their AKS clusters and run their application. Make sure you cover all of the requirements, and can explain why you made certain decisions.

## Hints 

* AKS baseline: https://learn.microsoft.com/en-us/azure/architecture/reference-architectures/containers/aks/baseline-aks
* AKS networking: https://learn.microsoft.com/en-us/azure/aks/concepts-network 



