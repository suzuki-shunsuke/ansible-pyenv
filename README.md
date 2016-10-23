pyenv
=========

[![Build Status](https://travis-ci.org/suzuki-shunsuke/ansible-pyenv.svg?branch=master)](https://travis-ci.org/suzuki-shunsuke/ansible-pyenv)

Install pyenv.

Requirements
------------

* [motemen/ghq](https://github.com/motemen/ghq)

Role Variables
--------------

* pyenv_ghq_executable: The executable path of ghq command. The default is "ghq".

Dependencies
------------

* [suzuki-shunsuke.ghq-module](https://galaxy.ansible.com/suzuki-shunsuke/ghq-module/)

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
  - suzuki-shunsuke.pyenv
```

License
-------

MIT
