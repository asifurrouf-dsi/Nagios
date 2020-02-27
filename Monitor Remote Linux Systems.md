# Monitor Remote Linux Systems With Nagios

On Remote Linux System Nagios Remote Plugin Executor (abbreviated as NRPE) plugin allows you to monitor 
applications and services running on remote Linux / Windows hosts. This NRPE Add-on helps Nagios to monitor
local resources like CPU, Memory, Disk, Swap, etc. of the remote host

## Install NRPE Add-on & Nagios Plugins at CentOS / RHEL

NRPE Server and Nagios plugins are available in the EPEL repository for CentOS / RHEL.
So, configure the EPEL repository your CentOS / RHEL system.


### CentOS 8 / RHEL 8 ###

rpm -ivh https://dl.fedoraproject.org/pub/epel/epel-release-latest-8.noarch.rpm

### CentOS 7 / RHEL 7 ###

rpm -ivh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm

### CentOS 6 / RHEL 6 ###

rpm -ivh https://dl.fedoraproject.org/pub/epel/epel-release-latest-6.noarch.rpm


### Use the following command to install NRPE Add-on and Nagios plugins.

yum install -y nrpe nagios-plugins-all

## Configure NRPE Add-on

Modify the NRPE configuration file to accept the connection from the Nagios server, 
Edit the /etc/nagios/nrpe.cfg file.

### CentOS / RHEL ###

vi /etc/nagios/nrpe.cfg

### Ubuntu / Debian ###

sudo nano /etc/nagios/nrpe.cfg

Add the Nagios servers IP address, separated by comma like below.

```
allowed_hosts= 10.0.0.153
```

