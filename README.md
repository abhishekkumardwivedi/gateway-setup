# gateway-setup

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
