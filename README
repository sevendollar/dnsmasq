# dnsmasq

# DNS and DHCP service
$ docker run --name=dnsmasq --hostname=dnsmasq -d --cap-add=NET_ADMIN --net=host quay.io/coreos/dnsmasq \
  --no-daemon \
  --dhcp-range=10.5.1.32,10.5.1.33,1h \
  --dhcp-option=option:netmask,255.255.255.0 \
  --dhcp-option=option:router,10.5.1.254 \
  --dhcp-option=option:dns-server,168.95.1.1 \
  --dhcp-option=option:domain-name,jef.jef \
  --dhcp-broadcast \
  --dhcp-lease-max=100 \
  --domain-needed \
  --bogus-priv \
  --no-resolv \
  --no-poll \
  --expand-hosts \
  --filterwin2k \
  --server=8.8.4.4 \
  --server=8.8.8.8 \
  --domain=dns.lab \
  --local=/dns.lab/ \
  --log-queries \
  --log-dhcp


# DHCP configuration example config with /etc/dnsmasq.conf
dhcp-range=192.168.10.50,192.168.10.240,255.255.255.0,24h
dhcp-lease-max=100
dhcp-option=option:netmask,255.255.255.0
dhcp-option=option:router,192.168.10.1
dhcp-option=option:dns-server,192.168.10.1
dhcp-option=option:domain-name,jef.jef

dhcp-host=00:0C:29:A5:BD:4A,192.168.10.51
dhcp-host=00:0C:29:A5:BD:5B,192.168.10.52
dhcp-host=00:0C:29:A5:BD:6C,192.168.10.53

dhcp-host=00:0C:29:D0:95:5E,10.1.1.11,esxi01