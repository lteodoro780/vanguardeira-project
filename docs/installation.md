# Installation

## Overview

The deployment process used Armbian community images together with Multitool to prepare and install Linux on RK322x-based TV Box devices.

---

## Requirements

### Hardware

* MXQ 5G TV Box
* MicroSD card
* USB keyboard
* HDMI monitor
* Ethernet connection (recommended)

### Software

* Armbian image for RK322x
* Multitool image
* Balena Etcher or similar imaging tool

---

## Preparing the SD Card

Flash the Multitool image to the MicroSD card using:

* Balena Etcher
* Raspberry Pi Imager
* dd command on Linux

---

## Booting Multitool

1. Insert the MicroSD card into the TV Box
2. Connect HDMI and keyboard
3. Power on the device
4. Wait for Multitool environment

---

## Backup Procedure

Before modifying the internal storage:

1. Open Multitool
2. Select backup option
3. Save eMMC backup to external storage

This step was important for recovery procedures.

---

## Installing Armbian

1. Copy the Armbian image to the Multitool storage
2. Select "Burn image to eMMC"
3. Choose the correct Armbian image
4. Wait for installation completion

---

## First Boot

After installation:

1. Remove the SD card
2. Reboot the device
3. Wait for Armbian initialization

Initial setup includes:

* User creation
* Password configuration
* Locale selection

---

## Recommended Configuration

Recommended post-installation steps:

```bash
sudo apt update && sudo apt upgrade -y
```

Install lightweight utilities and minimize unnecessary services whenever possible.

---

## Optimization Notes

Due to the 1 GB RAM limitation, the environment was optimized for:

* Low memory usage
* Lightweight applications
* Reduced background services
* Basic educational workloads

---

## Common Issues

### No Boot

Possible causes:

* Incorrect DTB
* Corrupted image
* Unsupported hardware revision

### eMMC Detection Failure

Possible causes:

* Hardware variation
* Incompatible kernel
* Bootloader limitations

### Performance Issues

Recommended actions:

* Disable unnecessary services
* Use lightweight desktop environment
* Avoid browser-heavy workloads
