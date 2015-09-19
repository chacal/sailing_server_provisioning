## Running locally

#### Install Ansible

    pip install ansible --upgrade

#### Install Vagrant

Download latest Vagrant from [http://www.vagrantup.com/downloads](http://www.vagrantup.com/downloads)

#### Upgrade paramiko

Paramiko 1.15.2 is required when using SSH connection to the Vagrant box with password authentication.

Check currently installed version:

    pip freeze | grep paramiko

Install (or update) to the latest version:

    pip install paramiko --upgrade

#### Start Vagrant box

    vagrant up

#### Run Ansible playbook

    ansible-playbook -i hosts site.yml -k     # use 'vagrant' as password

SSH host key checking can be disabled by setting ```ANSIBLE_HOST_KEY_CHECKING``` env variable to ```False```:

    export ANSIBLE_HOST_KEY_CHECKING=False
    ansible-playbook -i hosts site.yml -k     # use 'vagrant' as password