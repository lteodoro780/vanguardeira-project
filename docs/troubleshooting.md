# Troubleshooting

## Overview

Due to the hardware variations commonly found in RK322x TV Box devices, multiple issues were encountered during deployment and testing.

This document summarizes the most common problems and possible solutions.

---

## No Video Output

### Symptoms

* Black screen after boot
* No HDMI signal
* Device powers on but shows no image

### Possible Causes

* Incorrect DTB selection
* Unsupported HDMI configuration
* Corrupted image

### Recommended Actions

* Test alternative DTB files
* Reflash the image
* Verify HDMI cable and monitor compatibility

---

## Boot Failure

### Symptoms

* Device stuck during boot
* Infinite reboot loop
* System does not start

### Possible Causes

* Corrupted eMMC installation
* Unsupported Armbian image
* Bootloader incompatibility

### Recommended Actions

* Reinstall using Multitool
* Restore backup image
* Test different Armbian builds

---

## eMMC Detection Problems

### Symptoms

* Internal storage not detected
* Installation failure
* Read/write instability

### Possible Causes

* Hardware revision differences
* Kernel compatibility issues
* Storage degradation

### Recommended Actions

* Use updated community builds
* Verify storage integrity
* Attempt SD card boot instead of eMMC installation

---

## Poor Performance

### Symptoms

* System freezes
* High RAM usage
* Slow application startup

### Recommended Actions

* Disable unnecessary services
* Use lightweight applications
* Configure swap memory
* Reduce background processes

---

## Network Problems

### Symptoms

* Ethernet not detected
* Unstable connection
* No IP address assignment

### Possible Causes

* Driver limitations
* DHCP issues
* Hardware incompatibility

### Recommended Actions

* Test static IP configuration
* Verify switch connectivity
* Update kernel if possible

---

## Overheating

### Symptoms

* Random reboots
* System instability
* Thermal throttling

### Recommended Actions

* Improve ventilation
* Add passive cooling
* Reduce sustained workload

---

## SSH Access Failure

### Symptoms

* Connection timeout
* Authentication failure

### Recommended Actions

* Verify IP address
* Confirm SSH service status

```bash id="gj9vmi"
sudo systemctl status ssh
```

* Check firewall configuration

---

## Recovery Strategy

The deployment process always included:

* eMMC backup before installation
* Recovery image preparation
* SD card fallback boot option

---

## Notes

Due to the unofficial and community-supported nature of RK322x Linux environments, troubleshooting and experimentation were important parts of the deployment process.
