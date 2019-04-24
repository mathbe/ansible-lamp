# ansible-lamp 

Ansible playbook to deploy a LAMP stack on Ubuntu hosts. Tested with the following environment

```
$ ansible --version
ansible 2.7.10
```

  * OVH VPS Ubuntu 16.04
  * OVH VPS Ubuntu 18.04

## Setup

  * Configure hosts file. Something like
```
[webserver]
server1.example.org     ansible_ssh_user=root ansible_ssh_pass=rootPassword ansible_python_interpreter=python3
```
  * Edit **host_vars/server1.example.org.yml** with your own values.

MySQL passwords generated with ```select password('password');```

  * Default password for root account: **rootPassword**
  * Default password for user account: **userPassword**

## Usage

  * Run ```ansible-playbook -i hosts lamp-http.yml``` for a web server running with an http access.
  * Run ```ansible-playbook -i hosts lamp-https.yml``` for a web server running with an https access, certificat generated with Letsencrypt.

## References

  * http://ferm.foo-projects.org/
  * https://dev.mysql.com/doc/refman/5.6/en/password-hashing.html
