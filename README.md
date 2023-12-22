# linux-showcase
To showcase knowledge withing Linux.


* proxmox:
  - user: root
  - pass: proxmox
  
* ssh:
  - key: showcase
    - phrase: 123
  - key: ctrlr default
    - phrase: 123
  - key: ansible
    - phrase: <blank>

* ubuntu-22.04-cloud-init-template
  - user: micke
  - pass: 123
  - sshkey: showcase
  - ipconfig: dhcp
  - storage: ssd emulator
* ubuntu-22.04-k8s-template
  - user: micke
  - pass: 123
  - sshkey: showcase
  - ipconfig: dhcp
  - storage: ssd emulator

servers:
ansible-node-1: 192.168.122.157
ansible-node-2: 192.168.122.166
ansible-node-3: 192.168.122.11
