## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

- [Diagram](./Diagram/Diagram.pdf) 

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the _____ file may be used to install only certain pieces of it, such as Filebeat.

 - [YAML-Playbook](./Ansible/YAML-Playbook.yml)

This document contains the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly available or redudancy, in addition to restricting access to the network.

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the file and system log.

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

| Machine  	| Role    	| Local IP 	| OS    	| Public IP     	|
|----------	|---------	|----------	|-------	|---------------	|
| Jump Box 	| Gateway 	| 10.0.0.4 	| Linux 	| 13.64.172.153 	|
| Web-01   	| Server  	| 10.0.0.5 	| Linux 	|               	|
| Web-02   	| Server  	| 10.0.0.6 	| Linux 	|               	|
| Web-03   	| Server  	| 10.0.0.7 	| Linux 	|               	|
| Elk      	| Server  	| 10.1.0.4 	| Linux 	| 13.64.172.153 	|

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the Jump Box machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- 50.188.201.133

Machines within the network can only be accessed by Jump Box with internal IP 10.0.0.4.

A summary of the access policies in place can be found in the table below.

| Machine  	| Publicly Accessible 	| Allowed IP Address 	|
|----------	|---------------------	|--------------------	|
| Jump Box 	| Yes                 	| 50.188.201.133     	|
| Web-01   	| No                  	| 10.0.0.0/24        	|
| Web-02   	| No                  	| 10.0.0.0/24        	|
| Web-03   	| No                  	| 10.0.0.0/24        	|
| Elk      	| Yes                 	| 50.188.201.133     	|

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because consistent, void human error

The playbook implements the following tasks:
- Install docker
- Install pip3
- Install docker python module
- Use more memory
- Download and launch a docker elk container
- Enable service docker on boot

The following screenshot displays the result of running [docker-ps](./Diagram/docker-ps.PNG) after successfully configuring the ELK instance.

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_

We have installed the following Beats on these machines:
- _TODO: Specify which Beats you successfully installed_

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_
- _Which URL do you navigate to in order to check that the ELK server is running?

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._
