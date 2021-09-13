Playbook for setting up my work environment
====================================

Set hostname to whatever you want and run

``` bash
apt -qq update
apt -y install python3 python3-pip python3-setuptools python3-dev build-essential libssl-dev libffi-dev sudo unzip zip man-db curl
pip3 install ansible==4.5.0
useradd -m -c "Samwise the Brave" diego  -s /bin/bash -p '*'
ansible-playbook -i "localhost," -c local playbook.yml --ask-sudo-pass --become --extra-vars "testing=false hostname=laptop install_packages=false"
```
