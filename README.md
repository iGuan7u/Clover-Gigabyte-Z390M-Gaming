# CloverEFI
An Clover config of hackintosh, about Gigabyte Z390M Gaming.

## Computer Configuration
Component | Brank
-|-
CPU | Intel i7 9700K
MotherBoard | Gigabyte Z390M Gaming
Memory | Corsair 16G DDR4 3200
Graphic Card | Dataland RX580 2304sp 8G
SSD | Samsung 970evo 500G
Net Card | BCM94360CD（Including BlueTooth）
Power | EVGA 750P2
Fan | JONSBO TW3-240
Case | JONSBO C3-PLUS
Monitor | AOC U2790VQ 27” 4K
Keyboard & Mouse | Magic Keyboard 2 & Mouse 2

## BIOS Changes
Comes from [tonymacx86](https://www.tonymacx86.com/threads/success-jbarnettes-build-gigabyte-z390-m-gaming-i9-9900k-sapphire-rx-vega-64-8gb-32gb-ram-macos-10-14-3-w-usb3-working.273381/).

- Save & Exit
    - Load Optimized Defaults then make (or confirm) the following settings -- important settings in **bold**:
- M.I.T.
    - Extreme Memory Profile (X.M.P.) → **Profile 1**
- BIOS
    - Windows 8/10 Features → **Other OS**
    - CSM Support → **Enabled**
        - Secure Boot will be disabled by default, but good to check
- Peripherals
    - Initial Display Output → PCIe Slot 1. If your discrete graphics card is in Slot 2, change this appropriately.
    - Intel Platform Trust Technology (PTT) → Disabled
    - Thunderbolt(TM) Configuration
        - TBT Vt-d Base Security → **Disabled**
        - Thunderbolt Boot Support → **Disabled**
        - Security Level → **No Security**
    - USB Configuration
        - Legacy USB Support → Enabled
        - XHCI Hand-off → **Enabled**
    - Network Stack Configuration
        - Network Stack → **Disabled**
- Chipset
    - Vt-d → **Disabled**
    - Internal Graphics → **Enabled**
    - DVMT Pre-Alloc → 64M
    - DVMT Total Gfx Mem → 256M
    - Audio Controller → **Enabled**
    - Above 4G Decoding → **Enabled**
- Power
    - ErP → Disabled
    - RC6 (Render Standby) → Enabled

## Special Config
- I caculate my own slide number of OsxAptioFix2Drv-free2000.efi as the Boot Option, you should replace it with your own.
- USB3.0 is active by kexts/Other/USBPorts.kext. USBInjectALL.kext is unnecessary.

## What Is Not Working.
As far as I know, everything is working fine on it.

## Problems
- 1 time out of 10, booting fails in Clover with error `Couldn't allocate runtime area`. Reboot and try again and it works.
- After the first Apple logo showing at the launch, graphic card start may cause a splash, and then show the second Apple logo.
