#  💻Terraform Azure Virtual Machine with SSH Access

------------
BY: Sebastian navia

------------
<h2 align="center">Overview</h1>

<p align="justify"> This repository contains Terraform configuration files to deploy a virtual machine (VM) on Microsoft Azure cloud platform. The main purpose of this deployment is to showcase how to create a VM instance using Terraform and enable SSH access to it. </p>

<h2 align="center">Description</h1>

#### In the main file, we will find:

* **Resource Group**: Creates an Azure resource group where all the resources will reside.

* **Virtual Network**: Sets up a virtual network (VNet) to provide network connectivity for the VM.

* **Subnet**: Defines a subnet within the virtual network to segment the network traffic.

* **Public IP Address**: Allocates a static public IP address for the VM to allow external connectivity.

* **Network Security Group**: Configures a network security group to control inbound and outbound traffic to the VM.

* **Network Interface**: Creates a network interface for the VM, which connects it to the virtual network.

* **Network Security Rule**: Defines a network security rule to allow SSH traffic (TCP port 22) to the VM.

Additionally, the script provisions the Azure virtual machine itself with the following specifications:

* **Size**: Specifies the VM size as "Standard_DS1_v2" (adjustable based on requirements).

* **Operating System**: Uses an Ubuntu Server image from Canonical with the latest LTS version.

* **OS Disk**: Configures the operating system disk with caching, managed disk type, and creates it from the specified image.

* **OS Profile**: Sets the computer name, admin username, and admin password for logging into the VM.

* **Linux Configuration**: Enables password authentication for the Linux OS profile.


> NOTE
* Ensure that the admin_username and admin_password fields in the os_profile section are appropriately set to your desired values.

> Use the same credentials to create this virtual machine and avoid errors, as it is a practice resource.

------------


------------


------------


####Finally, we proceed to create it with the Terraform commands.
1. **terraform init**: Initializes the Terraform environment.

2. **terraform validate**: Validates the syntax and configuration of Terraform files.

3. **terraform plan**: Generates a plan of infrastructure changes.

4. **terraform fmt**: Applies consistent formatting to Terraform code.

5. **terraform apply**: Applies the changes defined in Terraform files.

------------

> "It is demonstrated that the resource has been created."
------------
![image](https://github.com/Sebastianavia/VM-ssh-Terraform-AZ/assets/71205906/e36785e3-90ab-40e4-b22c-13d065a8953e)
------------
![image](https://github.com/Sebastianavia/VM-ssh-Terraform-AZ/assets/71205906/8bd42c18-b9d6-4cf0-8de1-0271872d6aca)
------------
> SSH active
------------
![image](https://github.com/Sebastianavia/VM-ssh-Terraform-AZ/assets/71205906/27bf0b4b-26e0-4f13-aed6-3b1421b9185e)

------------


<h2 align="center">Resources</h1>
* [Terraform - virtual machine.](http://https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/virtual_machine#ssh_keys "Terraform - virtual machine.")






