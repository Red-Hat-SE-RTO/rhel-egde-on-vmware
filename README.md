RHEL Edge VMWare Ansible role
=========

This project is an Ansible role to deploy to a rhel-edge instance to VCenter.


Requirements
------------
* install ansible collections
```
ansible-galaxy collection install -r collections/requirements.yml
```
* isntall pyvmomi
```
pip install pyvmomi
```

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    ---
    - hosts: localhost
      remote_user: root
      roles:
        - rhel-egde-on-vmware

How-To 
--------

To Deploy 

```
ansible-playbook -i inventory myplaybook.yml --extra-vars "@your_vars.yml"
```

Create foler and upload iso the vSphere
```
 ansible-playbook -i inventory myplaybook.yml --extra-vars "@your_vars.yml" -t vmware_create_folder,vmware_check_for_iso,vmware_upload_iso -vv
```


Create folder and upload iso the vSphere
```
 ansible-playbook -i inventory myplaybook.yml --extra-vars "@your_vars.yml" -t vmware_deploy_vms -vv
```

License
-------

BSD

Author Information
------------------

Tosin Akinosho

