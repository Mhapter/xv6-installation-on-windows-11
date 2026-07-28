# 🛠️ xv6 RISC-V Kernel — Enterprise Installation & Setup Guide

> **Standard Operating Environment & Deployment Manual**  
> A comprehensive reference for configuring, compiling, and running the MIT xv6 RISC-V kernel inside a virtualized Linux development container on Windows 11.

---

## 🌐 Quick Access

* 🚀 **[Interactive Live Documentation]( https://mhapter.github.io/xv6-installation-on-windows-11/)**
* 📦 **[GitHub Source Repository](https://github.com/Mhapter/xv6-installation-on-windows-11)**
* 📄 **`index.html`** — Web documentation source

---

## 📋 System Requirements & Prerequisite Stack

| Layer | Recommended Specification |
| :--- | :--- |
| **Host OS** | Windows 11 (64-bit) |
| **Hypervisor** | VMware Workstation Pro / Player or WSL2 |
| **Guest OS** | Ubuntu 22.04 LTS / 24.04 LTS |
| **Compiler Toolchain** | `gcc-riscv64-unknown-elf` or `gcc-riscv64-linux-gnu` (v8.0+) |
| **Emulator** | QEMU (`qemu-system-misc` / `qemu-system-riscv64`) |

---

## ⚙️ Automated Setup Sequence

### 1. Toolchain & Environment Provisioning
Run the following package initialization inside your Ubuntu guest shell:

```bash
sudo apt-get update && sudo apt-get upgrade -y
sudo apt-get install -y \
    git \
    build-essential \
    gdb-multiarch \
    qemu-system-misc \
    gcc-riscv64-linux-gnu \
    binutils-riscv64-linux-gnu
