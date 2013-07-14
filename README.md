##DS2413
======

DS2413 RaspberryPI 1Wire Dual Relay Modul for  
Linux vz 3.6.11+ #371 PREEMPT Kernel

###Installation
============

###Operation
============

echo -e '\x01' |dd of=/sys/bus/w1/devices/3a-0000000d2c0e/output bs=1 count=1 >/dev/null 2>&1   
echo -e '\xff' |dd of=/sys/bus/w1/devices/3a-0000000d2c0e/output bs=1 count=1 >/dev/null 2>&1
