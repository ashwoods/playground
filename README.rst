Playground - set of scripts for trying out different architectures
==================================================================



Base ansible script for setting up a docker environment with some devop tools

- elkstack
- teamcity with postgresql


Requirements on source machine
------------------------------

- ansible 
- dochang.docker, 1.0.0 (galaxy)
- geerlingguy.security, 1.3.0 (galaxy)


Ansible galaxy roles
--------------------

It's a good idea run the script after a fresh manual upgrade. Furthermore you need:

- a gatekeeper user with passwordless sudo rights and your deploy key in authorized hosts (default:heimdall)
- python



Run the ansible playbook on the target
--------------------------------------

To run the script, just run ansible on the target:
    
    ansible-playbook "-e 'EV_KEY=EV_VALUE'" host.yml  // -- if using an inventory -- //

    or:

    ansible-playbook -i "XXX.XXX.XXX.XXX," --extra-vars "EV_KEY=EV_VALUE" host.yml
    
 Note: XXX.XXX.XXX.XXX IP address or host, do not forget the trailing `,` if only specifiying one host.
 Currently not using any configurable Environment variables
    
    
