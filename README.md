# Role Name

This role is used to setup my personal laptop

## Requirements

```
sudo dnf install -y python2 python2-dnf libselinux-python ansible npm
cd ~/.atom/packages/atom-beautify
npm install tidy-markdown@2.0.4
```

## Role Variables

TBD

## Dependencies

None

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```
- hosts: localhost
  roles:
     - { role: avnes.ansible-role-audun }
```

# Running

```
sudo dnf install -y python2 python2-dnf libselinux-python ansible npm
ANSIBLE_CONFIG=./role.cfg; export ANSIBLE_CONFIG
ansible-playbook -i tests/inventory --connection=local --ask-become-pass -vvvv tests/test.yml
```

## License

MIT

## Author Information

<https://github.com/avnes>
