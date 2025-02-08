rpi_configure_radio
===================
[![Ansible Lint](https://github.com/oxivanisher/role-rpi_configure_radio/actions/workflows/ansible-lint.yml/badge.svg)](https://github.com/oxivanisher/role-rpi_configure_radio/actions/workflows/ansible-lint.yml)

Enable or disable the wifi and bluetooth adapter. Also disable wifi powersave for wifi enabled devices.

As always: Use at your own risk!

Role Variables
--------------

| Name                             | Comment                                   | Default value |
|----------------------------------|-------------------------------------------|---------------|
| rpi_configure_radio_disable_wifi | Should the wifi adapter be disabled?      | `false`       |
| rpi_configure_radio_disable_bt   | Should the bluetooth adapter be disabled? | `false`       |
| rpi_configure_radio_rpi_boot_dev | The boot device where the `config.txt` is located. Will be overwritten if `raspberry_pi_boot_dev` is set! | `/dev/mmcblk0p1` |

Example Playbook
----------------

```yaml
- name: Enable or disable wifi and bluetooth on Raspberry Pi
  hosts: rpis
  collections:
    - oxivanisher.raspberry_pi
  roles:
    - role: oxivanisher.raspberry_pi.rpi_configure_radio
```

License
-------

BSD

Author Information
------------------

This role is part of the [oxivanisher.raspberry_pi](https://galaxy.ansible.com/ui/repo/published/oxivanisher/raspberry_pi/) collection, and the source for that is located on [github](https://github.com/oxivanisher/collection-raspberry_pi).
