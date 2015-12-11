# mit.zabbix-agent.disk-performance

Based on https://github.com/grundic/zabbix-disk-performance with the following changes:

* `Template Disk Performance.xml`
    * Switched from "Zabbix Agent" to "Zabbix Agent active"
    * Changed history from 30 to 7 days
    * Uses DEVICE and DEVICENAME
* `zabbix-lld-disk` (`lld-disks.py`)
    * DEVICENAME will be "vg--lv" if the devices begins with dm-
* Can now be used as ansible module

# Notes

* All active items are using `/proc/diskstats`, see [iostats.txt](https://www.kernel.org/doc/Documentation/iostats.txt) for details.
* The default zabbix items (`vfs.dev.read` and `vfs.dev.write`) are included in the template but disabled by default.
