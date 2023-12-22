# Tiny linux showcase

## High-level Infrastructure
* Proxmox VE running on KVM.
* Ansible with hosts and a few simple playbooks for provisioning/bootstrap.
* Kubernetes with nodes running a simple webservice.
* Prometheus for monitoring using Grafana.
* Snort V3 as IDS with simple rules.
* Suricata for IPS with simple rules.

## Credentials
*SSH:*
* showcase / 123
* ctrlr default / 123
* ansible / [null]

*VM:*
* proxmox: root / proxmox
* VMs: micke / 123

*Metrics:*
* Grafana: admin / 12345

## Templates within Proxmox
* Ubuntu with Cloud-init drive, ssd emulated + qemu guest agent.
* Ubuntu k8s, same as above, but with k8s packages installed and ready to join the cluster.

## Networking
Nothing special. DHCP with reserved leases from FW. Controller is static.
This is just a demo. See Snort and Suricata config files.
