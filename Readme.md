

Install Ansible

Create a file named `secrets.pass` with the Ansible vault password as a string on a single line.

## Deployment

- Install Ubuntu 24.04 on all hosts, with the usual credentials.
- Install openssh-server on all hosts
- Add the public ssh key of the managing computer to the hosts's `authorized_keys`.

Run:

```
ansible-playbook -i inventory.yaml playbook.yaml --ask-become-pass --vault-password-file secrets.pass
```


