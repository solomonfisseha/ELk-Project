# ELk-Project
#These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the yml and config file may be used to install only certain pieces of it, such as Filebeat.



![GitHub](diagram.png)


* ![Metricbeat Configuration File](https://gist.githubusercontent.com/slape/58541585cc1886d2e26cd8be557ce04c/raw/0ce2c7e744c54513616966affb5e9d96f5e12f73/metricbeat)
## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![TODO: Update the path with the name of your diagram](Images/diagram_filename.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the yml and config file may be used to install only certain pieces of it, such as Filebeat.

  - _TODO: Enter the playbook file._
Ansible configuration
For editing: nano ansible.cfg   change remote_user = RedAdmin
Ansible hosts
Ansible playbook
Ansible ELK Installation and VM configuration
Ansible filebeat config file
[playbook.yml](https://github.com/the-Coding-Boot-Camp-at-UT/UTA-MCC-VIRT-CYBER-PT-03-2021-U-C/blob/main/Lesson%20Plans/13-Elk-Stack-Project/Activities/Stu_Day_2/Solved/config_files/filebeat-playbook.yml)
Ansible metricbeat config file
Ansible metricbeat playbook


This document contains the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly available, in addition to restricting traffic to the network.
- _TODO: What aspect of security do load balancers protect? 
answer: availability, Web Traffic, Web Security
What is the advantage of a jump box?_answer: automation, security, network segmentation, access control

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the data and system logs.
- _TODO: What does Filebeat watch for?_filebeat monitors the log files or locations that you specify, collects log events, and forwards them either to elasticsearch or logstash for indexing.
- _TODO: What does Metricbeat record?_metricbeat takes the metrics and statistics that it collects and ships them to the output that you specify, such as elasticsearch and logstash.

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.






