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

The text to copy is after the `>` - Any all caps replace with your info.

## Test Servers

All test servers are hosted by Digital Ocean.  Referrals appreciated

(Referral Link)[https://www.digitalocean.com/?refcode=980586449ebd]

---

 # Ansible CLI

 ### ping

 ```
 2.2.3 in intro-to-ansible-workshop/ on master
 › ansible -i "SERVER," -m ping all
 ```

 ### ls -al /home

 ```
 2.2.3 in intro-to-ansible-workshop/ on master
 › ansible -i "SERVER," -m command -a "ls -al ~" all
 ```

 ### install ntp with yum module

 ```
 2.2.3 in intro-to-ansible-workshop/ on master
 › ansible -i "SERVER," -m yum -a "name=ntp state=present" all
 ```

 ### install and configure Tomcat & deploy sample.war

 ```
 2.2.3 in intro-to-ansible-workshop/ on master
 › git clone https://github.com/e30chris/Ansible-ApacheTomcat.git
 › cd Ansible-ApacheTomcat/
 ```

```
2.2.3 in intro-to-ansible-workshop/ on master
› ansible-playbook -i "SERVER," site.yml -vvvv
```
