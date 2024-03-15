# EFI-X99-MACHINIST-RS9-RX6600M

```bash
Plataform: Desktop | Intel Xeon
Motherboard: MACHINIST X99-RS9
CPU: Intel Xeon E5-2670 v3, 2300 MHz (12C/24T)
GPU: Radeon RX6600M (8 GB)
Memory: 16GB RAM
Audio: Realtek ALC897
SMBIOS: iMacPro1,1
macOS: Sonoma 14.4
Opencore: 0.9.9
```

# BIOS Settings

### Disable

- Fast Boot
- Secure Boot
- Serial/COM Port
- Parallel Port
- VT-d (can be enabled if you set `DisableIoMapper` to YES)
- Compatibility Support Module (CSM).
- Thunderbolt(For initial install, as Thunderbolt can cause issues if not setup correctly)
- Intel SGX
- Intel Platform Trust
- CFG Lock (MSR 0xE2 write protection)
  - This must be off, if you can't find the option then **`ENABLE`** `AppleXcpmCfgLock`. 
  - Your hack will not boot with CFG-Lock enabled.
  - For 10.10 and older, you'll need to **`ENABLE`** `AppleCpuPmCfgLock` as well.

### Enable

- VT-x
- Above 4G decoding. 
  - This must be on, if you can't find the option then add `npci=0x2000` to `boot-args`. 
  - Do not have both this option and `npci` on `boot-args` enabled at the same time.
- Hyper-Threading
- Execute Disable Bit
- EHCI/XHCI Hand-off
- OS type: Windows 8.1/10/11 UEFI Mode
- SATA Mode: AHCI

# References

https://github.com/luchina-gabriel/BASE-EFI-INTEL-HEDT-4THGEN-X99-HASWELL-E
<br>
https://dortania.github.io/OpenCore-Install-Guide/config-HEDT/haswell-e.html
<br>
https://dortania.github.io/Getting-Started-With-ACPI/
