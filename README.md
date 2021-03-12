net-tools
=========================
a simple bash script to check network connectivity and set various other network things 
nothing special just to make things a little eaiser becasue im lazy

Features
--------------
* Set Static IP
* Set DHCP IP
* Set Default
* Set nameserver 
* Add entries to hosts file 
* net-check - checks connectivity - arp,ping,dns,portscan,curl
* Speedtest - using speedtest-cli
* Find public IP
* Block IPv4 and IPv6 addresss using iptables,arptables and ip6tables
* Display iptables
* flush iptables
* Set Proxy Settings
* Clear Proxy Settings 


Install
-----------
Tried to make it easy use the oneliner to install the script and add it to bashrc

```console
cd /usr/share && git clone https://github.com/shifty0g/net-tools/ && cd net-tools && chmod +x net-tools.sh && ./net-tools.sh net-tools-install
```


Usege
---------
```console
net-help 
               __              __                .__
  ____   _____/  |_          _/  |_  ____   ____ |  |   ______
 /    \_/ __ \   __\  ______ \   __\/  _ \ /  _ \|  |  /  ___/
|   |  \  ___/|  |   /_____/  |  | (  <_> |  <_> )  |__\___ \
|___|  /\___  >__|            |__|  \____/ \____/|____/____  >
     \/     \/                                             \/

[*] Usage: [FUNCTION] [PARAMS]
========================================================================================
dhcp                                   DHCP on eth0  (specify the interface if you want another one)
static  192.168.2.99/24                set static IPv4 Address
gateway  192.168.1.1                   set default gateway
nameserver  192.168.1.1                add nameserver to /etc/resolve.conf
net-check                              does a set of tests to check connectivity (arp,ping,portscan,host)
tables-show                            shows the tables (iptables,ip6tables,arptables)
tables-flush                           flush all the tables (iptables,ip6tables,arptables)
block-ip  192.168.2.2                  BLOCK IPv4 addresses(iptables + arptables)
block-ip-file excludes.txt             BLOCK IPv4 addresses from file(iptables + arptables)
block-ip6                              use ip6tables to block a ipv6 adddress
hosts-add  10.10.10.171 htb.openadmin  adds hosts entry to /etc/hosts
hosts                                  opens up /etc/hosts
flush                                  flushes eth0 (specify the interface if you want another one)
ifu                                    ifconfig up on eth0  (specify the interface if you want another one)
ifd                                    ifconfig down on eth0  (specify the interface if you want another one)
flushall                               flushes ALL eth adapters
i                                      shows ifconfig - just lazy
publicip                               shows public ip address
ws                                     starts wirshark on eth0 (specify the interface if you want another one)
speedtest                              runs speedtest-cli
proxy-off                              clear proxy settings
proxy-on                               add proxy settings
net-help                               ashow the net-tools help menu (THIS)
net-tools-install                      run as root to install tools and include file in .bashrc
========================================================================================

```
