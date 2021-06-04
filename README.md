# ELk-Project
#These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the yml and config file may be used to install only certain pieces of it, such as Filebeat.



![GitHub](diagram.png)
![ansible config](https://github.com/the-Coding-Boot-Camp-at-UT/UTA-MCC-VIRT-CYBER-PT-03-2021-U-C/blob/main/Lesson%20Plans/13-Elk-Stack-Project/Activities/Stu_Day_1/Unsolved/Resources/ansible.cfg)
 make change: remote_user = RedAdmin
![Ansible host file](https://github.com/the-Coding-Boot-Camp-at-UT/UTA-MCC-VIRT-CYBER-PT-03-2021-U-C/blob/main/Lesson%20Plans/13-Elk-Stack-Project/Activities/Stu_Day_1/Solved/Resources/hosts)
![installing ELk](https://github.com/the-Coding-Boot-Camp-at-UT/UTA-MCC-VIRT-CYBER-PT-03-2021-U-C/blob/main/Lesson%20Plans/13-Elk-Stack-Project/Activities/Stu_Day_1/Solved/Resources/install-elk.yml)
* ![Filebeat Configuration file](https://github.com/the-Coding-Boot-Camp-at-UT/UTA-MCC-VIRT-CYBER-PT-03-2021-U-C/blob/main/Lesson%20Plans/13-Elk-Stack-Project/Activities/Stu_Day_2/Solved/config_files/filebeat-configuration.yml)
   make change: 
   output.elasticsearch:
   hosts: ["10.1.0.4:9200]
   username: "elastic"
   password: "changeme"
   
   setup.kibana:
   host: "10.1.0.4:5601"
   
* ![filebeat Playbook](https://github.com/the-Coding-Boot-Camp-at-UT/UTA-MCC-VIRT-CYBER-PT-03-2021-U-C/blob/main/Lesson%20Plans/13-Elk-Stack-Project/Activities/Stu_Day_2/Solved/config_files/filebeat-playbook.yml)
* ![Metricbeat Configuration File]https://github.com/the-Coding-Boot-Camp-at-UT/UTA-MCC-VIRT-CYBER-PT-03-2021-U-C/blob/main/Lesson%20Plans/13-Elk-Stack-Project/Activities/Stu_Day_2/Solved/config_files/metricbeat-configuration.yml)
  make change: 
   output.elasticsearch:
   hosts: ["10.1.0.4:9200]
   username: "elastic"
   password: "changeme"
   
   setup.kibana:
   host: "10.1.0.4:5601"
   
* ![Meatricbeat playbook](https://github.com/the-Coding-Boot-Camp-at-UT/UTA-MCC-VIRT-CYBER-PT-03-2021-U-C/blob/main/Lesson%20Plans/13-Elk-Stack-Project/Activities/Stu_Day_2/Solved/config_files/metricbeat-playbook.yml)
## Automated ELK Stack Deployment


