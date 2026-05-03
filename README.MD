# 🛠️ Custom ESXi ISO Collection

This repository contains customized **VMware ESXi** installers (ISO) optimized for Homelabs, legacy hardware, and modern consumer-grade networking. These builds include community-sourced drivers and critical bug fixes not found in the official releases.

---

## 📂 Available Versions

### 1. ESXi 8.0 Update 3i (v8.0.3)
**Build:** 25205845  
**Focus:** Modern features on legacy CPUs & USB/Realtek networking.

#### 🚀 Features:
*   **Integrated Drivers:** 
    *   `USB Network Native Driver`: Wide support for USB-to-Ethernet adapters.
    *   `Realtek Native Driver`: Community support for onboard Realtek NICs.
*   **Kernel Optimizations (`BOOT.CFG`):**
    *   `allowLegacyCPU=true`: Bypasses hardware checks for Sandy/Ivy Bridge, Westmere, and Bulldozer CPUs.
    *   `systemMediaSize=min`: Limits **ESX-OSData** to 32GB to save disk space.

---

### 2. ESXi 6.7 Update 3v (v6.7.0)
**Build:** 24514018 (Latest Patch 202503001)  
**Focus:** Maximum legacy compatibility and SATA/NVMe support.

#### 🚀 Features:
*   **Hardware Support (VIBs):**
    *   `net55-r8168` & `net-r8125`: Realtek 1GbE and 2.5GbE support.
    *   `sata-xahci`: Support for ASMedia (ASM1166) and other SATA expansion cards.
    *   `nvme-community`: Enhanced NVMe SSD compatibility.
    *   `net-igb`: Legacy Intel LAN support.
*   **Critical UI Fix:**
    *   Replaced `esx-ui-1.43.10` with **`v1.33.7`**. This restores the ability to attach existing `.vmdk` disks via the Web Host Client, fixing a well-known bug in the final 6.7 builds.

---

## 💻 Installation & Usage

1.  **Download** the desired ISO from the [Releases](https://github.com/tu-usuario/tu-repo/releases) section.
2.  **Flash** to a USB drive using [Rufus](https://rufus.ie/) or [Ventoy](https://www.ventoy.net/).
3.  **Boot** your server. 
    *   *Note for 8.0u3i:* If you have an unsupported CPU, the `allowLegacyCPU=true` flag is already embedded in the boot configuration.

## ⚠️ Disclaimer
These images are **not official VMware products**. They are intended for **educational, home-lab, and testing purposes only**. Use them at your own risk.

---

> **Looking for more?** If you need specific drivers added to these builds, feel free to open an Issue or a Pull Request.
