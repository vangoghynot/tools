Visit https://ubios.blogspot.com/ to see more details.

--------------------------------
# v1.0.1.13 (2026.4.6)
--------------------------------
Few improvements and bug fixes.

Features: Firmware Commander (Trial version)  
- Local and Remote File Manager along with Firmware, Hardware, and OS data viewer
(Raise request to unlock this feature)

--------------------------------
# v1.0.1.12 (2026.4.5)
--------------------------------
Improvements:
-Standardize export data function cross all viewers.

--------------------------------
# v1.0.1.10 (2026.4.5)
--------------------------------
Features:
-Add Remote UEFI Variable Compare

--------------------------------
# v1.0.1.9 (2026.4.4)
--------------------------------
Features:
-Add TCP/IP Transport
  Client mode: connect to remote PLF server for debug log streaming
  Server mode: listen for incoming PLF client connections

--------------------------------
# v1.0.1.8 (2026.4.3)
--------------------------------
Features:
-Add ACPI Table Viewer.
  ACPI table content decode.
  AML-to-ASL disassembler for DSDT/SSDT tables
  Add multi-format save (TXT, HTML, JSON) with Save/Save All for single and multiple acpi tables save

--------------------------------
# v1.0.1.7 (2026.4.1)
--------------------------------
Features:
-Complete Security Toolkit with 5 functional tabs
  Key: RSA/ECDSA/AES/TripleDES key generation, import, export (XML/PEM/Base64/Hex)
  Hash: MD5/SHA-1/SHA-256/SHA-384/SHA-512 with text/file input
  Cipher: AES-256/128-CBC, TripleDES-CBC, RSA-OAEP encrypt/decrypt
  Signing: RSA+SHA, ECDSA+SHA, HMAC sign and verify
  Certificate: X.509 cert viewer with full chain validation
  Tools: Base64, password generator, PEM/DER converter, file checksum

--------------------------------
# v1.0.1.6 (2026.3.30)
--------------------------------
Features:
-Add 'BIOS' view for ACPI Tables, SMBIOS, PCI Devices, UEFI Variables, OS Info, and Boot Performance metrics in OS Information
-Add 'UEFI Var' view for UEFI variables read in OS
  Export 'UEFI variable list' tree as (TXT, HTML, JSON, Markdown)
  Friendly decode for known variables (SecureBoot, BootOrder, Boot####, etc.)
  ASN1 Decode for Secure Boot certificate variables (PK, KEK, db, dbx)
-Add 'USB Commander' for USB control transfers via WinUSB API
-Add Raw Data hex dump tree nodes in Disk Info
  Physical disks: MBR, GPT Header, Backup GPT, GPT Partition Entries
  Logical volumes: VBR (Volume Boot Record) via live read

Improvements:
-Fix UEFI variable name list (ErrOut, ErrOutDev, db/dbx/dbt/devAuthBoot) per Uefi 2.11 specification update

--------------------------------
# v1.0.1.5 (2025.9.10)
--------------------------------
- Support Serial Port speed up to 8M bps.

--------------------------------
# v1.0.1.4 (2025.5.17)
--------------------------------

--------------------------------
# v1.0.1.2 (2020.7.19)
--------------------------------
- Add Command Line option -noerrpause
  <br>"No Error Pause" option is added

- Add Serial Port ReadTimeOut/WriteTimeout Parameter
  <br>Add Serial Port ReadTimeOut/WriteTimeOut setting in Configuration

- Uefi Variable Dump
  <br>Add Hex view title to link to the variable name

- Acpi Table Dump
  <br>Add hex data dump

--------------------------------
# v1.0.1.1 (2020.6.26)
--------------------------------
- Add UEFI Variable Dump
   <br>Add Read UEFI Variable UI
   <br>**Need Administrator right!!!**

--------------------------------
# v1.0.1.0 (2020.5.14)
--------------------------------
- Remove the app administrator right requirment
- SUT Control improvement
  - 'Config' screen includes complete SUT control button definition and actions.
  - Invalid web request error display. 
- Console Window (VT100/ANSI)
  - Add Menu in FormConsole - 'Save ScreenAs'
  - Backspace key bug fixed
  - char background/foreground color bug fixed

--------------------------------
# v1.0.0.42
--------------------------------
 - DiskInfo
   -Show MBR information - bootable/nonbootable.
   -Show OS name in OsType field.

 - Add Command Line Mode
   - Arguments
     <br>-cli                   Command Line Mode
	   <br>-com [COM Settings]    COM port settings
	   <br>-file [FileName]       Logs will be save to this file
	   <br>-fchk [FileName]       The existence of this file will terminate the log capture  
	   <br>**Example:**
	          <br>plc -cli -com COM4:115200:None:8:ONE:None -file d:\mylog.txt -fchk stop.txt

  - Add SUT Control 
    <br>Add **"Sut Control"** field in Main Window.
    <br>The action string can be either web URL or executable file. Set the action string in "Option" window.
    <br>Below are the samples of the action string:
      <br>http://yourhost-ip/gpio/on/
      <br>d:\sut\AcPowerOn.bat      
      <br>d:\sut\PressPowerButton.exe

 - Console Window
   <br>Add "Backspace" key process.
