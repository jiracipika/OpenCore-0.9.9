# OpenCore-1.0.0
OpenCore with MacOS Ventura 13.6.6 (+Dualboot Windows 10)
Followed these guides: 
https://dortania.github.io/getting-started/
https://github.com/USBToolBox/tool

Specs:
CPU: Intel i9 9900k (Overclocked to 4.7GHZ)
Motherboard: MSI Z 370 A-PRO
Memory: Adata XPG Z1 DDR4 @2666mhz 8gbx2
Storage: 
1x 500gb NVME via PCi-E adapter (only 1 NVME slot on MOBO)
3x500gb (Windows)
Networking:
Broadcom BRCM20702 off-brand Ebay (worked OOB)
![Screenshot 2024-05-12 at 11 12 41 PM](https://github.com/jiracipika/OpenCore-1.0.0/assets/74633726/0a099599-1f99-4544-a37c-54e4bc1f8fff)

Input Devices: 
-Apple Magic Trackpad 2
-Gaming Keyboard
-Redragon M801 Sniper Pro

Display (via Displayport on RX 5600xt)
-Dell 27inch 1080p@280hz

What's working:
-Everything! will upload GeekBench+Metal soon
-Wifi (worked OOB with WIFI BT card)
-Ethernet
-Bluetooth (worked OOB with WIFI BT card)
-All USB ports mapped with USBTOOLBOX (literally amazing)
(Note: all USB ports were functional at USB 2.0, only 4/5 USB 3.0 were functional prior to mapping) 

What's not working:
FIXED: Hardware acceleration
MSI Z370 Motherboard settings under "Settings\Advanced\Integrated Graphics Configuration"
\\
Initiate Graphics Adapter [PEG]
Integrated Graphics Share Memory [64M]
IGD Multi-Monitor [Enabled]
\\

FIXED: Random kernel panics/lockups due to ram, overclocks brought down back to stock 3200mhz -> 2666mhz. (Was previously causing issues with Geekbench completing benchmark)

My use case:
Primarily using VS Code, Logic Pro X (for those hard renders)
Windows for gaming, M1 MBA for on-the-go

Benchmark Results:
Geekbench 6.3.0 for macOS AVX2
CPU: 
Single-Core: 1634
Multi-Core: 7866

GPU (Metal): 82561 (custom flashed bios from mining, doesn't affect anything but timings=performance)

Note: Find and replace these values in config.plist:
REPLACE_ME_PLEASE

Thank you to:

@dortania for Opencore
https://github.com/dortania

@corpnewt for ProperTree, GenSMBIOS
https://github.com/corpnewt/

@dhinakg for USBToolBox
https://github.com/dhinakg
