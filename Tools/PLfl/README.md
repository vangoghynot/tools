# PLF(L) - Project Lambda for Firmware (Linux)

Linux console application for firmware debugging and system inspection.
Linux port of PLF (Project Lambda for Firmware).

## Features

### PLF Features
| # | Feature | Description |
|---|---------|-------------|
| 1 | **UEFI Variables** | Enumerate and inspect UEFI variables from `/sys/firmware/efi/efivars/` |
| 2 | **ACPI Tables** | View and decode ACPI tables from `/sys/firmware/acpi/tables/` |
| 3 | **USB Topology** | Full USB device tree with VID/PID, speed, classes, interfaces |
| 4 | **Disk Information** | Physical disks, MBR/GPT partition tables, raw sector access |
| 5 | **BIOS Information** | Combined SMBIOS + ACPI + PCI + UEFI variables view |
| 6 | **TCPIP/DTP** | client/server for remote debugging |

### Extra PLFL Features
| # | Feature | Description |
|---|---------|-------------|
| 7 | **BMC Information** | BMC/IPMI data via ipmitool (sensors, FRU, SEL, LAN, etc.) |
| 8 | **Linux Information** | Kernel, CPU, memory, network, modules, mount points |

### Additional Viewers
- **SMBIOS/DMI** — Full SMBIOS structure parser (BIOS, System, Baseboard, Processor, Memory, TPM)
- **PCI Devices** — PCI config space viewer with class/driver info

### Export Formats
All modules support export to **TXT**, **HTML**, **JSON**, and **Markdown**.

## Usage

### Interactive Mode
```bash
sudo ./plfl
```

### Command-Line Mode
```bash
sudo ./plfl uefi-var    # UEFI variables
sudo ./plfl acpi        # ACPI tables
sudo ./plfl usb         # USB topology
sudo ./plfl disk        # Disk information
sudo ./plfl bios        # Combined BIOS info
sudo ./plfl smbios      # SMBIOS/DMI data
sudo ./plfl pci         # PCI devices
sudo ./plfl dtp         # DTP 1.0 client/server
sudo ./plfl bmc         # BMC/IPMI info
sudo ./plfl linux       # Linux system info
sudo ./plfl export      # Export all to file
```

### Export All
```bash
sudo ./plfl export      # Interactive export
```

## Requirements

- Linux kernel 3.x+ with sysfs support
- Root/sudo for full access (ACPI, SMBIOS, raw disk, UEFI vars)

