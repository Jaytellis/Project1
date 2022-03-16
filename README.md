**Automated ELK Stack Deployment**

The files in this repository were used to configure the network depicted below.

![alt text](https://github.com/Jaytellis/Project1/blob/main/Images/Elk_Deployment_Diagram.png)
These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the configuration file may be used to install only certain pieces of it, such as Filebeat.

[Filebeat Playbook](https://github.com/Jaytellis/Project1/blob/main/Ansible/Filebeat_Playbook.txt)

[Metricbeat Playbook](https://github.com/Jaytellis/Project1/blob/main/Ansible/Metricbeat_Playbook.txt)

[Install VM with Docker](https://github.com/Jaytellis/Project1/blob/main/Ansible/Install_Docker_Playbook.txt)

[Install Elk Playbook](https://github.com/Jaytellis/Project1/blob/main/Ansible/Install_Elk_Playbook.txt)

This document contains the following details:

- Description of the Topology

- Access Policies

- ELK Configuration

- Beats in Use

- Machines Being Monitored

- How to Use the Ansible Build

**Description of the Topology**

- The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.
- Load balancing ensures that the application will be highly available, in addition to limiting the exposure of backend servers directly to the network.
- Load Balancers contribute to the availability aspect of the CIA Triad
- JumpBox is used for System Administration and secured external network access. JumpBox is advantageous because it can be used for launching Administrative Tasks. The JumpBox Provisioner becomes a System Admin Workstation. Tasks will need to be completed while connected to the JumpBox. The JumpBox is also configured for limited access providing a secure network environment. 
- Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the filesystem and system resources.
  - Filebeat monitors log files or locations that have been configured. Filebeat also collects logs.
  - Metricbeat records metric and statistical data from the operating system and from the services running on the host servers. 

The configuration details of each machine may be found below.

![Image1](https://user-images.githubusercontent.com/91991300/158522833-8833fe4b-160c-4fd6-987e-fecef77cf0e5.png)

**Access Policies** 

The machines on the internal network are not exposed to the public Internet. 

Only the Jump-Box virtual machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- Admin's personal IP Address

Machines within the network can only be accessed by SSH

- Allowed Jump-Box Provisioner - IP 10.0.0.4

A summary of the access policies in place can be found in the table below.

![Image2](https://user-images.githubusercontent.com/91991300/158523176-bd503437-8388-4138-80bd-b13520ca9d1d.png)

**Elk Configuration**

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because:
- Ansible exercises automation and simplifies repetitive, complex, and tedious tasks. 

The playbook implements the following tasks:

- Install: docker.io
- Install: python3-pip
- Install: docker module
- Increase Memory Use: sysctl -w vm.max_map_count =262144

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![alt text](https://github.com/Jaytellis/Project1/blob/main/Images/Elk761.png)
