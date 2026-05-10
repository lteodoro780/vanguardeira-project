# Hardware

## Overview

The Vanguardeira project reused low-cost TV Box devices as Linux-based educational workstations.

Most devices were based on ARM architecture and adapted to run lightweight Linux environments using community-supported distributions.

---

## Tested Devices

### MXQ 5G TV Box

The MXQ 5G was one of the primary devices used during testing and deployment.

### Hardware Specifications

| Component    | Specification    |
| ------------ | ---------------- |
| Platform     | ARM              |
| SoC          | Rockchip RK322x  |
| RAM          | 1 GB DDR3        |
| Storage      | eMMC             |
| Connectivity | Ethernet / Wi-Fi |
| USB Ports    | USB 2.0          |
| Video Output | HDMI             |

---

## Operating System

The devices were deployed using Armbian community builds.

### Distribution

* Armbian
* Debian-based environment
* Lightweight Linux environment

---

## Installation Method

The installation process used Multitool for:

* eMMC backup
* Boot preparation
* Armbian installation
* Recovery procedures

---

## Deployment Goals

Key deployment objectives:

* Stable Linux operation on low-end hardware
* Low memory usage
* Fast boot time
* Reduced infrastructure cost
* Educational workstation deployment

---

## Technical Challenges

Common challenges during deployment:

* Device Tree Blob (DTB) compatibility
* eMMC detection issues
* Bootloader limitations
* RK322x hardware variations
* Limited RAM optimization
* GPU driver limitations

---

## Linux Compatibility

The project relied on:

* Community-maintained Armbian images
* RK322x Linux support
* ARM optimization
* Embedded Linux troubleshooting

---

## Notes

Despite the limited hardware resources, the devices were successfully adapted for educational and laboratory usage through lightweight Linux environments and optimized system configuration.
