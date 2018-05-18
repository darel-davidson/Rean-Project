How I would have used Ansible(Please view Ansible defects to explain why this plan did not come to fruition) :
1.	Create EC2 Instance, Configure EC2 to create an instance with also installing Ansbile or use a specific cloudformation to have ansible already installed.
2.	Automatically download github playbooks to user EC2 instance.
3.	Have the user execute the ELK.yml playbook, which should trigger installation of Jenkins. Once Jenkins is installed the user can kick off the job to install ELK.

Ansible install:
1.	sudo easy_install pip
2.	sudo pip install ansible
3.	sudo yum update
4.	sudo yum-config-manager --enable epel
5.	yum repolist
6.	sudo yum install ansible
7.	sudo yum install git

