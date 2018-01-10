# gateway-setup

## avahi service advertisement and descovery
   
   
## Install packages

```
sudo apt-get install avahi-daemon avahi-discover avahi-utils libnss-mdns mdns-scan
```

## Setup
```
$ getent hosts
$ hostnamectl status|grep -i static
// if not set then set it over here
$ hostnamectl set-hostname test.hostname.com
$ systemctl start avahi-daemon
$ statemctl enable avahi-daemon
$ getent hosts
$ getent hosts test.local
$ ping test.local
```

## Resolve hostname
```
$vi /etc/nsswitch.conf
```
 Change the hosts line to include mdns_minimal [NOTFOUND=return] before resolve and dns   
    
 ```
 hosts: ... mdns_minimal [NOTFOUND=return] resolve [!UNAVAIL=return] dns ...
 ```

## Adding services
