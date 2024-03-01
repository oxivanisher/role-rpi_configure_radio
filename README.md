rpi_configure_radio
===================

Enable or disable the wifi and bluetooth adapter. Also disable wifi powersave for wifi enabled devices.

As always: Use at your own risk!

Role Variables
--------------

| Name                             | Comment                                   | Default value |
|----------------------------------|-------------------------------------------|---------------|
| rpi_configure_radio_disable_wifi | Should the wifi adapter be disabled?      | `false`          |
| rpi_configure_radio_disable_bt   | Should the bluetooth adapter be disabled? | `false`          |
| raspberry_pi_boot_dev | Raspberry pi boot dev (used for editing config.txt) | /dev/mmcblk0p1 |

Example Playbook
----------------

```yaml
- name: Raspberry Pi
  hosts: rpis
  collections:
    - oxivanisher.raspberry_pi
  roles:
    - role: oxivanisher.raspberry_pi.rpi_configure_radio              # configure radio on rpis
```

License
-------

BSD

Author Information
------------------

This role is part of the [oxivanisher.raspberry_pi](https://galaxy.ansible.com/ui/repo/published/oxivanisher/raspberry_pi/) collection, and the source for that is located on [github](https://github.com/oxivanisher/collection-raspberry_pi).
