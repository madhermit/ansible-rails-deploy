Rails Deployment Ansible Role
=========

![HE:Labs](https://raw.githubusercontent.com/Helabs/helabs.github.com/master/images/logo.png "HE:Labs")

This is a simple role, that deploys a rails application from a git repo.

Requirements
------------

This role only requires Ansible version 1.9+
An Ansible vault with the RSA key pair that'll be used by the application user.

Role Variables
--------------

All variables should be overwritten at the playbook level. Those are:

`required_packages`:

      - git
      - build-essential

`rails_bundle_without`:

`required_gems`:

      - rails

`rails_user`:

      webapp

`rails_path`:

      "/opt/{{ rails_user }}"

`rails_app_name`:

      "{{ rails_user }}"

rails_repo:

      "git@github.com:lucazz/demo_app.git"

Dependencies
------------

This role has no dependecies

Using this role
----------------

Using this roles as as simples as:

    - hosts: servers
      gather_facts: true
      roles:
         - helabs.rails-deploy


License
-------

BSD

Author Information
------------------

Lucas do Amaral Saboya Works as DevOps/SysOps @ [HE:Labs](https://www.helabs.com)
