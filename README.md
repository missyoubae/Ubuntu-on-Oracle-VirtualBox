# Ubuntu on Oracle VirtualBox

![Alt image](https://github.com/missyoubae/Ubuntu-on-Oracle-VirtualBox/blob/0055ca5139d1ae4c81ed69325a622e9ba68504d2/0_lZod12Dzva5hOie4.jpg)

A step-by-step guide to installing and running Ubuntu on Oracle VirtualBox.

## 📋 Requirements

* Oracle VirtualBox
* Ubuntu ISO image (22.04 LTS or later)
* Minimum 4 GB RAM (8 GB recommended)
* At least 25 GB free disk space

## 🚀 Installation

### 1. Download Ubuntu

Download the latest Ubuntu Desktop ISO from the official Ubuntu website.

### 2. Create a Virtual Machine

1. Open VirtualBox.
2. Click **New**.
3. Configure:

   * **Name:** Ubuntu
   * **Type:** Linux
   * **Version:** Ubuntu (64-bit)
4. Allocate memory (4 GB recommended).
5. Create a virtual hard disk:

   * VDI (VirtualBox Disk Image)
   * Dynamically Allocated
   * 25 GB or larger

### 3. Attach Ubuntu ISO

1. Select the VM and click **Settings**.
2. Navigate to **Storage**.
3. Under **Controller: IDE**, select **Empty**.
4. Choose the Ubuntu ISO file.

### 4. Install Ubuntu

1. Start the VM.
2. Select **Install Ubuntu**.
3. Follow the installation wizard.
4. Create a user account and password.
5. Reboot after installation completes.

## 🔧 Post-Installation

Update the system:

```bash
sudo apt update
sudo apt upgrade -y
```

Install Guest Additions:

```bash
sudo apt install build-essential dkms linux-headers-$(uname -r)
```

Then from VirtualBox:

```text
Devices → Insert Guest Additions CD Image
```

Run:

```bash
sudo mount /dev/cdrom /mnt
sudo /mnt/VBoxLinuxAdditions.run
sudo reboot
```

## 🌐 Network Modes

| Mode            | Description                                 |
| --------------- | ------------------------------------------- |
| NAT             | Internet access through host                |
| Bridged Adapter | VM acts as a separate device on the network |

## 🛠 Useful Commands

Check Ubuntu version:

```bash
lsb_release -a
```

Check IP address:

```bash
ip addr
```

Update packages:

```bash
sudo apt update && sudo apt upgrade -y
```

## 📸 Screenshots

Add screenshots of:

* VirtualBox VM configuration
* Ubuntu installation process
* Ubuntu desktop after installation

Example:

```markdown
![Ubuntu Desktop](screenshots/ubuntu-desktop.png)
```

## 📁 Project Structure

```text
Ubuntu-on-Oracle-VirtualBox/
├── README.md
├── screenshots/
└── docs/
```

## 🤝 Contributing

Contributions, issues, and feature requests are welcome.

## 📄 License

This project is licensed under the MIT License.
