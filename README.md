Python WMI Client
=================

Communicate with Windows machines via WMI from *nix machines.

Based on [py-wmi-client](https://github.com/ProjectPatatoe/py-wmi-client/) by David Lundgren.

Installation
------------

To install simply run the following:

```bash
$ pip install wmic
```

##### Requirements

* impacket >= 0.9.13
* natsort >= 3

Usage
-----

The simplest way to run it is similar to the following

```wmic -A /etc/nagios3/wmic_auth.ini //ServerName "SELECT * FROM Win32_PerfFormattedData_PerfOS_Memory"```

##### Available arguments

* ```-A```, ```--authentication-file``` : INI style file that
    * ```domain``` : optional, default: WORKGROUP
    * ```username``` : required
    * ```password``` : required
* ```-U```,```--user``` : format ```[DOMAIN\]USERNAME[%PASSWORD]```
* ```--delimiter``` : how to separate the colums, default: |
* ```--namespace``` : namespace, default: //./root/cimv2

##### Notes

* If you do not supply a domain, then the script defaults to ```WORKGROUP```
* You must use either a file or user argument

License
-------

MIT
