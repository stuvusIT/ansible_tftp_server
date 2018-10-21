# tftp_server

Installs a tftpd-hpa server


## Requirements

A debian-based linux distribution


## Role Variables


| Name              | Default/Required | Description                                   |
|-------------------|:----------------:|-----------------------------------------------|
| `tftpd_username`  |      `tftp`      | User under which the tftp daemon runs         |
| `tftpd_directory` |    `/srv/tftp`   | Path where the served files reside            |
| `tftpd_address`   |       `:69`      | Adress on which the daemon should listen on   |
| `tftpd_options`   |    `--secure`    | Additional options to pass to the daemon      |
| `tftpd_users`     |       `[]`       | Users to allow read access to the tftpd files |
| `tftpd_owner`     |      `root`      | Owner to set for `tftpd_directory`            |
| `tftpd_group`     |      `tftp`      | Group to set for `tftpd_directory`            |
| `tftpd_mode`      |      `0755`      | Permissions to set for `tftpd_directory`      |


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
- [Markus Mroch (Mr. Pi)](https://github.com/Mr-Pi) _markus.mroch@stuvus.uni-stuttgart.de_
