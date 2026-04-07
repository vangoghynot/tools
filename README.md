# Firmware Tools Maintained by TonyLo

## Tools

Visit https://ubios.blogspot.com/ to see more details.

![img](ple.png)
![img](pl.jpg)
![img](plf.gif)

### PL for UEFI (PLe)
https://github.com/vangoghynot/tools/tree/master/Tools/PLe<br>

![img](ple.png)

#### Latest Version: **v0.9.7** <br>
#### OS: **UEFI (x64/Aarch64/RiscV)**
#### Features:
- **1.	PCI/PCI Express**
- **2.	System memory**
- **3.	ACPI**
- **4.	SMBIOS**
- **5.	CPU**
- **6.	UEFI System Tables/Handles/Variables/PCDs**
- **7.	UEFI Commander**
  <br> UEFI Protocols readiness check

### PL
https://github.com/vangoghynot/tools/tree/master/Tools/PL<br>

![img](pl.jpg)
#### Latest Version: **1.5.0.10**
#### OS: **DOS**
#### Features: 
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


### PL for Firmware (PLf)

https://github.com/vangoghynot/tools/tree/master/Tools/PLf)<br>

![img](plf.gif)

#### Latest Version: **1.0.1.12**
#### OS: **Windows**
#### Features: <br>
- **1. UEFI/BIOS Smart Debug Information**
  - Error/Checkpoint/Guid Message clarification and color highlight<br> - User defined message filter and color highight (Support two uder defined sets)<br> - Quick message search and locate debug message<br> - Save debug message on the fly (save to file)<br> - Load debug message and analysis<br>
- **2. Addon Debug Message Functions**<br>
  - Calculate the timeing between two marked debug messages, can be used to measure and tune the BIOS POST time.<br> (Click the 'Time' button on tool bar to open the 'Time' Windows, then use 'SPACE' key to mark the message.<br> - GUID and Meaniningful name translation <br> * Lookup the BIOS source code at startup. Once the GUID is displayed in the dbeug message, convert the GUID to the driver/protocol name of the GUID.<br>* (Need to set the 'GUID File Path' in the "Config" window to point to the UEFI/BIOS source code)<br>* (Click the 'Decode Messages' button in the tool bar to enable/disable the trsnslation.<br>

#### **Local/Remote Firmware/Hardware/OS Data Viewer:**<br>
- **1. BIOS**<br>
BIOS acpi/smbios/pci/uefi variables/OS data viewer.<br>

- **2. UEFI Variables<br>**  
  - **Need Administrator Right !!!** <br>- 
  - Read UEFI Variable in Windows<br>
  - UEFI Variable Commander to access specific variable

- **3. ACPI<br>**  - Dump ACPI Tables<br> - Decompile SSDT/DSDT AML to ASL<br>
- **4. USB<br>**  - USB topology map<br> - Save the USB topology map to TXT or ASL file<br>* - Compare the USB topology map. Can be utilize to check if any USB device loss cross system boots. (support command line mode)<br> - ACPI ASL _UPC and _PLD generation for USB devices.<br>
- **5. Disk<br>**  - **Need to launch the application in Administrator Right !!!** <br> - View GPT/MBR information<br> - Check disk boot capability.<br>
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
- **7. Console Redirection<br>**  - Click 'Terminal' button in the tool bar to open the console window.<br> - Support ANSI/VT100 (Similar to Putty/Teraterm)<br> - Capture screen to file.<br>

#### **Remote Platform Control**<br>
- **1. SUT Control (Control M/B)<br>**  - Need specific hardware<br> - Support Web http/https request or windows exe/bat to control the M/B - Support 'Level' or Pulse control<br> - Capable to control the M/B AC power or Power Button<br>


