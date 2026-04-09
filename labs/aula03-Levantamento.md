  UNIT                        LOAD   ACTIVE SUB     DESCRIPTION                                   
  apache2.service             loaded active running The Apache HTTP Server
  cron.service                loaded active running Regular background program processing daemon
  dbus.service                loaded active running D-Bus System Message Bus
  fwupd.service               loaded active running Firmware update daemon
  getty@tty1.service          loaded active running Getty on tty1
  grafana-server.service      loaded active running Grafana instance
  ModemManager.service        loaded active running Modem Manager
  multipathd.service          loaded active running Device-Mapper Multipath Device Controller
  mysql.service               loaded active running MySQL Community Server
  node_exporter.service       loaded active running Node Exporter
  polkit.service              loaded active running Authorization Manager
  prometheus.service          loaded active running Prometheus
  rsyslog.service             loaded active running System Logging Service
  ssh.service                 loaded active running OpenBSD Secure Shell server
  systemd-journald.service    loaded active running Journal Service
  systemd-logind.service      loaded active running User Login Management
  systemd-networkd.service    loaded active running Network Configuration
  systemd-resolved.service    loaded active running Network Name Resolution
  systemd-timesyncd.service   loaded active running Network Time Synchronization
  systemd-udevd.service       loaded active running Rule-based Manager for Device Events and Files
  tomcat11.service            loaded active running Apache Tomcat11
  udisks2.service             loaded active running Disk Manager
  unattended-upgrades.service loaded active running Unattended Upgrades Shutdown
  upower.service              loaded active running Daemon for power management
  user@1000.service           loaded active running User Manager for UID 1000

Legend: LOAD   → Reflects whether the unit definition was properly loaded.
        ACTIVE → The high-level unit activation state, i.e. generalization of SUB.
        SUB    → The low-level unit activation state, values depend on unit type.

25 loaded units listed.
lines 19-32/32 (END)
  systemd-resolved.service    loaded active running Network Name Resolution
  systemd-timesyncd.service   loaded active running Network Time Synchronization
  systemd-udevd.service       loaded active running Rule-based Manager for Device Events and Files
  tomcat11.service            loaded active running Apache Tomcat11
  Netid         State          Recv-Q         Send-Q                 Local Address:Port                    Peer Address:Port         Process
udp           UNCONN         0              0                         127.0.0.54:53                           0.0.0.0:*             uid:992 ino:6578 sk:1 cgroup:/system.slice/systemd-resolved.service <->
udp           UNCONN         0              0                      127.0.0.53%lo:53                           0.0.0.0:*             uid:992 ino:6576 sk:2 cgroup:/system.slice/systemd-resolved.service <->
tcp           LISTEN         0              4096                      127.0.0.54:53                           0.0.0.0:*             uid:992 ino:6579 sk:3 cgroup:/system.slice/systemd-resolved.service <->
tcp           LISTEN         0              4096                   127.0.0.53%lo:53                           0.0.0.0:*             uid:992 ino:6577 sk:4 cgroup:/system.slice/systemd-resolved.service <->
tcp           LISTEN         0              300                          0.0.0.0:3306                         0.0.0.0:*             uid:110 ino:9088 sk:5 cgroup:/system.slice/mysql.service <->
tcp           LISTEN         0              4096                         0.0.0.0:22                           0.0.0.0:*             ino:7587 sk:6 cgroup:/system.slice/ssh.socket <->
tcp           LISTEN         0              4096                               *:3000                               *:*             uid:111 ino:9161 sk:7 cgroup:/system.slice/grafana-server.service v6only:0 <->
tcp           LISTEN         0              100                                *:8080                               *:*             uid:1001 ino:10010 sk:8 cgroup:/system.slice/tomcat11.service v6only:0 <->
tcp           LISTEN         0              4096                               *:9091                               *:*             uid:999 ino:9978 sk:9 cgroup:/system.slice/prometheus.service v6only:0 <->
tcp           LISTEN         0              4096                               *:9100                               *:*             uid:996 ino:9486 sk:a cgroup:/system.slice/node_exporter.service v6only:0 <->
tcp           LISTEN         0              511                                *:8888                               *:*             ino:9406 sk:b cgroup:/system.slice/apache2.service v6only:0 <->
tcp           LISTEN         0              70                                 *:33060                              *:*             uid:110 ino:10013 sk:c cgroup:/system.slice/mysql.service v6only:0 <->
tcp           LISTEN         0              511                                *:80                                 *:*             ino:9402 sk:d cgroup:/system.slice/apache2.service v6only:0 <->