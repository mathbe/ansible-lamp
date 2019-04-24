# ansible-lamp 

Ansible playbook to deploy a LAMP stack on Ubuntu hosts. Tested with the following configurations :

```
$ ansible --version
ansible 2.7.10
```

  * OVH VPS Ubuntu 16.04
  * OVH VPS Ubuntu 18.04

## Setup

  * Configure hosts file, something like
```
[webserver]
server1.example.org     ansible_ssh_user=root ansible_ssh_pass=rootPassword ansible_python_interpreter=python3
```
  * Edit **host_vars/server1.example.org.yml** with your own values.
  * Run ```ansible-playbook -i hosts lamp-http.yml``` for a web server running with an http access.
  * Run ```ansible-playbook -i hosts lamp-https.yml``` for a web server running with an https access.

## References

  * [http://ferm.foo-projects.org/](http://ferm.foo-projects.org/)
