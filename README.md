Ansible playbooks to create an EC2 RHEL 7.x instance downloading and installing RHEL, OpenShift client, configuring the firewall and creating the oc cluster up start script 
with a public IP

Usage:

$ ansible-playbook create_ec2_instace.yml 
this will create and populate the inventory.yml file with the public DNS of the instance

$ansible-playbook setup_oc_cluster_up.yml -i inventory.yml  --key-file < path to your ssh key file>

config options and description are in the header of the file.
