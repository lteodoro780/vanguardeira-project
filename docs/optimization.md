# Optimization

## Overview

The RK322x devices used in the Vanguardeira project had limited hardware resources, especially the 1 GB RAM configuration.

System optimization was required to provide stable operation in educational environments.

---

## Optimization Goals

* Reduce RAM usage
* Improve boot time
* Maintain system stability
* Reduce background activity
* Improve responsiveness

---

## Lightweight Environment

The deployment focused on lightweight Linux environments and minimal background services.

Key objectives:

* Lower idle RAM usage
* Faster startup
* Reduced CPU overhead

---

## Swap Configuration

Swap memory was used to improve stability under memory pressure.

Example configuration:

```bash id="c9fhpw"
sudo fallocate -l 2G /swapfile
sudo chmod 600 /swapfile
sudo mkswap /swapfile
sudo swapon /swapfile
```

Persistent configuration:

```bash id="8a3cwf"
echo '/swapfile none swap sw 0 0' | sudo tee -a /etc/fstab
```

---

## Reduced Background Services

Unnecessary services were disabled whenever possible.

Examples:

```bash id="9k0we6"
sudo systemctl disable bluetooth
sudo systemctl disable cups
```

---

## Storage Optimization

Due to limited eMMC performance:

* Temporary files were minimized
* Cache usage was reduced
* Lightweight applications were preferred

---

## Application Selection

The environment prioritized lightweight applications for educational usage.

Examples:

* Lightweight browsers
* Minimal office tools
* Basic educational software

---

## Thermal Considerations

The RK322x devices could become unstable under prolonged high load.

Recommended practices:

* Passive cooling improvements
* Ventilation adjustments
* Avoid sustained heavy workloads

---

## Stability Notes

System stability depended on:

* Correct DTB selection
* Stable Armbian builds
* Controlled memory usage
* Minimal background processes

---

## Results

Despite hardware limitations, the devices were successfully adapted for:

* Educational activities
* Basic productivity
* Linux learning environments
* Lightweight infrastructure tasks
