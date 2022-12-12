Proxmox Container
=========

A small role to deploy LXC containers on a promxox cluster

Requirements
------------

Python module `proxmoxer` on localhost and access to the Proxmox cluster.
Use `pip install -r requirements.txt`

Dependencies
------------

none

Example Playbook
----------------

A container can be created by setting the Proxmox API credentials and a `physical_host`:

    - hosts: container01
      vars:
        physical_host: server01
        proxmox_api_password: "foobar"
      roles:
         - proxmox-container
      tasks:
        - name: some task inside the new container

License
-------

CC-BY 4.0
