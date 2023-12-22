# Infrastructure:
I'm running this on my homelab using Debian. Proxmox in KVM as the hypervisor. 16 cores and 25G memory. No playbooks against network equipment as I don't have access to it. IPS with Snort/Ossec and logging with Zabbix for basic events are sent to a Debian instance. No event-driven playbooks and little use of "when:".

## Servers:
* ubuntu-ctrlr = ansible and k8s controller.
* ubuntu-ansible-node-(1-3) = hosts for ansible, no k8s
* ubuntu-k8s-node-(1-2) = k8s cluster with ubuntu-ctrlr. Just a basic nginx service running, nodeport + flannel overlay.

## Templates:
* ubuntu-22.04-template = Template using Cloud-Init with ssd emulation and QEMU agent installed along with the "showcase" ssh-key.
* ubuntu-k8s-template = k8s node ready to use

## Credentials
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
