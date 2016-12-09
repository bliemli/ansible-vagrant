Role Name
=========

Ansible role for installing vagrant and plugins.

Requirements
------------

Fedora 24 or later.

Role Variables
--------------

vagrant_plugins: Choose which vagrant plugins to install. Available but not limited to:

- lxc
- libvirt
- cachier
- hostmanager
- registration
- sshfs
- digitalocean
- adbinfo

If there's a plugin missing in this list and it has a package named "vagrant-{{ plugin_name }}" available in the distro's official repos, you can simply add it to the list in order to install it.

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: localhost
      become: yes
      become_method: sudo
    
      vars:
        vagrant_plugins:
          lxc: false
          libvirt: true
          cachier: false
          hostmanager: false
          registration: true
          sshfs: false
          digitalocean: false
          adbinfo: false
    
      roles:
      - ansible-vagrant


License
-------

MIT

