ansible-deploy-projects-role
=========

Small role to handle initial code deployment via git. Composer install support included.

Requirements
------------

None

ToDo's
------------

- Make forcing git checkout / clone an option (Remove problems when local changes have been made to code)
- Add configuration variables for --no-dev and --no-scripts for composer install

Role Variables
--------------
```YAML
# Enable git deployment
deploy_git: true

#Exmaple git deployment
deploy_projects:
  - git:
      - repository: ssh://user@path/to/git/repository.git
        branch: master
        remote_user: user
        deploy_dir: /path/to/clone/directory
        composer_install: true
```

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: methorz.ansible-deploy-projects-role}

License
-------

BSD

Author Information
------------------

https://twitter.com/methor_z
