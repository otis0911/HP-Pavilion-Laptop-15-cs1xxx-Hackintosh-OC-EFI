# HP-Pavilion-Laptop-15-cs1xxx-Hackintosh-OC-EFI

## Test Platfrom Information/測試平台資訊

HP Pavilion Laptop 15-cs1064tx (CFG Unlocked)

CPU: Intel Core i5 8265U

GPU: Nvidia Geforce MX130 (disabled)

RAM: 4+8GB

Store: 128GB M.2 SATA SSD + 1TB SATA HDD

## Using SSDTs

[SSDT-USBX.aml/SSDT-EC.aml](https://dortania.github.io/Getting-Started-With-ACPI/Universal/ec-fix.html)

[SSDT-RTCAWAC.aml](https://dortania.github.io/Getting-Started-With-ACPI/Universal/awac.html)

[SSDT-PNLF.aml](https://dortania.github.io/Getting-Started-With-ACPI/Laptops/backlight.html)

[SSDT-HP-FixLidSleep.aml](https://dortania.github.io/OpenCore-Post-Install/universal/sleep.html#displays)

## Using Kexts

[Lilu.kext](https://github.com/acidanthera/Lilu)

[VirtualSMC.kext](https://github.com/acidanthera/VirtualSMC)

[WhateverGreen.kext](https://github.com/acidanthera/WhateverGreen)

[AppleALC.kext](https://github.com/acidanthera/AppleALC)

[VoodooPS2Controller.kext]()

[AppleItlwm.kext(normaly, it's disable)]()

[itlwm.kext]()

[IntelBluetoothFirmware.kext]()

[IntelBTPatcher.kext]()

[BlueToolFixup.kext]()

[RealtekRTL8111.kext]()

[CtlnaAHCIPort.kext]()

[SMCBatteryManager.kext]()

[SMCProcessor.kext]()

[SMCSuperIO.kext]()

[ECEnabler.kext]()

[DebugEnhancer.kext]()

## en-US

This is an OpenCore Hackintosh EFI for HP Pavilion Laptop 15-cs1xxx series.

## zh-TW

這是一個基於OpenCore的黑蘋果EFI，適用於HP Pavilion Laptop 15-cs1xxx系列。

### 如何使用？

很簡單，去看[Dortania的OpenCore安裝指南](https://dortania.github.io/OpenCore-Install-Guide/)，按照指南裡面的內容進行配置

然後 **很重要！這個EFI的SMBIOS資訊都是空的！請自行生成！**

### 注意事項

1.這個EFI的SMBIOS是空的，序號、ROM那些的都請自行生成

2.Config.plist裡面有設定AppleXcpmCfgLock為true，也就是理論上這個EFI不需要解鎖CFG就可以使用，但我仍然建議你把電腦的CFG鎖解掉，這可以避免很多麻煩。

3.所有的SSDT都是用我的電腦的配置去生成、編寫的，可能在不同電腦上會造成問題，如果發生問題，請從[Dortania的ACPI指南](https://dortania.github.io/Getting-Started-With-ACPI/)自行下載或生成以下
***
**請注意！這還只是alpha版本，這個版本仍然由許多問題！**
***
### 目前已知問題：

1.睡眠不正常，由S3喚醒至S0時會報錯Sleep Wake failure in EFI。

2.藍芽不可用，無法正常識別Intel Wireless-AC 9461的藍牙晶片。

3.鍵盤上的亮度調整鍵(F2/F3)不可用，這部分可以安裝MonitorControl來解決
