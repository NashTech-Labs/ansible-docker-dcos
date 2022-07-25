### What will this role do ?

The above docker role will install docker to prepare the environment for dcos to use it  from tar file in your system and the machines on which you will run the role.

This role will configure docker to use overlay module and along with it will install all the docker dependent packages. 

The above role uses a task bootstrap.yml that downloads htttpd docker tar and loads it and likewise other tasks that download registry and marathon-lb docker.

In the roles there is a file that is being used called as configure-docker-daemon.sh. This script is executed on all the nodes of DCOS cluster

#### Variable used in the role.

- docker_version: 18.03.0 


### How to run the playbook .

To run the playbook follow the below command:-

`ansible-playbook -i <your inventory file> playbook.yml`

**Note**:-  If you are running on your local system then you don't need to pass inventory file. Just use localhost in hosts of playbook. 