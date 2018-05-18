
How I would have used Jenkins (Please view Jenkins defects to view how this plan did not come to fruition)
  1. Install Jenkins on EC2 instance manually by running install commands.
  2. Use Jenkins to connect to EC2 instance. 
  3. Create a job in Jenkins to install ansible.
  4. The same job would also use pre-created ansible playbooks to install ELK on each instance the user asks to be created.

Jenkins install:
  1. sudo wget -O/etc/yum.repos.d/jenkins.repo http://pkg.jenkins-ci.org/redhat/jenkins.repo
  2. sudo rpm --import https://pkg.jenkins.io/redhat/jenkins.io.key
  3. sudo yum install jenkins -y
  4. sudo service jenkins start

If Jenkins does not load on its own: Connect to http://<your_server_public_DNS>:8080 
  1. Admin password can be retrieved via command line:
     sudo cat /var/lib/jenkins/secrets/initialAdminPassword

Configure Jenkins:
  1. On the left, click Manage Jenkins, and then click Manage Plugins.
  2. Click on the Available tab, and then enter Amazon EC2 plugin, install. Or check Installed to see if AEC2 already installed.
  3. Once the installation is done back to Manage Jenkins, and then Configure System.
  4. Access 'Cloud':
    a. Add a new cloud, and select Amazon EC2. 


