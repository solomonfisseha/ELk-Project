# ELk-Project
#These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the yml and config file may be used to install only certain pieces of it, such as Filebeat.



![GitHub](diagram.png)
* ![ansible config](https://github.com/the-Coding-Boot-Camp-at-UT/UTA-MCC-VIRT-CYBER-PT-03-2021-U-C/blob/main/Lesson%20Plans/13-Elk-Stack-Project/Activities/Stu_Day_1/Unsolved/Resources/ansible.cfg)
* make change: 
  remote_users: RedAdmin

* ![Ansible host file](https://github.com/the-Coding-Boot-Camp-at-UT/UTA-MCC-VIRT-CYBER-PT-03-2021-U-C/blob/main/Lesson%20Plans/13-Elk-Stack-Project/Activities/Stu_Day_1/Solved/Resources/hosts)
* ![installing ELk](https://github.com/the-Coding-Boot-Camp-at-UT/UTA-MCC-VIRT-CYBER-PT-03-2021-U-C/blob/main/Lesson%20Plans/13-Elk-Stack-Project/Activities/Stu_Day_1/Solved/Resources/install-elk.yml)
* ![Filebeat Configuration file](https://github.com/the-Coding-Boot-Camp-at-UT/UTA-MCC-VIRT-CYBER-PT-03-2021-U-C/blob/main/Lesson%20Plans/13-Elk-Stack-Project/Activities/Stu_Day_2/Solved/config_files/filebeat-configuration.yml)
 # make change: 
    output.elasticsearch:
    hosts: ["10.1.0.4:9200"]
    username: "elastic"
    password: "changeme"
    .....
    setup.kibana:
    host: "10.1.0.4:5601"
   
   
   
* ![filebeat Playbook](https://github.com/the-Coding-Boot-Camp-at-UT/UTA-MCC-VIRT-CYBER-PT-03-2021-U-C/blob/main/Lesson%20Plans/13-Elk-Stack-Project/Activities/Stu_Day_2/Solved/config_files/filebeat-playbook.yml)
* ![Metricbeat Configuration File](https://github.com/the-Coding-Boot-Camp-at-UT/UTA-MCC-VIRT-CYBER-PT-03-2021-U-C/blob/main/Lesson%20Plans/13-Elk-Stack-Project/Activities/Stu_Day_2/Solved/config_files/metricbeat-configuration.yml)
 # make change: 
    output.elasticsearch:
    hosts: ["10.1.0.4:9200"]
    username: "elastic"
    password: "changeme"
    .......
    setup.kibana:
    host: "10.1.0.4:5601"

* ![Meatricbeat playbook](https://github.com/the-Coding-Boot-Camp-at-UT/UTA-MCC-VIRT-CYBER-PT-03-2021-U-C/blob/main/Lesson%20Plans/13-Elk-Stack-Project/Activities/Stu_Day_2/Solved/config_files/metricbeat-playbook.yml)
## This document contains the following details:
* Description of the Topology
* Access Policies
* ELK Configuration
* Beats in Use
* Machines Being Monitored
* How to Use the Ansible Build
## Description of the Topology
- The main purpose of the network is to expose a load-balanced and monitored instance of DVWM, the D*mn Vulnerable Web Application.
- Load balancing ensures that the application will be highly available, in addition to restricting traffic to the network.
- Load balancer can add additional layers of security without any changes to the application. It portects websites form hackers and includes daily rule updates.
- The advantage of Jumb Box are easlily to control remote desktop connectivity, to restrict the IP address to communicate with secure environment and prevents the Azure VMs from exposing to the puplic.
- Integrating an ELK Server allows users to easily monitor the vulnerable VMs for changes to the data and system logs.
- Filebeat watches and monitors the log files or locations that users specify, collects log events, and forwards them either to Elasticsearch or Logstash for indexing. It is a lightweight shipper for forwarding and centeralizing log data.
- Metricbeat is a lightweight shipper that records and periodically collects metrics from the operationg system and from services running on the server and takes the metrics and statistics that it collects and ships them to the output that users specify, such as Elasticsearch or Logstash.
 -The configuratioon details of each machine may be found below.

## Access Policies
- The machines on the internal network are not exposed to the public Intersnet.
- Only the Jumb Box machine can accept connections from the Internet. Acess to this machine is only allowed from following IP addresses:13.72.75.41.
- Machines within the network can only be accessed by workstation and Jumb-Box.
 -The machine that allow to access ELK VM:
* Jumb-Box: 10.0.0.4/22
* workstation: TCP 5601
- A summary of the access policies in place can be found in the table below.
## ELK Configuration
- Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because Ansible lets you quickly and easily deploy multi tier apps. It helps from doing the same prosedure everytime on the IT administration and save us a lot of time.
- the steps of the ELK installation play:
  
      # Use pip module
      - name: Install Docker Python Module
        pip:
          name: docker
          state: present
      - name: Install docker.io
        apt:
          update_cache: yes
          name: docker.io
          state: present
      - name: download and launch a docker elk containers
        docker_container:
          name: elk
          image: sebp/elk:761
          state: started
          restart_policy: always
          published_ports:
             - 5601:5601
             - 9200:9200
             - 5044:5044
         - name: Increase virtual memory
            command: sysctl -w vm.max_map_count=262144
        
      
    



 




