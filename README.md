# Description
This playbook installs and configures Kodi to Raspberry Pi 4 running Raspberry Pi OS. Tested on Debian GNU/Linux 11 (bullseye). More info under roles/vese-kodi/README.md
# Usage
Add the IP address the Raspberry Pi 4 or localhost if installed locally to the inventory file. Run ansible playbook commnand:

``` 
ansible-playbook --ask-become-pass -i inventory site.yml --ask-vault-password
```
