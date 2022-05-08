##Linux-zen-surface custom kernel scripts##
Initramfs modesettings in zen kernel modesettings
#(Kernel Driver=icl_uncore)
#modeset=i915 (Kernel Driver=i915)
#modeset=xhci_pci (Kernel driver=xhci_hcd)
#modeset=intel_ish_ipc (Kernel driver=intel_ish_ipc)
#modeset=xhci_pci (Kernel driver=xhci_hcd)
#modeset=iwlwifi (Kernel driver=iwlwifi)
#modeset=intel_lpss_pci (Kernel driver=intel-lpss)
#modeset=mei_me
#Kernel driver=pcieport
#modeset=snd_hda_intel,modeset=snd_sof_intel_icl (Kernel driver=snd_hda_intel)
#modeset=intel_spi_pci (Kernel driver=intel-spi)
#modeset=nvme (Kernel driver=nvme)
#modeset=nouveau,nvidia_drm,nvidia (Kernel driver=nvidia)

##Device ID's by initramfs##
1. pci_0000_00_00_0:Intel Corporation Ice Lake-LP Processor Host Bridge/DRAM Registers (REV 03)
2. pci_0000_00_02_0:Intel Corporation Iris Plus Graphics G7 (REV 07)
3. pci_0000_00_05_0:Intel Corporation Image Signal Processor (REV 03)
4. pci_0000_0d_00_0:Intel Corporation Ice Lake Thunderbolt 3 USB Controller (REV 30)
5. pci_0000_12_00_0: Intel Corporation Ice Lake-LP Integrated Sensor Solution (REV30)
6. pci_0000_14_00_0:Intel Corporation Ice Lake-LP USB 3.1 xHCI Host Controller (REV 30)
7. pci_0000_14_00_2:Intel Corporation Ice Lake-LP DRAM Controller (REV 30)
8. pci_0000_14_00_3:Intel Corporation Ice Lake-LP PCH CNVi WiFi (REV 30)
9. pci_0000_15_00_0:Intel Corproration Ice Lake-LP Serial IO I2C Controller #0 (REV 30)
10. pci_0000_15_00_2: Intel Corporation Ice Lake-LP Serial IO I2C Controller #2 (REV 30)
11. pci_0000_15_00_3: Intel Corporation Ice Lake-LP Serial IO I2C Controller #3 (REV 30)
12. pci_0000_16_00_0: Intel Corporation Ice Lake-LP Management Engine (REV 30)
13. pci_0000_16_00_4: Intel Corporation Device 34e4 (REV 30)
14. pci_0000_19_00_0: Intel Corporation Ice Lake-LP Serial IO I2C Controller #4 (REV 30)
15. pci_0000_1d_00_0: Intel Corporation Ice-Lake-LP PCI Express Root Port #9 (REV 30)
16. pci_0000_1d_00_4: Intel Corporation Device 34b4 (REV 30)
17. pci_0000_1e_00_0: Intel Corporation Ice Lake-LP Serial IO UART Controller #0 (REV30)
18. pci_0000_1f_00_0: Intel Corporation Ice Lake-LP LPC Controller (REV 30)
19. pci_0000_1f_00_3: Intel Corporation Ice Lake-LP Smart Sound Technology Audio Controller (REV 30)
20. pci_0000_1f_00_5: Intel Corporation Ice Lake-LP SPI Controller (REV 30)
21. pci_0000_01_00_0: KIOXIA Corporation Device 0001
22. pci_0000_02_00_0: NVIDIA Corporation TU117M (GeForce GTX 1650 Mobile/Max-Q REV a1)

