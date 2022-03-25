# Role Name

This role is used to configure my personal laptop with Fedora customization

## Requirements

```
python2
python2-dnf
libselinux-python
npm
```

## Role Variables

### default/main.yml:

```
pycharm_download_url: https://download.jetbrains.com/python/pycharm-community-2017.1.1.tar.gz
pycharm_install_dir: /opt/pycharm
pycharm_checksum: 1300e15b760a05d0b41f7d85674c01368e37ac2b6215889badf8ab0adcf4a34b
checksum_algorithm: sha256
```

### vars/main.yml

Please note that this file is encrypted with Ansible Vault. It contains the following variables:

```
git_config_user_name:
git_config_user_email:
files_base_dir:
```

## Dependencies

None

## Example Playbook

```
- hosts: localhost
  roles:
     - { role: ansible-role-audun }
```

# Running

```
sudo dnf install -y python2 python2-dnf libselinux-python ansible npm
ANSIBLE_CONFIG=./role.cfg; export ANSIBLE_CONFIG
ansible-playbook -i tests/inventory --connection=local --ask-become-pass --ask-vault-pass -vvvv tests/test.yml
```

## License

MIT

## Author Information

<https://github.com/avnes>
