# Tiny linux showcase

## High-level Infrastructure
```diff
+ See screenshots at the bottom of the page to preview the setup.
```

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

## Screenshots
![proxmox dashboard](https://github.com/oshebj/linux-showcase/blob/main/proxmox-dash.png)
![simple ansible](https://github.com/oshebj/linux-showcase/blob/main/sample-ansible.png)
![snort3 installed](https://github.com/oshebj/linux-showcase/blob/main/snort-installed.png)
![snort3 icmp test](https://github.com/oshebj/linux-showcase/blob/main/snort-icmp-example.png)
![grafana dashboard](https://github.com/oshebj/linux-showcase/blob/main/grafana-dash.png)
![prometheus active targets](https://github.com/oshebj/linux-showcase/blob/main/prometheus.png)
