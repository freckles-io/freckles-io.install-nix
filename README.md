install-nix
===============

Ansible role to install the nix package manager.

Currently, only single-user install is supported (using the default bootstrap script from https://nixos.org/nix/install ), other ways of installing it might be implemented later on.

Requirements
----------------

Developed this role with Ansible 2.3, not sure if earlier versions will work.

Role Variables
--------------

The variables this role supports are:

    nix_installer_url: https://nixos.org/nix/install  # script that is used to install nix
    add_to_path: true  # whether to add nix to the path in rc files
    # rc files to add nix path loading line to
    rc_files_to_add_path_to:
      - "{{ ansible_env.HOME }}/.profile"


Dependencies
------------

No dependencies

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: localhost
      roles:
         - makkus.install-nix

License
-------

GPL v3

Author Information
------------------

Markus Binsteiner
