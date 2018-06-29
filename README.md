# DevOps

Project with tools to enable moving my server to the cloud. I am not sure whether would be useful for anybody but contributions are always welcome.

## The tools:
* Debian: https://www.debian.org/
* Ansible: https://www.ansible.com/
* Docker: https://www.docker.com/
* DebOps: http://debops.org
* Libvirt + Xen: https://libvirt.org/drvxen.html
* AWX - Ansible Tower Open Source https://github.com/ansible/awx

## The concept:
My intention is to use Ansible to create Docker images of different tools based on Debian. When possible Dockerfile will invoke an Ansible playbook that will configure as much as possible the environment and the tool. 

Also I want to be able to run many of the playbooks in AWX. I am defining two type of playbooks:
* Installation: Playbooks or manuals to install the operating system as I wish from a rescue/live cd/USB. 
* Maintenance: Playbooks or manuals that creates the necessary steps to perform normal operations, such as:
  * Restart a server: Providing the encryption keys
  * Perform backups
  * Add new VM
  * Update VM with latest software: In this case, depending of the software, I will probably create a playbook that will download the latest version of the software and run it in Docker, test that everything is correct and running and finally swap the docker image of production by the docker image updated. 
    Some software that I expect to use these capabilities are:
    * Wordpress
    * To be added more
    

