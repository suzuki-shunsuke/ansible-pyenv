# ansible-pyenv

[![Build Status](https://travis-ci.org/suzuki-shunsuke/ansible-pyenv.svg?branch=master)](https://travis-ci.org/suzuki-shunsuke/ansible-pyenv)

ansible role to install [pyenv](https://github.com/pyenv/pyenv).

* [suzuki-shunsuke.pyenv](https://galaxy.ansible.com/suzuki-shunsuke/pyenv/)

## Requirements

* git

## Role Variables

name | required | default | description
--- | --- | --- | ---
pyenv_root | no | $PYENV_ROOT >> $HOME/.pyenv
pyenv_repo | no | https://github.com/pyenv/pyenv |
pyenv_version | no | HEAD |
pyenv_update | no | yes |
pyenv_is_dependencies_installed | no | no | By default build dependencies are not installed
pyenv_rc_path | no | "NOT ADD" | By default configuration is not added
pyenv_darwin_build_dependencies | no | see [defaults/main.yml](https://github.com/suzuki-shunsuke/ansible-pyenv/blob/master/defaults/main.yml) | If pyenv_is_dependencies_installed is "no" this is ignored
pyenv_redhat_build_dependencies | no | see [defaults/main.yml](https://github.com/suzuki-shunsuke/ansible-pyenv/blob/master/defaults/main.yml) | If pyenv_is_dependencies_installed is "no" this is ignored
pyenv_debian_build_dependencies | no | see [defaults/main.yml](https://github.com/suzuki-shunsuke/ansible-pyenv/blob/master/defaults/main.yml) | If pyenv_is_dependencies_installed is "no" this is ignored
pyenv_darwin_additional_build_dependencies | no | [] | If pyenv_is_dependencies_installed is "no" this is ignored
pyenv_redhat_additional_build_dependencies | no | [] | If pyenv_is_dependencies_installed is "no" this is ignored
pyenv_debian_additional_build_dependencies | no | [] | If pyenv_is_dependencies_installed is "no" this is ignored

About build dependencies, see also [here](https://github.com/pyenv/pyenv/wiki/Common-build-problems).

## Dependencies

Nothing.

## Example Playbook

```yaml
- hosts: servers
  roles:
  - role: suzuki-shunsuke.pyenv
    pyenv_root: "{{ ansible_env.HOME }}/.ghq/github.com/pyenv/pyenv"
    pyenv_version: v1.1.0
    pyenv_update: no
    pyenv_is_dependencies_installed: yes
    pyenv_rc_path: "{{ ansible_env.HOME }}/.bashrc"
    pyenv_darwin_build_dependencies:
    - readline
```

## Change Log

See [CHANGELOG.md](CHANGELOG.md).

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## See also

* [suzuki-shunsuke.pyenv-virtualenv](https://github.com/suzuki-shunsuke/ansible-pyenv-virtualenv): ansible role to install pyenv-virtualenv
* [suzuki-shunsuke.pyenv-module](https://github.com/suzuki-shunsuke/ansible-pyenv-module): ansible module to run `pyenv` command

## License

[MIT](LICENSE)
