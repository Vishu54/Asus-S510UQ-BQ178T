<p align="center">
<img src="https://i.imgur.com/piJu4XY.png")
    </p>

# Specification

<p align="center">
<img src="https://www.asus.com/media/global/products/zSh0eyO9fvBbAZHv/P_setting_fff_1_90_end_500.png")
    </p>

Device | Details | status | Comment
------------ | ------------- | ------------- | -------------
CPU | [**Intel Core i5-7200U**](https://ark.intel.com/content/www/us/en/ark/products/95443/intel-core-i5-7200u-processor-3m-cache-up-to-3-10-ghz.html) | Working | 
Graphic | Intel UHD620 | Working |
Card Reader | Realtek RTL8411B_RTS5226_RTS5227 | Working |
Camera | ASUS UVC HD | Working |
Audio | Conexant Audio CX8050 | Working |
Battery | B31N1637 42Wh | Working | 
Touchpad | ELAN1300 | Working |
Wifi | Intel Wireless-AC 8265 | Unsupported | Replaced with *BCM94352Z* 
Discrete Graphic | Nvidia GeForce 940MX | Unsupported | Disabled with *NoHybGfx*
Fingerprint | ELAN EFSA96SA-H700Z | Unsupported | Disabled with *NoTouchID kext*
Bios | [**310**](https://dlcdnets.asus.com/pub/ASUS/nb/X510UQ/X510UQAS310.zip) | Compatible | Disabled CFG
MacOS | [**11.0 (20A5364e)**](https://developer.apple.com/macos/) | Compatible | Tested on latest beta
OpenCore | [**0.6.1**](https://github.com/acidanthera/OpenCorePkg) | Compatible | Updated to 0.6.1


# Asus Other Models 

For stability, user are adviced to use **whatnameisit** EFI file. 

Hackintosh  | Details | Clover | OpenCore | Maintainer link
------------ | ------------- | ------------- | ------------- | ------------- 
S510UA/F510UA | ***With*** KB Light and dGPU version | Supported | - | [tctien342](https://github.com/tctien342/Asus-Vivobook-S510UA-Hackintosh)
X510UA-BQ490 | ***No*** KB light and ***No*** dGPU version | Supported | Supported | [whatnameisit](https://github.com/whatnameisit/Asus-Vivobook-X510UA-BQ490-Catalina-10.15.3-Hackintosh)

## Changelog

**Sept 13, 2020**
- Revert back to MacBook14,1 for several reasons: 
1. HDMI Output not working, but works on 14,1 config
2. Battery performance weak compared to MacBookPro15,1 config
3. CPU Temperature always higher than MacBook14,1 config
- All the necessary SSDT patches merged into SSDT-macos.aml such as:
1. Battery BIX+FBST patch
2. Disable dGPU patch
3. MEM2 patch
4. FAN MOD patch
    
    
**Sept 11, 2020**
- Added back NoHybGfx (Accidentally left behind) 
- Clean Up X510UQ SSDT patch 
- Updated Config 
    
**Sept 10, 2020**
- Updated to latest OC and Kexts. 
- Removed Two EFI folder from git 
- Minimised ACPI patch
- Changed System Product name to MacBookPro15,1
- Revert changes that causes kernel panic when rebuild kext cache.

# CFG Lock Offset
CFG MUST BE Unlock to avoid **[EB|#LOG:EXITBS:START]** Issue in OpenCore, Of course you can ignore CFG lock but there's a chance to causes kernel panic when update OS. Make sure you enable AppleCpuPmCfgLock and AppleXcpmCfgLock in config before boot up the OC. 

Asus S510UQ bios version 310 CFG Lock offset is **0x527**, [Follow Dortania guide for unlock CFG](https://dortania.github.io/OpenCore-Install-Guide/extras/msr-lock.html)
    
# Useful tools  
[Open Core Configurator](https://mackie100projects.altervista.org/download-opencore-configurator/)

[Hackintool](https://github.com/headkaze/Hackintool)

[MaciASL](https://github.com/acidanthera/MaciASL) 

[IORegistryExplorer](https://github.com/vulgo/IORegistryExplorer) 


# Credits 
[Thanks to whatnameisit for Asus X510UA hackintosh port](https://github.com/whatnameisit/Asus-Vivobook-X510UA-BQ490-Catalina-10.15.3-Hackintosh), My OC Port is based on whatnameisit EFI.

[Thanks to Dortania for OpenCore Resources and guide](https://github.com/dortania)

[Thanks to acidanthera for OpenCorePkg](https://github.com/acidanthera/OpenCorePkg)



