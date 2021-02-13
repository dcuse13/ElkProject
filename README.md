## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![](https://github.com/dcuse13/ElkProject/blob/main/Images/CSDIAGRAM.png?raw=true)

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
- Description of the Topologu
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
| Jump Box | Gateway  | 10.0.0.1   | Linux            |
| TODO     |          |            |                  |
| TODO     |          |            |                  |
| TODO     |          |            |                  |

### Access Policies

The machines on the internal network are not exposed to the public Internet.

Only the _____ machine can accept connections from the Internet. Access to this machine is only allowed from the following IP ad>
- _TODO: Add whitelisted IP addresses_

Machines within the network can only be accessed by _____.
- _TODO: Which machine did you allow to access your ELK VM? What was its IP address?_

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes/No              | 10.0.0.1 10.0.0.2    |
|          |                     |                      |
|          |                     |                      |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous be>
- _TODO: What is the main advantage of automating configuration with Ansible?_

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...
- ...

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![TODO: Update the path with the name of your screenshot of docker ps output](Images/docker_ps_output.png)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_

We have installed the following Beats on these machines:
- _TODO: Specify which Beats you successfully installed_

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., >

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control>

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install th>
- _Which URL do you navigate to in order to check that the ELK server is running?

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._
