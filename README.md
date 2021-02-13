## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![](https://github.com/dcuse13/ElkProject/blob/main/Images/CSDIAGRAM%20(2).png?raw=true)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire>

  * [Ansible Playbook](https://github.com/dcuse13/ElkProject/blob/main/Ansible/Ansible%20Playbook)
  * [Ansible Config](https://github.com/dcuse13/ElkProject/blob/main/Ansible/Ansible%20Config)
  * [Ansible Hosts](https://github.com/dcuse13/ElkProject/blob/main/Ansible/hosts) 
  * [Filebeat Playbook](https://github.com/dcuse13/ElkProject/blob/main/Ansible/Filebeat%20Playbook)
  * [Filebeat Config](https://github.com/dcuse13/ElkProject/blob/main/Ansible/Filebeat%20Config)
  * [Metricbeat Playbook](https://github.com/dcuse13/ElkProject/blob/main/Ansible/Metricbeat%20Playbook)
  * [Metricbeat Config](https://github.com/dcuse13/ElkProject/blob/main/Ansible/Metricbeat%20config)
  * [ELK Install](https://github.com/dcuse13/ElkProject/blob/main/Ansible/InstallElk)

This document contains the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Applicatio>

Load balancing ensures that the application will be highly available, in addition to restricting traffic to the network.
  * What aspect of security do load balancers protect? 
     
     Answer: Web Traffic / Web Security / Availability
         
  * What is the advantage of a jump box?
     
     Answer: Access Control / Automation / Network Segmentation
     
Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the logs and system traffic.
 * What does Filebeat watch for? 
 
   Answer: Filebeat watches for log files or locations you specify and forwards them for indexing.
 
 * What does Metricbeat record?
 
   Answer: Metricbeat records metrics and statistics and sends the data to an output you specify, such as Elasticsearch. 

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

| Name     | Function | IP Address | Operating System |
|----------|----------|------------|------------------|
| Jump Box | Gateway  | 10.0.0.4   | Linux            |
| Web1     | Webserver         | 10.0.0.5           | Linux                 |
| Web2     | Webserver         | 10.0.0.6           | Linux                 |
| Elk      | Elk Server         | 10.1.0.4           | Linux                 |
| Load Balancer     | Load Balancer         | Static IP           | Linux                 |
| Workstation     | Access Control         | Public IP           | Linux                  |

### Access Policies

The machines on the internal network are not exposed to the public Internet.

Only the Elk Server machine can accept connections from the Internet. Access to this machine is only allowed from the following IP ad>
* Workstation Public IP through TCP 5601

Machines within the network can only be accessed by the Workstation and JumpboxVM.
* JumpBoxVM - 10.0.0.4 | 52.142.61.247
* Workstation - Public IP

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | No                  | Public IP    |
| Web1         | No                  | 10.0.0.4                     |
| Web2         | No                  | 10.0.0.4                     |
| Elk Server         | No                  | Public IP                     |
| Load Balancer         | No                  | Public IP                     |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous be>
* What is the main advantage of automating configuration with Ansible?

  Answer: By writing a playbook w/ a list of tasks, you will not have to write custom scripts to automate your systems. 

The playbook implements the following tasks:
 
 * Increasing System Memory
 
 * Download and Configure Containers
 
 * Launch and expose the container

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![](https://github.com/dcuse13/ElkProject/blob/main/Images/DockerPS.png?raw=true)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:

* WEB1 - 10.0.0.5
* WEB2 - 10.0.0.6

We have installed the following Beats on these machines:

* WEB1 - 10.0.0.5
* WEB2 - 10.0.0.6

These Beats allow us to collect the following information from each machine:

* Filebeat will allow us to collect logs events and Metricbeat witl collect system metrics & statisitics

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control>

SSH into the control node and follow the steps below:
- Copy the filebeat-config.yml file to filebeat-playbook.yml.
- Update the filebeat-playbook.yml file to include...
- Run the playbook, and navigate to http://104.209.128.31:5601/app/kibana#/home to check that the installation worked as expected.

BONUS:

| Purpose     | Command          | 
|----------|---------------------|
| SSH into Machine | ssh azureuser@10.0.0.4                  |
| Locate Ansible Container | sudo docker container list -a                  |
| Start Container | sudo docker start container_name                  |
| Launch Container | sudo docker attach container_name                  |
| List Containers | sudo docker ps -a                  |


