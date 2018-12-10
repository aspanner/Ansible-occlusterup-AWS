Ansible playbooks to create an EC2 RHEL 7.x instance downloading and installing RHEL, OpenShift client, configuring the firewall and creating the oc cluster up start script 
with a public IP

Usage:

$ ansible-playbook create_ec2_instace.yml <BR>
this will create and populate the inventory.yml file with the public DNS of the instance <BR>

$ansible-playbook setup_oc_cluster_up.yml -i inventory.yml  --key-file < path to your ssh key file> <BR>
  This playbook will register the RHEL instance with the subscription manager, download & install necessary RPMs and other software (eg docker), configure docker to allow insecure registries, configure the RHEL firewall, start all necessary daemons and create the oc cluster up startscript to allow a publicly routable IP as well as storing the state during openshift restarts.

config options and description are in the header of the file.
<BR>
  
 After the playbooks ran successfully ssh into the machine with ec2-user eg ssh ec2-user@ec2-13-210-36-32.ap-southeast-2.compute.amazonaws.com -i <path to your keyfile> <BR>
  
  You will find the startup script at /home/ec2-user
  
