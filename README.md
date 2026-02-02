Usage

Assuming the printer you want to configure is "ratos2""

# Prepare:

```
ssh-keyscan -H ratos2 >> ~/.ssh/known_hosts
```
(Or get the host key some other way)


# Single shot for everything after preparation
```
ansible-playbook -i "ratos2," additions.yml -u pi --ask-pass --ask-become-pass --tags bootstrap,all
```

# Later invocations 
Will not change the password or set the ssh public key access up:

```
ansible-playbook -i "ratos2," additions.yml -u pi --ask-pass --ask-become-pass
```
