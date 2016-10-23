pyenv
=========

Install pyenv.

Requirements
------------

* ghq

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
