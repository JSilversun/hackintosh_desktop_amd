## Description
This is the EFI folder for my personal hackintosh, I uploaded here so it can be used as reference for other people with the same motherboard or other people who needs some examples. The biggest problem I had was mapping the USB ports because the internal ports in my motherboard didn't work, but I was able to map them successfully. PLEASE DO NOT COPY THIS EFI IF YOUR HARDWARE IS DIFFERENT.

## Steps
I followed [Open core desktop guide](https://dortania.github.io/OpenCore-Desktop-Guide/) in this flow:

1. [Introduction](https://dortania.github.io/OpenCore-Desktop-Guide/)
1. [Why OpenCore](https://dortania.github.io/OpenCore-Desktop-Guide/why-oc.html)
1. [macOS install](https://dortania.github.io/OpenCore-Desktop-Guide/installer-guide/mac-install.html)
1. [Gathering files](https://dortania.github.io/OpenCore-Desktop-Guide/ktext.html)
1. [Getting started with ACPI](https://dortania.github.io/OpenCore-Desktop-Guide/extras/acpi.html) (Didn't need any special SSDT, only the usual `SSDT-EC-USBX` so I read the ACPI section just to know a bit about the process, the required SSDT is mentioned in the nexts guides so this section is not entirely necessary for MY SYSTEM)
1. [Zen](https://dortania.github.io/OpenCore-Desktop-Guide/AMD/zen.html) (This is the longest one to follow but it's really detailed)
1. [USB Mapping](https://dortania.github.io/USB-Map-Guide/) (This is the one which will help you map your USB ports, needed to solve the bluetooth problem, this is the hardest part, it took me 2 entire days to get the ports working, hopefully I'll create an article about it)

Following this guide I was able to get my system working smoothly.

## What works
- [x] Wifi and Bluetooth
- [x] Microphone
- [x] All USB ports (Mapped manually all the ports in the PTHX controller)
- [x] Sleep/awake
- [x] Audio (Both native and with VoodooHDA, using VoodooHDA right now for )


## What doesn't work
- Docker doesn't work, for now the only way to use it is with docker toolbox (virtualbox)
- If I use VoodoooHDA, the microphone won't work

## Specs
- CPU: AMD Ryzen 5 2600
- RAM: Corsair Vengeance 32 GB 2666Mhz (8GB * 4)
- Motherboard: Gigabyte Aorus Ultra Gaming x470
- GPU: AMD Sapphire Rx 580
- PSU: Corsair TX750 750w
- Wifi/Bluetooth: Fenvi T919 NIC Wireless card BCM94360CD
- 1 SSD NVME for Windows (500gb)
- 1 SSD Sata 3 for Macos (256gb)

## Bootloader
- Opencore 0.5.9

## SMBIOS
iMacPro1,1

## OS
- Mojave 10.10.4
- Catalina 10.15.1

## TO DO
- [ ] Create a guide and attach info about how to map usb ports
- [ ] Install Catalina 10.15.5
- [ ] Implement GUI for Bootloader (Opencore)