##Device ID by IOMMU Groupings
0. [0600] Host Bridge: Intel Corporation Ice Lake-LP Processor Host Bridge/DRAM Registers [8086:8a12] (rev 03)
1. [0300] VGA Compatibile Controller: Intel Corporation Iris Plus Graphics G7 [8086:8a52] (rev 07)
2. [0480] Multimedia Controller: Intel Corporation Image Signal Processor [8096:8a19] (rev 03)
3. [0c03] USB Controller: Intel Corporation Ice Lake Thunderbolt 3 USB Controller [8096:8a13] (rev 03)
4. [0700] Serial Controller: Intel Corporation Ice Lake-LP Integrated Sensor Solution [8086:34fc] (rev 30)
5. [0c03] USB Controller: Intel Corporation Ice Lake-LP USB 3.1 xHCI Host Controller [8086:34ed] (rev 40)
6. [0500] RAM Memory: Intel Corporation Ice Lake-LP DRAM Controller [8086:34ef] (rev 30)
7. [0280] Network Controller: Intel Corporation Ice Lake-LP PCH CNVi WiFi [8086:34f0] (rev 30)
8. [0c80]Serial Bus Controller as Serial bus controller #0: Intel Corporation Ice Lake-LP Serial IO I2C Controller #0 (rev 30)
9. [0c80]Serial Bus Controller as Serial bus controller #2: Intel Corproration Ice Lake-LP Serial IO I2C Controller #2 (rev 30)
10. [0c80]Serial Bus Controller as Communication Controller Host Bridge: Intel Corporation Ice Lake-LP Serial IO I2C Controller #3
11. [0c80]Serial Bus Controller as Serial Bus Controller Host:Intel Corporation Ice Lake-LP Serial IO I2C Controller #4 [8086:34c5] (rev30)
12. [0604]PCI bridge: Intel Corporation Ice Lake-LP PCI Express Root Port #9 [8086:34b0] (rev 30)
13. [0604]PCI Bridge: Intel Corporation Device [8086:7270] (rev 30)
14. [0780]Communication Controller: Intel Corporation Ice Lake-LP Serial IO UART Controller #0 [8086:34a8] (rev 30)
15. [0601]ISA bridge: Intel Corporation Ice Lake-LP LPC Controller [8086:3482] (rev 30)
16. [0403]Audio device: Intel Corporation Ice Lake-LP LPC Smart Sound Technology Audio Controller [8086:34c8] (rev 30)
17. [0c80]Serial Bus Controller: Intel Corporation Ice Lake-LP SPI Controller [8086:34a4] (rev 30)
18. [0180]Non-Volatile memory controller: KIOXIA Corporation Device [1e0f:0001] 
19. [0302]3D Controller: NVIDIA TU117M GeForce GTX 1650 Mobile/Max-Q [10de:1f91] (rev a1)

##by lscpi -nnk for kernel modesetting
1. driver: icl_uncore 8086:8a12 (rev 03),7270 [Modesettings: ??]
2. driver: i915 8086:8a52 (rev 07), 1414:0043 (Microrsoft Corporation Device) [Modesettings: i915]
3. driver: xhci_hcd 8086:8a13 rev 03, 8086:34ed rev 30 [Modesettings: xhci_pci]
4. driver: intel_ish_ipc: 8086:34fc rev 30 [Modesettings: intel_ish_ipc]
5. driver: iwlwifi: 8086:34f0 rev 30 [Modesettings: iwlwifi]
6. driver: intel-lpss: 8086:7270,4e8,34ea,34eb,34c5 [Modesettings: intel_lpss_pci]
7. driver: pcieport: 8086:7270,34b0,34a8 [Modesettings: ?]
8. driver: intel_lpss: 7270,8086:34a8 [Modesettings: intel_lpss_pci]
10. driver:snd_hda_intel: 8086:7270, 34c8 [Modesettings: with snd_sof_pci_intel_icl
11. driver: intel-spi: 8086:7270, 34a4,0c80 [Modesettings: intel_spi_pci]
12. driver: nvme: 1e0f:0001. 0108 [Modesettings: nvme]
13. driver: nvidia 10de:1f91, 0302, 0032 [Modesettings: nouveau,nvidia_drm,nvidia]
14. [Modesettings:mei_me]
