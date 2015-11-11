# intro-to-ansible-workshop
A hands on workshop to configure server states using Ansible.

## Requirements
  - OSX or Linux control machine
  - Ansible version 1.9.4 or newer
  - SSH access to target machine

## Workshop Format

This workshops goal is to have you deploying server states onto target machines using Ansible and realizing the 5 minute learning curve is actual.

All commands are copy and paste to avoid typos.  That also follows our goal of infrastructure as code but in this sense it is workshop as code.

Command example:

```
2.2.3 in intro-to-ansible-workshop/ on master
› ansible -i "fed22," -m ping all
```

The text to copy is after the `>`
