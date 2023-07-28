The default is "On"
This can cause problems when you use Network Manager! Nodes will show "3 DNS servers" instead of 2, with the first one being MAAS. Disable this to fix DNS resolution on nodes!

configure_url: http://192.168.121.219:5240/MAAS/r/subnet/2
name: Allow DNS resolution
state: Disallowed
