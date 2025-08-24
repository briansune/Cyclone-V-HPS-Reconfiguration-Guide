# Cyclone-V-HPS-Reconfiguration-Guide

## Markdown project to log the latest kernel reconfiguration method.

### Issues

According to old kernel 4.xx:

The reload is very easy and simple via /sys/class/fpga/xxx/firmware

However latest kernel no longer exist.

### Solutions

References:

[Vendor](https://www.intel.com/content/www/us/en/developer/articles/technical/reconfigure-an-fpga-from-the-cloud-with-containers.html)

[Forum](https://forum.rocketboards.org/t/how-to-program-fpga-from-hps-de10-nano/1278/6)

As mentioned (not confirm), since 3.10 kernel and no longer support on 4.x.

The method is very simply and stable to handle via the dtbo.

As for the driver just runs the command and reprobe the devices:

```
sudo modprobe -r xxxxxx
sudo modprobe xxxxxx
```
