Role Name
=========

Ansible role for installing vagrant and providers.

Requirements
------------

Fedora 24 or later.

Role Variables
--------------

- provider_libvirt: Install libvirt as vagrant provider.

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: localhost
      become: yes
      become_method: sudo
    
      vars:
        provider_libvirt: true
    
      roles:
      - ansible-vagrant


License
-------

MIT

