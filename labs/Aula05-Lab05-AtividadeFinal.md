     Online state: offline
    DNS Addresses: 127.0.0.53 (stub)
       DNS Search: .

●  1: lo ethernet UNKNOWN/UP (unmanaged)
      MAC Address: 00:00:00:00:00:00
        Addresses: 127.0.0.1/8
                   ::1/128

●  2: enp0s3 ethernet UP (networkd: enp0s3)
      MAC Address: 08:00:27:f1:74:10 (Intel Corporation)
        Addresses: 10.24.82.221/24
                   fe80::a00:27ff:fef1:7410/64 (link)
           Routes: 10.24.82.0/24 from 10.24.82.221 (link)
                   fe80::/64 metric 256

●  3: docker0 bridge UP (unmanaged)
      MAC Address: 8e:3e:1d:d3:8d:75
        Addresses: 172.17.0.1/16
                   fe80::8c3e:1dff:fed3:8d75/64 (link)
           Routes: 172.17.0.0/16 from 172.17.0.1 (link)
                   fe80::/64 metric 256
       Interfaces: veth4ffa819

●  4: veth4ffa819 virtual-ethernet UP (unmanaged)
      MAC Address: ae:f0:ee:08:77:90
        Addresses: fe80::acf0:eeff:fe08:7790/64 (link)
           Routes: fe80::/64 metric 256
           Bridge: docker0
No LSB modules are available.
Distributor ID: Ubuntu
Description:    Ubuntu 24.04.4 LTS
Release:        24.04
Codename:       noble
PRETTY_NAME="Ubuntu 24.04.4 LTS"
NAME="Ubuntu"
VERSION_ID="24.04"
VERSION="24.04.4 LTS (Noble Numbat)"
VERSION_CODENAME=noble
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
UBUNTU_CODENAME=noble
LOGO=ubuntu-logo


Linux ctlinux01 6.8.0-106-generic #106-Ubuntu SMP PREEMPT_DYNAMIC Fri Mar  6 07:58:08 UTC 2026 x86_64 x86_64 x86_64 GNU/Linux


 23:33:56 up 48 min,  2 users,  load average: 0.00, 0.00, 0.00


                total        used        free      shared  buff/cache   available
Mem:            3915         525        3021           1         586        3390  
Swap:           3914           0        3914


NAME                      MAJ:MIN RM  SIZE RO TYPE MOUNTPOINTS
sda                         8:0    0   50G  0 disk
├─sda1                      8:1    0    1M  0 part
├─sda2                      8:2    0    2G  0 part /boot
└─sda3                      8:3    0   48G  0 part
  └─ubuntu--vg-ubuntu--lv 252:0    0   48G  0 lvm  /
sr0                        11:0    1 1024M  0 rom



Filesystem                         Size  Used Avail Use% Mounted on
tmpfs                              392M  1.2M  391M   1% /run
/dev/mapper/ubuntu--vg-ubuntu--lv   47G  8.3G   37G  19% /
tmpfs                              2.0G     0  2.0G   0% /dev/shm
tmpfs                              5.0M     0  5.0M   0% /run/lock
/dev/sda2                          2.0G  198M  1.6G  11% /boot
tmpfs                              392M   12K  392M   1% /run/user/1000


 Static hostname: ctlinux01
       Icon name: computer-vm
         Chassis: vm 🖴
      Machine ID: 05c2865e767d44c4870777b482ba0652
         Boot ID: a69a259f420941678c605f28b8e0a737
  Virtualization: oracle
Operating System: Ubuntu 24.04.4 LTS
          Kernel: Linux 6.8.0-106-generic
    Architecture: x86-64
 Hardware Vendor: innotek GmbH
  Hardware Model: VirtualBox
Firmware Version: VirtualBox
   Firmware Date: Fri 2006-12-01
    Firmware Age: 19y 4month 1w    


    1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host noprefixroute
       valid_lft forever preferred_lft forever
