Usage
Single shot:
```
ansible-playbook -i "ratos2.local," additions.yml -u pi --ask-pass --ask-become-pass --tags bootstrap,all
```

Later invocations that will not change the password or set the ssh public key access up:

```
ansible-playbook -i "ratos2.local," additions.yml -u pi --ask-pass --ask-become-pass
```
