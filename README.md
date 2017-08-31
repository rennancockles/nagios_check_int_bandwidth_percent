# nagios_check_int_bandwidth_percent

Script to check the interface bandwidth usage in percents

&nbsp;

&nbsp;

### Usage 

check_int_bandwidth_percent HOSTADDR IF_NAME COMMUNITY DIRECTION LINK_SPEED

&nbsp;

HOSTADDR = Host IP address

IF_NAME = Interface name

COMMUNITY = SNMP Community

DIRECTION = Traffic direction - IN ou OUT

LINK_SPEED = Link speed in Mbps: 10Gbps = 10000

&nbsp;

&nbsp;

### Using with nagios

To use with nagios, copy the script to /usr/lib64/nagios/plugins/.

Edit the command file in /etc/nagios/conf.d:

```
define command{
        command_name    check_int_bandwidth_percent
        command_line    $USER1$/check_int_bandwidth_percent $ARG1$ $ARG2$ $ARG3$ $ARG4$ $ARG5$
}
```
