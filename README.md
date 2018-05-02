git
===

Installs git and essential extensions on a Debian system.
Generates configuration along with some useful aliases.

Requirements
------------

Tested on Ansible 2.5 or higher.

Role Variables
--------------
Available variables are listed below, along with default values (see `defaults/main.yml`):

Name for the config file

    git_user_name: "User Name"

Email address for the config file

    git_user_email: "your@email.com"


There are more variables in `vars/main.yml`.
Change these only if you know what you're doing.

Dependencies
------------

None.

Example Playbook
----------------

This example shows how the role can be used while prompting the user for data.

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

License
-------

MIT / BSD

Author Information
------------------

jniewt |[jniewt@gmail.com](jniewt@gmail.com)
