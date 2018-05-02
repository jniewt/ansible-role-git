git
===

A brief description of the role goes here.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

* Tested on Ansible 2.5 or higher.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - name: Some git installation playbook
      hosts: all
      vars_prompt:
        - name: "git_user_name"
          prompt: "Full name"
          private: no
        - name: "git_user_email"
          prompt: "Email address"
          private: no
      tasks:
        - import_role:
            name: git


Author Information
------------------

jniewt |[jniewt@gmail.com](jniewt@gmail.com)
