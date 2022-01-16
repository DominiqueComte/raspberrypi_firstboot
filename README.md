Raspberry FirstBoot Ansible Playbook
=========

An Ansible Playbook for when a pile of Raspberry Pi is booted for the first time or has been reset.

It removes the known SSH keys from the local known_hosts file and copies the local SSH key to the Raspberry Pis using the default SSH password.


Requirements
------------

- A Linux computer that runs Ansible.
- A SSH key already generated locally.
- Raspberry Pi computer(s) to connect to remotely.


Role Variables
--------------

None.

Dependencies
------------

None.

Example Playbook
----------------

See setup.yml file.

    - hosts: all
      gather_facts: no
      vars:
        ansible_python_interpreter: /usr/bin/python3
        ansible_user: pi
        ansible_become: no
      roles:
         - raspberry_firstboot


License
-------

BSD

Author Information
------------------

Dominique Comte.
