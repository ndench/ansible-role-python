# Ansible ndench.python role

[![Build Status](https://img.shields.io/travis/ndench/ansible-role-python.svg)](https://travis-ci.org/ndench/ansible-role-python)
[![Galaxy](http://img.shields.io/badge/galaxy-ndench.python-blue.svg)](https://galaxy.ansible.com/ndench/python)
[![GitHub Tags](https://img.shields.io/github/tag/ndench/ansible-role-python.svg)](https://github.com/ndench/ansible-role-python)


> `ndench.python` is an [Ansible](http://www.ansible.com) role which:
>
> * installs [DeadSnakes PPA](https://launchpad.net/~deadsnakes/+archive/ubuntu/ppa)
> * installs specified version of python

## Installation

Using `ansible-galaxy`:

```shell
$ ansible-galaxy install ndench.python
```

Using `requirements.yml`:

```yaml
- src: ndench.python
```

Using `git`:

```shell
$ git clone https://github.com/ndench/ansible-role-python.git ndench.python
```

## Dependencies

* Ansible >= 2.4

## Variables

Here is a list of all the default variables for this role, which are also available in `defaults/main.yml`.

```yaml
---
python_version: 3.7

```


## Usage

This is an example playbook:

```yaml
---
- hosts: all
  roles:
    - ndench.python

```


## Testing

```shell
$ git clone https://github.com/ndench/ansible-role-python.git
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
Copyright (c)  under the MIT license.
