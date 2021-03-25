# HAProxy - Ansible Playbook

Ansible Playbook to launch AWS Infrastructure to Configure Reverse Proxy (i.e. HAProxy) and update it's configuration file automatically with IP of webserver instances launched  

## Prerequisites
- Ansible should be installed and configured  
- AWS CLI should be installed and configured  

## Usage
- Clone or Download the Repository  
- Update ansible.cfg 

        [defaults]
        inventory=/etc/ansible/hosts/myhosts.txt
        host_key_checking = false
        remote_user = ec2-user
        private_key_file = /etc/ansible/webenvkey.pem
        ask_pass = false
        become = true


        [privilege_escalattion]
        become = true
        become_user = root
        become_method = sudo
        become_ask_pass = false

- Add [loadbalancer] and [webserver] groups in inventory

        [loadbalancer]


        [webserver]
  
- Update variables in playbook accordingly
- Finally run setup-haproxy.yaml using 'ansible-playbook setup-haproxy.yaml' command  

## Links

[Click here for Video and Post](https://www.linkedin.com/in/amanjhagrolia143/)
  
***Feel free to Contact!!***

<a href="https://www.linkedin.com/in/amanjhagrolia143" target="_blank"> <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" /> </a> 
