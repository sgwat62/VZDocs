# Cloud Management Reference Architecture v1.0

##Summary

The purpose of this document is to define a standard working implementation of the RHEL Cloud Management Architecture using the following RedHat products;

- Cloudforms 4.5
- Ansible Tower 3.1.4
- Openshift 3.5

This document will define basic use cases and the integration and configuration of the RHEL product components.  We recognize there are a number of different ways to do several of these processes.  We have consolidated it down to a

##Use Cases:
- Successfully Launch a simple VM from a Catalog Item
- Successfully Launch a Catalog Bundle to deploy a VM and run an Ansible Playbook against it
- Successfully Launch an Openshift Cluster
- Add & remove nodes from the Openshift Cluster 
- Configure VM Analysis
- Unregister VM's at shutdownovider and configure Hawkular (Create a Playbook(s))
- Configure Openshift Reporting
- Bonus: Automate adding Openshift Cluster to CloudForms as a Container Provider


## 



