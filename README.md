ANSIBLE-ROLE-SUDO
=================

Ansible role add sudo user in group with sudo NOPASSWORD access.



## Howto use this role?
This role need to be include in a playbook. 

Call this **Galaxy** role  like this:

````bash
ansible-galaxy install -r requirements.yml 
````

Inside requirements.yml
````yaml
# from GitHub, overriding the name and specifying a specific tag
- src: redbeard28.sudo
````

More info => [Ansible Docs](https://docs.ansible.com/ansible-container/roles/access.html)

## Requirements

 * Ansible 2.9+


Role Variables
--------------

```yaml
---
sudoers:
  - {name: 'riri', sudouser_append: true}
  - {name: 'fifi', sudouser_append: true}
  - {name: 'loulou', sudouser_append: true}

sudoes_group: 'wheel'
```

Dependencies
------------

  * redbeard28.groups
  * redbeard28.users

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - { role: redbeard28.sudo, tags: mytags }


Molecule testing framework
--------------------------

You can use molecule to test this role.
```bash
image=debian tag="buster" molecule converge 
image=debian tag="buster" molecule verify 
```

Author Information
------------------

Jeremie CUADRADO[¹](mailto:info@redbeard-consulting.fr) from Redbeard-Consulting
