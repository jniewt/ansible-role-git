git
===

Installs git and essential extensions on a Debian or Ubuntu system.
Generates configuration along with some useful aliases.

Run as the user you want to use git with.
When running the playbook, it might be necessary to use `--ask-become-pass`.

Tested on the following distributions:
 * Debian buster/sid
 * Debian 9
 * Ubuntu 18.04
 * Ubuntu 16.04
 * Ubuntu 14.04

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

Whether to install git prompt in your bash prompt, showing current branch and some other useful information.
See [bash-git-prompt](https://github.com/magicmonty/bash-git-prompt) for details.

Note, that **this will overwrite your .bashrc** (will backup the old one though)!

    git_prompt_install: no

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

jniewt | [jniewt@gmail.com](jniewt@gmail.com)
