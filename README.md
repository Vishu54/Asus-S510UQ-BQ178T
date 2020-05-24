# Asus-S510UQ-BQ178T
This port is for Asus VivoBook S150UQ-BQ178T 

This build running on MacOS 12.14.5 (Mojave)

# Updated Detail

   Support Catalina version. 
   -Fixed Touchpad (VoodooIC2)
   -Fixed Stuck at afps when booting (Asus EC ddst)
   -Fixed Sound (Use MacBook 14,2) 
 Post installation tools can be found on tctien342 repo: https://github.com/tctien342/Asus-Vivobook-S510UA-Hackintosh

    Version:    10
    Support:    310
    Changelogs:
        - Updated to BIOS 310

# Specification

    1.Name:           Asus Vivobook S510UQ BQ178T
    2.CPU:            Intel Core i5-7200U
    3.Graphic:        Intel UHD620
    4.Wifi:           NOT WORKING, NEED TO REPLACED WITH DW1560
    5.Card Reader:    Realtek_CardReader(RTL8411B_RTS5226_RTS5227)
    6.Camera:         ASUS UVC HD
    7.Audio:          Conexant Audio CX8050
    8.Touchpad:       ELAN1300
    9.Bios Version:   310

# Thing that not able to use

    1. Nvidia DGPU 940MX
    2. Fingerprint
    3. FN + media controller's key

# Log 
    1. Added DDST-Disable-DGPU.aml 
    2. Added SSDT-PowerManagement.aml
    3. Boot will be slower compared to last update
    (Remove SSDT-Disable-DGPU.aml will boot faster)
