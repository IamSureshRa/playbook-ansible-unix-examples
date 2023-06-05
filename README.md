# playbook-ansible-unix-examples
Ansible Playbook Examples - Unix

Structure (merger of best practices)
------------------------------------

```
ansible.cfg
collections/
    collection1/
    requirements.yml # not required if present in root
defaults/
    main.yml
files/
filter_plugins/
handlers/
    main.yml
inventories/
    production/
        hosts               # inventory file for production servers
        group_vars/
            group1.yml       # here we assign variables to particular groups
            group2.yml
        host_vars/
            hostname1.yml    # here we assign variables to particular systems
            hostname2.yml

    staging/
        hosts               # inventory file for staging environment
        group_vars/
            group1.yml       # here we assign variables to particular groups
            group2.yml
        host_vars/
            stagehost1.yml   # here we assign variables to particular systems
            stagehost2.yml
library/
meta/
    main.yml
module_utils/
playbooks/
    deprovision.yml
    provision.yml
roles/
    common/
    webtier/
    monitoring/
    fooapp/
    requirements.yml # not required if present in root
README.md
requirements.yml # optional
site.yml
tasks/
    main.yml
templates/
tests/
    ansible.cfg
    inventory
    test.yml
vars/
    main.yml
```
