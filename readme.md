Playbook for setting up my work environment
====================================

Set hostname to whatever you want and run

``` bash
ansible-playbook -i "localhost," -c local playbook.yml --ask-sudo-pass --become --extra-vars "testing=false hostname=laptop install_packages=false"
```
