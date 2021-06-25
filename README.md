## packer-template

[![CI](https://github.com/Oefenweb/ansible-packer-template/workflows/CI/badge.svg)](https://github.com/Oefenweb/ansible-packer-template/actions?query=workflow%3ACI)
[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-packer--template-blue.svg)](https://galaxy.ansible.com/Oefenweb/packer_template)

Build Debian-like [Virtualbox](https://www.virtualbox.org/) images using [Packer](https://packer.io/) by HashiCorp.

#### Requirements

None

#### Variables

* `packer_template_state` [default: `''`]: State (e.g. `pre`, `post`)
* `packer_template_metadata` [default: `build: {timestamp: "{{ packer_template_metadata_build_timestamp }}", revision: "{{ packer_template_metadata_build_revision }}", version: "{{ packer_template_metadata_build_version }}"`]:
* `packer_template_metadata_build_timestamp` [default: `__UNKNOWN_BUILD_TIMESTAMP__`]: Build timestamp
* `packer_template_metadata_build_revision` [default: `__UNKNOWN_BUILD_REVISION__`]: Build revision
* `packer_template_metadata_build_version` [default: `__UNKNOWN_BUILD_VERSION__`]: Build version

* `packer_template_cleanup_development_exclude` [default: `[]`]: Packages (development) *not* to remove (e.g. `libmysqlclient-dev`)
* `packer_template_cleanup_doc_exclude` [default: `[]`]: Packages (doc) *not* to remove
* `packer_template_cleanup_more` [default: `"{{ packer_template_preset_cleanup_more_x11_libraries + packer_template_preset_cleanup_more_obsolete_networking + packer_template_preset_cleanup_more_oddities + packer_template_preset_cleanup_more_various }}"`]: Packages (more) to remove

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
