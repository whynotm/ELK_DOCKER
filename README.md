# ELK_DOCKER

33START FROM SCRATCH

#sudo docker pull sebp/elk 


#sudo docker run -p 5601:5601 -p 9200:9200 -p 5044:5044 -it --name elk sebp/elk

## ADD VOLUM ON START DOCKER
k/run


##Install PING COMMAND and COMMIT on V2 Images

#apt-get install iputils-ping

#sudo docker commit -m "install iputils-ping " elk-nagios sebp/elk:v2



## redierct some log to enable kabana

#sudo docker exec -it elk /bin/bash
#/opt/logstash/bin/logstash --path.data /tmp/logstash/data -e 'input { stdin { } } output { elasticsearch { hosts => ["localhost"] } }'



## USING ELK INTEGRATION WITH NAGIOS  
    URL https://www.elastic.co/blog/integrating-nagios-checks-with-logstash

#

[root@059282ca97d3:/# apt-get install nagios-plugins
Reading package lists... Done
Building dependency tree
Reading state information... Done
The following additional packages will be installed:
  bind9-host dnsutils geoip-database ifupdown iproute2 isc-dhcp-client isc-dhcp-common libarchive13 libatm1 libbind9-140 libdbi1 libdns-export162 libdns162 libgdbm3 libgeoip1
  libisc-export160 libisc160 libisccc140 libisccfg140 libldb1 liblwres141 liblzo2-2 libmnl0 libmysqlclient20 libnet-snmp-perl libpci3 libperl5.22 libpq5 libpython-stdlib libpython2.7
  libpython2.7-minimal libpython2.7-stdlib libsmbclient libsnmp-base libsnmp30 libtalloc2 libtdb1 libtevent0 libtirpc1 libwbclient0 libxtables11 monitoring-plugins
  monitoring-plugins-basic monitoring-plugins-common monitoring-plugins-standard mysql-common netbase perl perl-base perl-modules-5.22 python python-crypto python-ldb python-minimal
  python-samba python-talloc python-tdb python2.7 python2.7-minimal rename rpcbind samba-common samba-common-bin samba-libs smbclient snmp
Suggested packages:
  rblcheck ppp rdnssd iproute2-doc resolvconf avahi-autoipd isc-dhcp-client-ddns apparmor lrzip geoip-bin libcrypt-des-perl libdigest-hmac-perl libio-socket-inet6-perl
  snmp-mibs-downloader icinga | icinga | nagios3 nagios-plugins-contrib fping postfix | sendmail-bin | exim4-daemon-heavy | exim4-daemon-light qstat perl-doc libterm-readline-gnu-perl
  | libterm-readline-perl-perl make python-doc python-tk python-crypto-dbg python-crypto-doc python2.7-doc binutils binfmt-support heimdal-clients cifs-utils
The following NEW packages will be installed:
  bind9-host dnsutils geoip-database ifupdown iproute2 isc-dhcp-client isc-dhcp-common libarchive13 libatm1 libbind9-140 libdbi1 libdns-export162 libdns162 libgdbm3 libgeoip1
  libisc-export160 libisc160 libisccc140 libisccfg140 libldb1 liblwres141 liblzo2-2 libmnl0 libmysqlclient20 libnet-snmp-perl libpci3 libperl5.22 libpq5 libpython-stdlib libpython2.7
  libpython2.7-minimal libpython2.7-stdlib libsmbclient libsnmp-base libsnmp30 libtalloc2 libtdb1 libtevent0 libtirpc1 libwbclient0 libxtables11 monitoring-plugins
  monitoring-plugins-basic monitoring-plugins-common monitoring-plugins-standard mysql-common nagios-plugins netbase perl perl-modules-5.22 python python-crypto python-ldb
  python-minimal python-samba python-talloc python-tdb python2.7 python2.7-minimal rename rpcbind samba-common samba-common-bin samba-libs smbclient snmp
The following packages will be upgraded:
  perl-base
1 upgraded, 66 newly installed, 0 to remove and 41 not upgraded.
Need to get 28.2 MB of archives.
After this operation, 128 MB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 perl-base amd64 5.22.1-9ubuntu0.5 [1,284 kB]
Get:2 http://archive.ubuntu.com/ubuntu xenial/main amd64 libatm1 amd64 1:2.5.1-1.5 [24.2 kB]
Get:3 http://archive.ubuntu.com/ubuntu xenial/main amd64 libmnl0 amd64 1.0.3-5 [12.0 kB]
Get:4 http://archive.ubuntu.com/ubuntu xenial/main amd64 libgdbm3 amd64 1.8.3-13.1 [16.9 kB]
Get:5 http://archive.ubuntu.com/ubuntu xenial/main amd64 liblzo2-2 amd64 2.08-1.2 [48.7 kB]
Get:6 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libwbclient0 amd64 2:4.3.11+dfsg-0ubuntu0.16.04.17 [30.3 kB]
Get:7 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 perl-modules-5.22 all 5.22.1-9ubuntu0.5 [2,645 kB]
Get:8 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libperl5.22 amd64 5.22.1-9ubuntu0.5 [3,396 kB]
19% [8 libperl5.22 1,936 kB/3,396 kB 57%]

]]]]



##INSTALL PLUGIN
/opt/logstash/bin/logstash-plugin install logstash-input-nagioscheck





