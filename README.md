DS2413
======

Replace all files in the target directory '/lib/modules/3.6.11+/kernel/drivers/w1'

---

# /etc/modules: kernel modules to load at boot time.
#
# This file contains the names of kernel modules that should be loaded
# at boot time, one per line. Lines beginning with "#" are ignored.
# Parameters can be specified after the module name.

# Part of DS2482 I²C 1-Wire® Master to Volkszaehler 'RaspberryPI deamon'.
i2c-bcm2708
i2c-dev
ds2482
w1_therm
w1_ds2413

---

'ls -la /sys/bus/w1/devices'

DS2413 Slaves starts with '3a'

---
 
Must be root! Sodu won't work :(

echo -e '\x01' |dd of=/sys/bus/w1/devices/3a-0000000d2c0e/output bs=1 count=1
echo -e '\x02' |dd of=/sys/bus/w1/devices/3a-0000000d2c0e/output bs=1 count=1
echo -e '\xff' |dd of=/sys/bus/w1/devices/3a-0000000d2c0e/output bs=1 count=1
