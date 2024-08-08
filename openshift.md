# Installation of OpenShift Container Platform 4

## Overview

OpenShift Container Platform (OCP) 4 is a Kubernetes-based container orchestration platform developed by Red Hat. It provides a powerful foundation for building, deploying, and managing containerized applications. The installation of OCP 4 can be achieved through two primary methods: Installer-Provisioned Infrastructure (IPI) and User-Provisioned Infrastructure (UPI).

## Installation Methods

### Installer-Provisioned Infrastructure (IPI)

IPI is designed to simplify the installation process by automating the provisioning of the underlying infrastructure. This method leverages the OpenShift installer to create and configure the necessary resources, such as virtual machines (VMs), networking, and storage. The IPI method is ideal for users who want a quick and straightforward deployment process.

#### Steps for IPI Installation:

1. **Prepare the Environment**:
   - Ensure that you have the necessary privileges to create resources in your target cloud or bare-metal environment.
   - Set up DNS records for the cluster. This includes records for the API server and wildcard records for applications.

2. **Obtain the OpenShift Installer**:
   - Download the OpenShift installer binary from the Red Hat OpenShift Cluster Manager portal.

3. **Create the Installation Configuration**:
   - Run the OpenShift installer to generate the installation configuration files. This typically involves executing the `openshift-install create install-config` command and providing details such as the cluster name, base domain, and platform-specific settings.

4. **Deploy the Cluster**:
   - Execute the `openshift-install create cluster` command to start the installation process. The installer will provision the necessary infrastructure, deploy the OpenShift components, and configure the cluster.

5. **Monitor the Installation**:
   - Monitor the installation progress through the installer logs. The process can take several minutes to complete, depending on the infrastructure and network conditions.

6. **Post-Installation Configuration**:
   - Once the installation is complete, perform any necessary post-installation steps, such as configuring storage, setting up additional networking, and integrating with existing systems.

### User-Provisioned Infrastructure (UPI)

UPI gives users greater control and flexibility over the infrastructure setup by requiring manual provisioning of the underlying resources. This method is suited for environments where specific configurations are needed or where the infrastructure must adhere to custom requirements.

#### Steps for UPI Installation:

1. **Prepare the Environment**:
   - Set up the necessary infrastructure components, including VMs, networking, and storage. This typically involves creating VMs for the master and worker nodes, configuring load balancers, and ensuring that the required ports are open.

2. **Set Up DNS**:
   - Configure DNS records for the cluster. Ensure that the API server and wildcard application records are correctly set up.

3. **Obtain the OpenShift Installer**:
   - Download the OpenShift installer binary from the Red Hat OpenShift Cluster Manager portal.

4. **Create the Installation Configuration**:
   - Run the OpenShift installer to generate the installation configuration files using the `openshift-install create install-config` command. Provide the necessary details, including the cluster name, base domain, and platform-specific settings.

5. **Manually Provision the Infrastructure**:
   - Using the generated configuration files, manually set up the infrastructure. This includes creating the master and worker nodes, configuring the load balancers, and setting up networking.

6. **Deploy the Cluster**:
   - Execute the `openshift-install create cluster` command to begin the installation. The installer will deploy the OpenShift components and configure the cluster based on the manually provisioned infrastructure.

7. **Monitor the Installation**:
   - Keep track of the installation process through the installer logs. Ensure that all components are correctly deployed and configured.

8. **Post-Installation Configuration**:
   - After the installation is complete, perform any additional configuration required for your environment. This may include setting up persistent storage, configuring network policies, and integrating with existing systems.

## Conclusion

Installing OpenShift Container Platform 4 can be accomplished through either the IPI or UPI methods, each catering to different needs and levels of control. IPI offers a streamlined, automated approach, while UPI provides greater flexibility for custom infrastructure setups. Understanding the steps involved in each method ensures a successful and efficient deployment of your OpenShift clusters.
