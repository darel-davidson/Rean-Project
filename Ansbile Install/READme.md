How I would have used Ansible(Please view Ansible defects to explain why this plan di not come to frutiion :
I struggled here as well, after installing ansible I was able to create plays to run installs, but for any play that require user input I was unable to automate that and therefore could not complete this plan either, however here is an outline of my second plan:
1. Create EC2 Instance, Configure EC2 to create an instance with also installing ansbile or use a specific cloudformation to have ansible already installed.
2. Automatically download github playbooks to user EC2 instance.
3. Have the user execute the ELK.yml playbook, which should trigger installation of Jenkins. Once Jenkins is installed the user can kick off the job to install ELK.

Defects:
1. Longstash yml not completed.
2. I wanted to created ansible playbook to check which version of java is currently installed if less than 1.8:
 a. sudo yum install java-1.8.0-openjdk-devel
 b. sudo /usr/sbin/alternatives --config java
 c. 2
--Example -> Check Java version.
-- This failed after not being able to automate the user input requested from java install.
