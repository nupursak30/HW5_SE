# HW5

Solutions to the conceptual questions: [Answers](Answers.md)

_Pre-requisities:_ Vagrant and VirtualBox should already be installed in your machine.  
__Steps to run the Ansible Playbook:__
1. Create two folders in your local machine - 1)AnsibleVM 2)node1
2. Go to the __node1__ folder and run the following commands in it:
   1. vagrant init ubuntu/trusty64
   2. Uncomment and edit the following line in Vagrantfile:  
      __config.vm.network "private_network", ip: "192.168.33.40"__
   3. vagrant up
   4. vagrant ssh  
   You should be able to log into the node1VMwhen you perform step (4).Logout of node1VM using __exit__ command.You should be back in the __node1__ folder.
   5. Run __vagrant ssh-config__ command to get path of the private_key of node1, open it up and copy contents into textfile/clipboard.
3. Go to the __AnsibleVM__ folder and run the following commands in it:
   1. vagrant init ubuntu/trusty64
   2. Uncomment the following line in Vagrantfile:  
      __config.vm.network "private_network", ip: "192.168.33.10"__
   3. vagrant up
   4. vagrant ssh  
  Now you will be logged into the Ansible Virtual Machine(AnsibleVM) and so all the below commands need to be operated inside the AnsibleVM
   5. sudo apt-add-repository ppa:ansible/ansible
   6. sudo apt-get update
   7. sudo apt-get install ansible  
   The above steps install Ansible in the Virtual Machine
   8. Create a new file - 'inventory' that has the following contents:  
      __[nodes]
192.168.33.40 ansible_ssh_user=vagrant ansible_ssh_private_key_file=keys/node1.key__
    9. Create a new directory 'keys' in the current folder where inventory file is located and go into that folder.Create a new file __node1.key__ and paste the contents copied from step 2.(5) into this file.
    10. chmod 600 keys/node1.key  
    __Before running the below command,make sure that the HW5.yml playbook file is present in the same folder where inventory file is present__
    11. ansible-playbook HW5.yml -i inventory

Screencast demonstrating setup,tasks and running app: [Screencast](https://youtu.be/wmHob_sUuRM)
Another better quality link :[Screencast2](https://drive.google.com/open?id=1QnVfiLCRMw7sRI9_3uf0OZ7TH8jlHLkR)
