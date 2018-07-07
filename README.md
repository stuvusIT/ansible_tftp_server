# tftp_server

Installs a tftpd-hpa server


## Requirements

A debian-based linux distribution


## Role Variables


| Name              | Default/Required | Description                                 |
|-------------------|:----------------:|---------------------------------------------|
| `tftpd_username`  | `tftp`           | User under which the tftp daemon runs       |
| `tftpd_directory` | `/srv/tftp`      | Path where the served files reside          |
| `tftpd_address`   | `:69`            | Adress on which the daemon should listen on |
| `tftpd_options`   | `--secure`       | Additional options to pass to the daemon    |

## Example Playbook

```yml
- hosts: pxe-servers
  roles:
  - tftp_server
    tftpd_directory: /var/lib/pxe
```

## License

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/).

## Author Information

- [Mohammed El-Rajab (GreatTeacherOni)](https://github.com/GreatTeacherOni) _mohammed.el-rajab@stuvus.uni-stuttgart.de_