2: enp0s3: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 08:00:27:f1:74:10 brd ff:ff:ff:ff:ff:ff
    inet 10.24.82.221/24 brd 10.24.82.255 scope global enp0s3
       valid_lft forever preferred_lft forever
    inet6 fe80::a00:27ff:fef1:7410/64 scope link
       valid_lft forever preferred_lft forever
3: docker0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc noqueue state UP group default
    link/ether 8e:3e:1d:d3:8d:75 brd ff:ff:ff:ff:ff:ff
    inet 172.17.0.1/16 brd 172.17.255.255 scope global docker0
       valid_lft forever preferred_lft forever
    inet6 fe80::8c3e:1dff:fed3:8d75/64 scope link
       valid_lft forever preferred_lft forever
4: veth4ffa819@if2: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc noqueue master docker0 state UP group default
    link/ether ae:f0:ee:08:77:90 brd ff:ff:ff:ff:ff:ff link-netnsid 0
    inet6 fe80::acf0:eeff:fe08:7790/64 scope link
       valid_lft forever preferred_lft forever


       
default via 10.24.82.1 dev enp0s3 proto static 
10.24.82.0/24 dev enp0s3 proto kernel scope link src 10.24.82.221
172.17.0.0/16 dev docker0 proto kernel scope link src 172.17.0.1



Global
         Protocols: -LLMNR -mDNS -DNSOverTLS DNSSEC=no/unsupported
  resolv.conf mode: stub

Link 2 (enp0s3)
    Current Scopes: DNS
         Protocols: +DefaultRoute -LLMNR -mDNS -DNSOverTLS DNSSEC=no/unsupported  
Current DNS Server: 8.8.8.8
       DNS Servers: 8.8.8.8 8.8.4.4

Link 3 (docker0)
    Current Scopes: none
         Protocols: -DefaultRoute -LLMNR -mDNS -DNSOverTLS DNSSEC=no/unsupported  

Link 4 (veth4ffa819)
    Current Scopes: none
         Protocols: -DefaultRoute -LLMNR -mDNS -DNSOverTLS DNSSEC=no/unsupported  


         
State    Recv-Q   Send-Q     Local Address:Port     Peer Address:Port   Process   
LISTEN   0        4096             0.0.0.0:22            0.0.0.0:*
LISTEN   0        4096          127.0.0.54:53            0.0.0.0:*
LISTEN   0        4096          127.0.0.54:53            0.0.0.0:*
LISTEN   0        4096             0.0.0.0:9000          0.0.0.0:*
LISTEN   0        4096       127.0.0.53%lo:53            0.0.0.0:*


  UNIT                        LOAD   ACTIVE SUB     DESCRIPTION                  >
  containerd.service          loaded active running containerd container runtime  
  cron.service                loaded active running Regular background program pr>
  dbus.service                loaded active running D-Bus System Message Bus      
  docker.service              loaded active running Docker Application Container >
  fwupd.service               loaded active running Firmware update daemon        
  getty@tty1.service          loaded active running Getty on tty1
  ModemManager.service        loaded active running Modem Manager
  multipathd.service          loaded active running Device-Mapper Multipath Devic>
  polkit.service              loaded active running Authorization Manager
  portainer.service           loaded active running Portainer container
  rsyslog.service             loaded active running System Logging Service        
  ssh.service                 loaded active running OpenBSD Secure Shell server   
  systemd-journald.service    loaded active running Journal Service
  systemd-logind.service      loaded active running User Login Management
  systemd-networkd.service    loaded active running Network Configuration
  systemd-resolved.service    loaded active running Network Name Resolution       
  systemd-timesyncd.service   loaded active running Network Time Synchronization  
  systemd-udevd.service       loaded active running Rule-based Manager for Device>
  udisks2.service             loaded active running Disk Manager
  unattended-upgrades.service loaded active running Unattended Upgrades Shutdown  
  upower.service              loaded active running Daemon for power management   
  user@1000.service           loaded active running User Manager for UID 1000     

Legend: LOAD   → Reflects whether the unit definition was properly loaded.        
        ACTIVE → The high-level unit activation state, i.e. generalization of SUB.
        SUB    → The low-level unit activation state, values depend on unit type. 

22 loaded units listed.