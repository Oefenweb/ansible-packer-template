## packer-template

[![Build Status](https://travis-ci.org/Oefenweb/ansible-packer-template.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-packer-template) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-packer--template-blue.svg)](https://galaxy.ansible.com/Oefenweb/packer-template)

Build Debian-like [Virtualbox](https://www.virtualbox.org/) images using [Packer](https://packer.io/) by HashiCorp.

#### Requirements

None

#### Variables

* `packer_template_version` [default: `1.0.0`]: Version to install

## Dependencies

None

#### Example

```yaml
---
- hosts: all
  roles:
    - packer-template
```

#### License

MIT

#### Author Information

Mischa ter Smitten (based on work from [chef/bento](https://github.com/chef/bento))

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-packer-template/issues)!
