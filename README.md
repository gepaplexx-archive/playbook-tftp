# Ansible Playbook: tftp

![MIT](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)
![GitHub Workflow Status](https://img.shields.io/github/workflow/status/gepaplexx/playbook-tftp/Main?style=flat-square)
![GitHub last commit](https://img.shields.io/github/last-commit/gepaplexx/playbook-tftp?style=flat-square)
![Maintenance](https://img.shields.io/maintenance/yes/2022?style=flat-square)

An Ansible playbook for installing a TFTP (Trivial File Transfer Protocol) server on Ubuntu. Specifically, the responsibilities of this playbook are to:

- install the necessary packages
- manage the configuration
- manage SELinux settings

| Variable | Default | Comment |
| :--- | :--- | :--- |
| `tftp_anon_write`             | false                                | Boolean that specifies whether SELinux allows modifying files. |
| `tftp_group`                  | root                                 | Group of the `tftp_root_directory`                             |
| `tftp_home_dir`               | false                                | Boolean that specifies whether SELinux                         |
| `tftp_mode`                   | 0755                                 | Permissions of the `tftp_root_directory`                       |
| `tftp_root_directory`         | /var/lib/tftpboot                    | The path to the root directory served by tftp.                 |
| `tftp_server_args`            | --secure                             | Command line arguments to be passed to the server executable   |
| `tftp_server_foreman_support` | false                                | Enable Foreman support by creating suitable tftpd.map          |
| `tftp_setype`                 | tftpdir_rw_t                         | SELinux context for the tftp root directory                    |
| `tftp_user`                   | root                                 | Owner of the `tftp_root_directory`                             |

For more relevant documentation on TFTP, see:

- [`tftpd(8)` man page](http://linuxmanpages.net/manpages/fedora21/man8/tftpd.8.html)
- [`tftp_selinux(8)` man page](http://linuxmanpages.net/manpages/fedora21/man8/tftpd_selinux.8.html)

## License

MIT

## Contributions:

- [@ckaserer](https://github.com/ckaserer)
