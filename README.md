# EFI-X99-MACHINIST-RS9-RX6600M

```bash
Plataform: Desktop | Intel Xeon
Motherboard: MACHINIST X99-RS9
CPU: Intel Xeon E5-2670 v3, 2300 MHz (12C/24T)
GPU: Radeon RX6600M (8 GB)
Memory: 16GB RAM
Audio: Realtek ALC897
SMBIOS: MacPro7,1
macOS: Tahoe 26
Opencore: 1.0.5
```

# BIOS Settings

First of all, check if the BIOS date and time are correct.
Now just follow the steps below:

### Advanced

- NCT5532D SIO Configuration
  - Serial Port [Disabled]
    
- PCI Subsystem Settings
  - Above 4G Decoding [Disabled] & Re-size BAR Support [Disabled]
        
- CSM Configuration
  - CSM Support [Disabled]
  (PS: To do this, you first need to change the Video setting to UEFI (save and restart), return to the BIOS, and then you will be able to disable CSM Support.)
    
- USB Configuration
  - XHCI Hand-off [Enabled] & EHCI Hand-off [Enabled]  

### IntelRCSetup

- Processor Configuration
  - MSR Lock Control [Disabled]
 
### Security 

- Secure Boot menu
  - Secure Boot [Disabled]


# References

https://github.com/luchina-gabriel/BASE-EFI-INTEL-HEDT-4THGEN-X99-HASWELL-E
<br>
https://dortania.github.io/OpenCore-Install-Guide/config-HEDT/haswell-e.html
<br>
https://dortania.github.io/Getting-Started-With-ACPI/
