
- [Firmware Tools Maintained by TonyLo](#firmware-tools-maintained-by-tonylo)
  - [Tools](#tools)
    - [---------- PL for UEFI (PLe) ----------](#-----------pl-for-uefi-ple-----------)
      - [Overview](#overview)
      - [Latest Version: **1.0.0.0** ](#latest-version-1000-)
      - [OS: **UEFI (x64/Aarch64/RiscV)**](#os-uefi-x64aarch64riscv)
      - [Features](#features)
    - [---------- PL ----------](#-----------pl-----------)
      - [Overview](#overview-1)
      - [Latest Version: **1.5.0.10**](#latest-version-15010)
      - [OS: **DOS**](#os-dos)
      - [Features](#features-1)
    - [---------- PL for Firmware (PLf) ----------](#-----------pl-for-firmware-plf-----------)
      - [Overview](#overview-2)
      - [Latest Version: **2.0.0.0**](#latest-version-2000)
      - [OS: **Windows**](#os-windows)
      - [Features](#features-2)
      - [Local/Remote Firmware/Hardware/OS Data Viewer](#localremote-firmwarehardwareos-data-viewer)
      - [Remote Platform Control](#remote-platform-control)
      - [Test Features](#test-features)
    - [---------- PL for Firmware (Linux) ----------](#-----------pl-for-firmware-linux-----------)
      - [Overview](#overview-3)
      - [Latest Version: **1.0.0.0**](#latest-version-1000)
      - [OS: **Linux**](#os-linux)
      - [Requirements](#requirements)
      - [Pre-built Binary](#pre-built-binary)
      - [Usage](#usage)
        - [Interactive Mode](#interactive-mode)
        - [Command-Line Mode](#command-line-mode)
      - [Options](#options)
      - [Features](#features-3)


# Firmware Tools Maintained by TonyLo

## Tools

Visit https://ubios.blogspot.com/ to see more details.

![img](ple.png)
![img](pl.jpg)
![img](plf_v2.png)
![img](plf.gif)
![img](plfl.png)

### ---------- PL for UEFI (PLe) ----------
https://github.com/vangoghynot/tools/tree/master/Tools/PLe<br>

![img](ple.png)

#### Overview
PLe (Project Lambda for UEFI) is an UEFI shell application for firmware (BIOS/BMC...etc) debugging and system inspection. It is the UEFI port of PL (Project Lambda).

#### Latest Version: **1.0.0.0** <br>
#### OS: **UEFI (x64/Aarch64/RiscV)**
#### Features
- **1.	PCI/PCI Express Register and Data Decode**
- **2.	System Memory Viewer** 
- **3.	ACPI Table Viewer**
- **4.	SMBIOS Table Viewer**
- **5.	CPU Information**
- **6.	UEFI System Tables/Handles/Variables/PCDs**
- **7.	UEFI Commander**
  <br> UEFI Protocols readiness check

### ---------- PL ----------
https://github.com/vangoghynot/tools/tree/master/Tools/PL<br>

![img](pl.jpg)

#### Overview
PL (Project Lambda) is a DOS application for firmware (BIOS/BMC...etc) debugging and system inspection. 

#### Latest Version: **1.5.0.10**

#### OS: **DOS**

#### Features
- **1.	PCI Bus/Device Information(PCI register read/write)**
- **2.	USB host controller information** 
- **3.	System memory read/write** 
- **4.	I/O address read/write**
- **5.	Index IO read/write**
- **6.	HD-Audio Controller Information**
  <br>(Include immediate VERB command, save codec cmd sequence as c file)
- **7.	AC97 Controller** 
- **8.	ACPI Table** 
- **9.	Disk read/write** 
- **10.	Int15h E820 maps advanced browsing**
- **11.	Multi Processor(MP) Table dump** 
- **12. Advanced Browsing experience** 
  <br> &nbsp;&nbsp;&nbsp; - Goto alternative view (Alt+G) Example: PCI<>IO or Memory, ACPI<>Memory<br>&nbsp;&nbsp;&nbsp; - Go back previous view(Alt+B)<br> 
- **13. Save View data to file (Save as TXT, HTML, Binary)** 


### ---------- PL for Firmware (PLf) ----------

https://github.com/vangoghynot/tools/tree/master/Tools/PLf)<br>

![img](plf.gif)

#### Overview
PLf (Project Lambda for Firmware) is a Windows GUI application for firmware (BIOS/BMC...etc) debugging and system inspection. 

#### Latest Version: **2.0.0.0**

#### OS: **Windows**

#### Features
- **1. UEFI/BIOS Smart Debug Information**
  - Error/Checkpoint/Guid Message clarification and color highlight<br> 
  - User defined message filter and color highight (Support two uder defined sets)<br> 
  - Quick message search and locate debug message<br> 
  - Save debug message on the fly (save to file)<br> 
  - Load debug message and analysis<br>
  
- **2. Addon Debug Message Functions**<br>
  - Calculate the timeing between two marked debug messages, can be used to measure and tune the BIOS POST time.<br> 
  (Click the 'Time' button on tool bar to open the 'Time' Windows, then use 'SPACE' key to mark the message.<br> 
  - GUID and Meaniningful name translation <br> 
    Lookup the BIOS source code at startup. Once the GUID is displayed in the debug message, convert the GUID to the driver/protocol name of the GUID.<br>
   (Need to set the 'GUID File Path' in the "Config" window to point to the UEFI/BIOS source code)<br>
   (Click the 'Decode Messages' button in the tool bar to enable/disable the trsnslation)<br>

#### Local/Remote Firmware/Hardware/OS Data Viewer
- **1. BIOS**<br>
  BIOS acpi/smbios/pci/uefi variables/OS data viewer.<br>

- **2. UEFI Variables<br>**  
  - **Need Administrator Right !!!** <br>
  - Read UEFI Variable in Windows<br>
  - UEFI Variable Commander to access specific variable

- **3. ACPI<br>**  
  - Dump ACPI Tables<br> 
  - Decompile SSDT/DSDT AML to ASL<br>
- **4. USB<br>**  
  - USB topology map<br> 
  - Save the USB topology map to TXT or ASL file<br>
  - Compare the USB topology map. Can be utilize to check if any USB device loss cross system boots. (support command line mode)<br> 
  - ACPI ASL _UPC and _PLD generation for USB devices.<br>
- **5. Disk<br>**  
  - **Need Administrator Right !!!** <br> 
  - View GPT/MBR information<br> 
  - Check disk boot capability.<br>
- **6. Security/Cryptograhy**<br>  
  - Key Management
    - **Generate keys**: RSA (1024/2048/3072/4096), ECDSA (P-256/P-384/P-521), AES (128/192/256), TripleDES
    - **Export keys**: XML, Base64, PEM formats; private and public key export
    - **Import keys** from file
  
  - Hash
    - **Hash algorithms**: MD5, SHA-1, SHA-256, SHA-384, SHA-512
    - Hash from text or file input
  
  - Cipher
    - **Encrypt/Decrypt**: AES-256-CBC (password-based) and other modes
    - File or text input

  - Digital Signing
    - **Sign**: RSA + SHA-256 and other combinations
    - **Verify** signatures

  - Certificate
    - **X.509 certificate** viewing and parsing<br>
  
- **7. Console Redirection<br>**  
  - Click 'Terminal' button in the tool bar to open the console window.<br> 
  - Support ANSI/VT100 (Similar to Putty/Teraterm)<br> 
  - Capture screen to file.<br>

#### Remote Platform Control
- **1. SUT Control (Control M/B)<br>**  
  - Need specific hardware<br> 
  - Support Web http/https request or windows exe/bat to control the M/B 
  - Support 'Level' or Pulse control<br> 
  - Capable to control the M/B AC power or Power Button<br>

#### Test Features

- Firmware Image Explorer <br>
  Supports firmware parsing for BIOS, UEFI, BMC, MCU formats with tree view
- Firmware Commander <br>
  Local and Remote File Manager along with Firmware, Hardware, and OS data viewer


### ---------- PL for Firmware (Linux) ----------

https://github.com/vangoghynot/tools/tree/master/Tools/PLfl)<br>

![img](plfl.png)

#### Overview
PLFL (Project Lambda for Firmware — Linux) is a console application for firmware (BIOS/BMC...etc) debugging and system inspection. It is the Linux port of PLF (Project Lambda for Firmware).

#### Latest Version: **1.0.0.0**

#### OS: **Linux**

#### Requirements

- Linux kernel 3.x+ with sysfs support
- Root/sudo for full access (ACPI, SMBIOS, raw disk, UEFI vars)
- Optional: `ipmitool` for BMC features
- Optional: `ipmi_devintf` kernel module for IPMI device access

#### Pre-built Binary

The static release binary has no external dependencies and runs on any x86_64 Linux system.

```bash
chmod +x plfl
sudo ./plfl
```
#### Usage

##### Interactive Mode

Run without arguments to start the interactive menu:

```bash
sudo ./plfl
```

The main menu presents all available features:

```
  PLF Features:
    1. UEFI Variables
    2. ACPI Tables
    3. USB Topology
    4. Disk Information
    5. BIOS Information (SMBIOS + ACPI + PCI + UEFI)
    6. TCPIP/DTP

  Extra PLFL Features:
    7. BMC Information
    8. Linux Information

  Other:
    S. SMBIOS/DMI Viewer
    P. PCI Device Viewer
    A. Export All (dump all info to file)
    Q. Quit
```

Type the number or letter of the feature to launch it.

##### Command-Line Mode

Run a specific feature directly from the command line:

```bash
sudo ./plfl <command>
```

| Command | Description |
|---------|-------------|
| `uefi-var` | Show UEFI variables |
| `acpi` | Show ACPI tables |
| `usb` | Show USB topology |
| `disk` | Show disk information |
| `bios` | Show BIOS information (combined) |
| `smbios` | Show SMBIOS/DMI data |
| `pci` | Show PCI devices |
| `dtp` | DTP client/server (interactive) |
| `dtp-listen [port]` | DTP server (headless, default port 29760) |
| `bmc` | Show BMC/IPMI information |
| `linux` | Show Linux system information |
| `export` | Export all information to file |

#### Options

| Option | Description |
|--------|-------------|
| `-h`, `--help` | Show usage help |
| `-v`, `--version` | Show version |

#### Features

- 1. UEFI Variables

Enumerates and inspects UEFI variables from `/sys/firmware/efi/efivars/`.

Displays variable names, GUIDs, attributes (NV, BT, RT, etc.), and data contents. Requires root access.

- 2. ACPI Tables

Lists and decodes ACPI tables from `/sys/firmware/acpi/tables/`.

Shows table signatures, sizes, and raw hex data. Requires root access.

- 3. USB Topology

  Displays a full USB device tree with:
  - Vendor ID / Product ID
  - Device speed (Low/Full/High/Super)
  - Device class and subclass
  - Interface details

- 4. Disk Information

  Shows physical disks and partition tables:
  - MBR and GPT partition table parsing
  - Partition sizes and types
  - Raw LBA sector access

- 5. BIOS Information

  Combined view of system firmware information:
  - SMBIOS/DMI structures
  - ACPI tables
  - PCI devices
  - UEFI variables summary

- 6. TCPIP/DTP

  DTP client/server for remote firmware debugging over TCP.

  - Default port: 29760
  - JSON payload handshake
  - CRC-32 frame integrity
  - Log event streaming
  - Remote UEFI variable access
  - File transfer
  - Compatible with PLF Windows DTP implementation

  **Interactive mode:** `./plfl dtp`<br>
  **Headless server:** `./plfl dtp-listen [port]`<br>

- 7. BMC Information

  Displays BMC/IPMI data via `ipmitool`:
  - Sensors
  - FRU (Field Replaceable Unit)
  - SEL (System Event Log)
  - LAN configuration
  - BMC info

  Requires `ipmitool` to be installed.

- 8. Linux Information

  Shows Linux system information:
  - Kernel version and parameters
  - CPU details
  - Memory usage
  - Network interfaces
  - Loaded kernel modules
  - Mount points

- SMBIOS/DMI Viewer (S)

  Full SMBIOS structure parser with decoded fields:
  - BIOS, System, Baseboard information
  - Processor and memory details
  - TPM information

- PCI Device Viewer (P)

  PCI configuration space viewer:
  - Device class and subclass
  - Vendor/Device IDs
  - Driver information

- Export <br>
All modules support exporting collected data to file.
  - Export All (A)<br>
Gathers information from all modules and writes to a single file.

    Supported formats:
    - **TXT** — Plain text
    - **HTML** — Formatted HTML
    - **JSON** — Structured JSON
    - **Markdown** — Markdown document

  When prompted, select the format and output filename.

  - Command-Line Export

  ```bash
  sudo ./plfl export
  ```


