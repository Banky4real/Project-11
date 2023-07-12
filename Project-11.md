## **Documentation for Project 11**

### Installing Ansible
`sudo apt update`

`sudo apt install ansible`
![Installing-Ansible](./Images/Ansible-installation.png)

### Configuring Jenkins Build Job to save repository content anytime an Update is made

### Creating a Freestyle Project Ansible

![Freestyle-Project-Ansible](./Images/Freestyle-Project-Ansible-Created-on-Jenkins.png)

### Configuring Webhook to Trigger Ansible Build Automatically

![Webhook-Configuration](./Images/Webhook-successfully-created-to-trigger-ansible-build.png)

### Configuring a Postbuild Job to Archive Artifacts

![Postbuild-Job-Configuration](./Images/Configuring-a-postbuild-job-to-archive-all-our-artifacts.png)

### Testing setup by Updating README File

### First Successful Build for Ansible

![1st-build-Success](./Images/1st-build-Success.png)

### Artifacts Saved Locally on Jenkins Server

![Artifacts-Saved-Locally](./Images/Artifacts-saved-locally-on-Jenkins-Server.png)

### Cloning Down ansible-config-mgt on ansible instance
`git clone https://github.com/Banky4real/ansible-config-mgt.git`

![ansible-config-mgt-Clone](./Images/Successful-Clone-of-ansible-config-mgt-repo-on-ansible-instance.png)

### Creating a new git Branch that will be used for the development of a new feature

![git-branch-created](./Images/Created-a-new-git-branch.png)

### Checking out the newly created feature branch to our local machine to start building code and directory structure

### Setting up ssh host config

![ssh-host-config](./Images/Config-file-for-remote-connection-on-Local-Machine.png)

### Successful Connection to remote host Jenkins ansible server

![Connected-to-Jenkins-ansible-server](./Images/Successful-connection-to-our-Jenkins-ansible-server.png)

### Checking out or switching to our newly created feature branch on our local machine

`git checkout -b feature/project-11-ansible`
![Successful-checkout-to-our-newly-created-feature-branch](./Images/Successful-checkout-to-our-newly-created-feature-branch-on-local-machine.png)

### Creating files and folders for the development of our new features

![Files-and-folders-creation](./Images/Creating-our-files-and-folders-for-the-development-of-a-new-feature.png)

### Setting up our Ansible inventory in order to be able to ssh into remote host to execute tasks

### Importing our control server private key into ssh agent

#### Initializing SSH agent
`eval `ssh-agent -s` `

#### Path to our control server (Jenkins Ansible Server) Private Key
`ssh-add /home/ubuntu/.ssh/id_rsa`
![Importing-our-private-key-into-ssh-agent](./Images/Importing-our-private-key-into-ssh-agent.png)

### Confirming our control server private key has been added to ssh agent

`ssh-add -l`

![Confirming-our-added-key](./Images/Confirming-our-added-key.png)

### SSH into webserver 1

`ssh -A ec2-user@3.86.167.125`

![ssh-into-webserver1-successful](./Images/Successful-ssh-into-webserver-1.png)

### Updating our Inventory/dev.yml with the Private Ip's of the target servers

` [nfs] `
` 172.31.93.135 ansible_ssh_user='ec2-user' `

` [webservers] `
` 172.31.88.170 ansible_ssh_user='ec2-user' ` 
` 172.31.94.194 ansible_ssh_user='ec2-user' `

` [db] `
` 172.31.92.231 ansible_ssh_user='ubuntu' `

` [lb] `
` 172.31.92.204 ansible_ssh_user='ubuntu' `

![Updating-inventory-yml-with-target-servers-private-ip's](./Images/Updating-inventory-yml-with-target-servers-private-ip's.png)

### Testing Connectivity to one of our target servers in the inventory dev.yml file by Pinging Load Balancer(lb), returned success

`ansible lb -m ping -i dev.yml`

![connectivity-test-by-ping-to-one-of-our-target-servers-load-balancer-returned-success](./Images/connectivity-test-by-ping-to-one-of-our-target-servers-load-balancer-returned-success.png)

### Testing Connectivity to all of our target servers in the inventory dev.yml file by Pinging all, returned success

`ansible all -m ping -i dev.yml`

![connectivity-test-by-ping-to-all-of-our-target-servers-returned-success.png](./Images/connectivity-test-by-ping-to-all-of-our-target-servers-returned-success.png)