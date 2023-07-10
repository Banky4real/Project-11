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

### Creating files and folders for the development of our new features

![Files-and-folders-creation](./Images/Creating-our-files-and-folders-for-the-development-of-a-new-feature.png)

### Checking out the newly created feature branch to our local machine to start building code and directory structure

### Setting up ssh host config

![ssh-host-config](./Images/Config-file-for-remote-connection-on-Local-Machine.png)

### Successful Connection to remote host Jenkins ansible server

![Connected-to-Jenkins-ansible-server](./Images/Successful-connection-to-our-Jenkins-ansible-server.png)

### Checking out or switching to our newly created feature branch on our local machine

`git checkout -b feature/project-11-ansible`
![Successful-checkout-to-our-newly-created-feature-branch](./Images/Successful-checkout-to-our-newly-created-feature-branch-on-local-machine.png)