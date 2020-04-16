# stegotorus_deployer
Deploying Stegotorus Bridges by Using Ansible Scripts

Here are the steps to go for installing the ansible scripts for deploying the Stegotorus bridges: 

(1) Make sure that you have ssh access to your server. The server is tested with Debian OS. 

(2) Install locally the ansible software (version 2.2.1.0 or later) 

Add the following line to /etc/apt/sources.list:

deb http://ppa.launchpad.net/ansible/ansible/ubuntu trusty main

 sudo apt add-repository ppa:ansible/ansible 

Then run these commands:

  sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 93C4A3FD7BB9C367
  
  sudo apt update
  
  sudo apt install ansible
  
  sudo ansible --version 

For more information, check the guide: https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html 

(3) Download all the stegotorus_deployer files and move them to the folder ansible-platform 

(4) In hosts -> add the IP of your server on line 1 

(5) In playbook.yml -> add the port and the steg_mod (there are example values already written, but your port to the server may be different, examples of steg_mod are listed in the file itself)

(6) Finally, run the following command from the command line (from inside the ansible-platform folder):  

   ansible-playbook -K playbook.yml -vvvv 
