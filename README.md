# Ansible Nathan Dench.python role

[![Build Status](https://img.shields.io/travis/Nathan Dench/ansible-role-python.svg)](https://travis-ci.org/Nathan Dench/ansible-role-python)
[![Galaxy](http://img.shields.io/badge/galaxy-Nathan Dench.python-role-blue.svg)](https://galaxy.ansible.com/Nathan Dench/python)
[![GitHub Tags](https://img.shields.io/github/tag/Nathan Dench/ansible-role-python.svg)](https://github.com/Nathan Dench/ansible-role-python)
[![GitHub Stars](https://img.shields.io/github/stars/Nathan Dench/ansible-role-python.svg)](https://github.com/Nathan Dench/ansible-role-python)

> `Nathan Dench.python` is an [Ansible](http://www.ansible.com) role which:
>
> * installs python
> * configures python
> * manages python
> * configures service

## Installation

Using `ansible-galaxy`:

```shell
$ ansible-galaxy install Nathan Dench.python
```

Using `requirements.yml`:

```yaml
- src: Nathan Dench.python
```

Using `git`:

```shell
$ git clone https://github.com/Nathan Dench/ansible-role-python.git Nathan Dench.python
```

## Dependencies

* Ansible >= 2.4
* dependency a
* dependency b

## Variables

Here is a list of all the default variables for this role, which are also available in `defaults/main.yml`.

```yaml
---
# package name (version)
python_package: python
# service name
python_service_name: python
# start on boot
python_service_enabled: yes
# current state: started, stopped
python_service_state: started

```

## Handlers

These are the handlers that are defined in `handlers/main.yml`.

```yaml
---
- name: restart python
  service:
    name: "{{ python_service_name }}"
    state: restarted
  when: python_service_state != 'stopped'

```

## A new section after the handler section

Lorem ipsum dolor sit atem ...

## Usage

This is an example playbook:

```yaml
---
- hosts: all
  # pre_tasks for installing dependencies for running the tests within docker
  # pre_tasks:
  #  - name: Installing openssh
  #    action: "{{ ansible_pkg_mgr }} pkg=my-package state=present"
  roles:
    - Nathan Dench.python
  vars:
    foo: bar

```

## A new section after the usage section

Lorem ipsum dolor sit atem ...

## Testing

```shell
$ git clone https://github.com/Nathan Dench/ansible-role-python.git
$ cd ansible-role-python
$ make test
```

## Contributing
In lieu of a formal style guide, take care to maintain the existing coding style. Add unit tests and examples for any new or changed functionality.

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

*Note: To update the `README.md` file please install and run `ansible-role`:*

```shell
$ gem install ansible-role
$ ansible-role docgen
```

## License
Copyright (c) Hyra iQ under the MIT license.
