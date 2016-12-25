docker-dnsmasq
==============

Bash script to add running docker containers to dnsmasq config and restart dnsmasq service.

**Docker Container to DNS Entries:**

```bash
sudo cp update-docker0-dnsmasq /usr/local/bin/update-docker0-dnsmasq
chmod +x /usr/local/bin/update-docker0-dnsmasq
# DOCKERDNS_FILE=/etd/docker0-dnsmasq.d/docker0-network
# DOCKERDNS_SUFFIX=.docker.local
update-docker0-dnsmasq
# DOCKERDNS_FILE will be generated
```

**Docker Container to DNS Entries -> for public Interface, everything is proxied by nginx-proxy:**

```bash
sudo cp update-enp2s0-dnsmasq /usr/local/bin/update-enp2s0-dnsmasq
chmod +x /usr/local/bin/update-enp2s0-dnsmasq
# DOCKERDNS_FILE=/etd/enp2s0-dnsmasq.d/docker0-network
# DOCKERDNS_SUFFIX=.docker.local
update-enp2s0-dnsmasq
# DOCKERDNS_FILE will be generated
```
