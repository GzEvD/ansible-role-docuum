# ansible-role-docuum

> Docuum performs least recently used (LRU) eviction of Docker images. 🗑️

Status:

[![Release and Changelog Builder](https://github.com/GzEvD/ansible-role-docuum/actions/workflows/changelog_builder.yml/badge.svg)](https://github.com/GzEvD/ansible-role-docuum/actions/workflows/changelog_builder.yml)

[![Ansible Lint](https://github.com/GzEvD/ansible-role-docuum/actions/workflows/ansible-lint.yaml/badge.svg)](https://github.com/GzEvD/ansible-role-docuum/actions/workflows/ansible-lint.yaml)

This roles installes [docuum](https://github.com/stepchowfun/docuum) and configures a systemd service to start it on boot.

## Variables

| Variable                | default                     | description                                                                          |
| ----------------------- | --------------------------- | ------------------------------------------------------------------------------------ |
| docuum_version          | `0.21.1`                    | version of docuum                                                                    |
| docuum_systemd_template | `systemd/docuum.service.j2` | template for systemd service                                                         |
| docuum_threshold        | `10G`                       | threshold for docker images see [flags](https://github.com/stepchowfun/docuum#usage) |
| docuum_keep_pattern     |                             | RegEx pattern of images to keep                                                      |
| docuum_loglevel         | `debug`                     | See [log levels](https://github.com/stepchowfun/docuum#usage) for more options       |
