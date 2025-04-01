# Playbook for setting up my work environment

Set hostname to whatever you want and run as root

```bash
apt -qq update && \
apt -y install python3 python3-debian pipx python3-pip python3-setuptools python3-dev build-essential libssl-dev libffi-dev sudo unzip zip man-db curl && \
pipx install --include-deps  ansible==11.3.0 && \
useradd -m -c "Samwise the Brave" diego  -s /bin/bash -p '*'
sudo -u root bash
/root/.local/bin/ansible-playbook -i "localhost," -c local playbook.yml --become --extra-vars "testing=false hostname=dt90 install_packages=false"
```
