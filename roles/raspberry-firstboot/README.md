Raspberry FirstBoot
=========

An Ansible role to run just once, when a pile of Raspberry Pi is booted for the first time or has been reset.

It removes the known SSH keys from the local known_hosts file and copies the local SSH key to the Raspberry Pis.


Requirements
------------

Raspberry Pi computers
A SSH key already generated.

Role Variables
--------------

None.

Dependencies
------------

None.

Example Playbook
----------------


    - hosts: all
      gather_facts: no
      vars:
        ansible_python_interpreter: /usr/bin/python3
        ansible_user: pi
        ansible_become: no
      roles:
         - raspberry_firstboot


* `gather_facts` is `no` because if the old SSH keys are still present, nothing runs.
* `ansible_become` is `no` to avoid setting the ownership of the user's `known_hosts` file to root.


License
-------

BSD

Author Information
------------------

Dominique Comte.
