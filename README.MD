# Ubuntu Desktop 24.04 LTS – Autoinstall

This repository contains an `autoinstall.yaml` for an automated, unattended
installation of Ubuntu Desktop 24.04 LTS. It was created for a programming
workshop and sets up a ready-to-use development environment.

---

## What gets installed

| Category | Software |
|---|---|
| **IDE & Editors** | Visual Studio Code, Arduino IDE |
| **Programming** | Python 3, pip, venv, build-essential, Java 17 |
| **Python Libraries** | Adafruit CircuitPython DHT (in venv) |
| **Hardware Tools** | i2c-tools, libgpiod2 |
| **Office & Browser** | LibreOffice (DE), Firefox |
| **Multimedia** | VLC |
| **Utilities** | git, curl, wget, htop, vim, nano, net-tools |
| **Imaging** | Raspberry Pi Imager |

---

## Requirements

- A bootable USB stick with the **Ubuntu Desktop 24.04 LTS** ISO
- A second USB stick containing the `autoinstall.yaml`
- An active internet connection via ethernet cable (DHCP)
- Target machine with an internal SSD

---

## Usage

### 1. Prepare the USB sticks

- Create a bootable USB stick with the **Ubuntu Desktop 24.04 LTS** ISO
  using a tool like **Rufus** or **Balena Etcher**.
- Copy the `autoinstall.yaml` to the root directory of a second USB stick.

### 2. Boot from the Ubuntu Live ISO

- Connect both USB sticks to the target machine.
- Boot the target machine from the Ubuntu Desktop 24.04 LTS USB stick.
- Wait for the Live desktop to load.

### 3. Launch the installer

- Click on **Install Ubuntu** on the Live desktop to open the GUI installer.

### 4. Select the autoinstall.yaml

- In the installer, navigate to the **Autoinstall** option.
- When prompted, select the `autoinstall.yaml` from the second USB stick.

### 5. Wait for the installation to complete

- The installation will run fully automated based on the `autoinstall.yaml`.
- All software packages and Snaps will be
  downloaded and installed automatically during the process.
- Once finished, the system will reboot automatically.

---

## Notes

> ⚠️ **The entire primary disk will be wiped and formatted without any prompt.**
> Make sure only the target SSD and the boot USB stick are connected during
> installation to avoid accidental data loss.

> ⚠️ **An active internet connection via ethernet cable is required** during
> installation, as software packages and Snaps are downloaded during the
> installation process.