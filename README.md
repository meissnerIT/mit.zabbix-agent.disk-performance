# mit.zabbix-agent.disk-performance

Based on https://github.com/grundic/zabbix-disk-performance with the following changes:

* `Template Disk Performance.xml`
    * Switched from "Zabbix Agent" to "Zabbix Agent active"
    * Changed history from 30 to 7 days
    * Uses DEVICE and DEVICENAME
* `zabbix-lld-disk` (`lld-disks.py`)
    * DEVICENAME will be "vg--lv" if the devices begins with dm-
* Can now be used as ansible module

