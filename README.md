### Create SSH key pair
```bash
ssh-keygen -t ed25519 -f id_ansible
```

### Disable checking host keys
```bash
export ANSIBLE_HOST_KEY_CHECKING=False
```

/etc/ansible/ansible.cfg or ~/.ansible.cfg
```
[defaults]
host_key_checking = False
```

### Start playbook
```bash
ansible-playbook -i inventory --private-key id_ansible setup-all.yaml
```
or without private key if it's defined in the inventory or variables.
```bash
ansible-playbook -i inventory setup-all.yaml
```
