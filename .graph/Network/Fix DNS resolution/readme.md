# Problem
The default is "On"
This can cause problems when you use Network Manager! Nodes will show "3 DNS servers" instead of 2, with the first one being MAAS. Disable this to fix DNS resolution on nodes!

# Solution
configure_url: http://192.168.121.219:5240/MAAS/r/subnet/2
name: Allow DNS resolution
state: Disallowed

## This has to run on each node!
https://www.tecmint.com/set-permanent-dns-nameservers-in-ubuntu-debian/

```
echo '''nameserver 8.8.8.8 
nameserver 8.8.4.4''' | sudo tee \
tee -a /etc/resolvconf/resolv.conf.d/head

sudo systemctl restart resolvconf.service
sudo systemctl restart systemd-resolved.service
```
