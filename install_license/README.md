Role Name
=========

Use this Role to Install the Product Support License with the ISAM Appliance.

Requirements
------------

start_config role is a required dependencies. It contains the Ansible Custom Modules 
and handlers. It also requires a valid license support file which can be obtained 
from IBM Password Advantage at https://www.ibm.com/software/passportadvantage/ 

Role Variables
--------------

Provide valid license support file location:
install_license_file: '/tmp/sds801-xxxxx-edition-activation-package.txt'

The role automatically takes a snapshot before installing the support license file, override as needed:
`install_license_comment: "Automated Snapshot Before Installing Product Support License"`

Dependencies
------------

start_config is a required role - since it contains the Ansible Custom Modules and Handlers.

Example Playbook
----------------

Here is an example of how to use this role:

    - hosts: servers
      connection: local
      roles:
         - role: install_license
           install_license_file: '/tmp/sds801-xxxxx-edition-activation-package.txt'

License
-------

Apache

Author Information
------------------

IFC
