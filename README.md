# RMX3706_CN_ROM
- Offical ROM  官方固件   OTA
- RMX3706      
- Realme GT NEO5 150W CN
- 真我 GT Neo5 150W
- GT Neo5 150W
- https://www.realme.com/realme-gt-neo-5

<br>
<br>


# Search OTA download link by yourself
#### Use this

https://github.com/R0rt1z2/realme-ota

#### Query command

`realme-ota -r 1 RMX3706 RMX3706_11.A.00_0000_000000000000 4 10010111`

#### For more info

- https://forum.xda-developers.com/t/global-eu-collection-of-firmware-files.4478153
- https://www.facebook.com/groups/1497997480377295/permalink/2372650139578687
- https://www.facebook.com/groups/1497997480377295/permalink/2439168646260169

<br>
<br>

# Check version
Open the zip you will see `payload_properties.txt`
```
FILE_HASH=LBZPxL4vb3PBtUzqbkPrxKNh+rq9InyxkIKFB24vO4Y=
FILE_SIZE=7378166928
METADATA_HASH=MII7YsvkoNlWI7qALSvoNSRIGWL9zJW8i79kPS9Yq8o=
METADATA_SIZE=273645
ota_target_version=RMX3706_11.A.36_0360_202305152136
security_patch_vendor=2023-05-05
oplus_rom_version=V13.1.0
security_patch=2023-05-05
oplus_update_engine_verify_disable=0
oplus_separate_soft=22624
```
RMX3706_11.A.36_0360_202305152136 == RMX3706_13.1.0.106(CN01)

<br>
<br>

# Extract images from OTA zip files
#### Download and unzip

https://github.com/ssut/payload-dumper-go

#### Command

`.\payload-dumper-go.exe path_to_your_zip`

#### Example

After completion you can find various images in `extracted_date_time`

##### Show list of partitions in payload.bin

 `.\payload-dumper-go.exe -l .\b979db22cbf74dce83e7e0441bb1a29d.zip`

##### Extra all

`.\payload-dumper-go.exe .\514f4cc67a1941a3a823aa90a641d177.zip`

##### Extra bootloader only

`.\payload-dumper-go.exe -p boot .\514f4cc67a1941a3a823aa90a641d177.zip`

<br>
<br>


# Flash bootloader
- Unlock bootloder lock, by using this offical app: https://www.realmebbs.com/post-details/1626138770372190208
- Turn off the phone, press `volume down` + `power button` get in to fastboot
- Connect your phone and computer using USB
- Install Google USB Driver https://developer.android.com/studio/run/win-usb (Chinese Guide: https://zhuanlan.zhihu.com/p/366904302)
- Download https://developer.android.com/tools/releases/platform-tools
- Unzip and open powershell in platform-tools dir
- Optional, test if the bootloder works  `.\fastboot.exe boot .\boot.img`
- Flash bootloder`.\fastboot.exe flash boot .\boot.img`
- Reboot device `.\fastboot.exe reboot`

#### How to Root
Just install magisk app, select `patch a file`, select the `boot.img` you extracted from the OTA ROM package. Of course, it must match your system version.
and flash patched bootloader `magisk_patched_boot.img`.

##### Root failed? 

Flash the the original `boot.img`.

<br>
<br>


# OTA collection


#### RMX3706_13.1.0.116(CN01)
GT NEO5 RMX3706 China Full OTA A.46

"md5": "aa4d5bf825b9de94ff379362e854da4b"

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-71ae671b3f99b7f84cfa0c7656c68830/component-ota/23/09/20/b5708664e4b94f82bef7737037a09a25.zip

<br>





#### RMX3706_13.1.0.115(CN01)
GT NEO5 RMX3706 China Full OTA A.45

"md5": "b904eee2d3ecb9e8b735f692c064040c"

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-df6a0b9b22ae06b9f45091b92ea8a45c/component-ota/23/08/17/1067d355b9874ed1b55b24dd59da83a3.zip

<br>



#### RMX3706_13.1.0.114(CN01)
GT NEO5 RMX3706 China Full OTA A.44

"md5": "de5b0a181839ba59d328c0d86e30430d"

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-d41a7ac050c5dc31e449c35a63ad6de5/component-ota/23/08/04/5183494c27674cebac324328b389f369.zip

<br>



#### RMX3706_13.1.0.113(CN01)
GT NEO5 RMX3706 China Full OTA A.43

"md5": "f539faab627248d8715253a9387dce97"

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-dff6782d2a8b22eae1c974ada4ec1f79/component-ota/23/07/11/b0969f1b1f2b44edb28cf31f8fd310e7.zip

<br>


#### RMX3706_13.1.0.112(CN01)
GT NEO5 RMX3706 China Full OTA A.42

"md5": "ceb08951636245973ae24f8603ee881f"

https://gauss-compotacostauto-cn.allawnfs.com/remove-c84e764c61c9993bbd0af7bdd0cb74cd/component-ota/23/06/27/b979db22cbf74dce83e7e0441bb1a29d.zip

<br>


#### RMX3706_13.1.0.106(CN01)
GT NEO5 RMX3706 China Full OTA A.36

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-7ddc446895f1f09b7a93f160bf8e0245/component-ota/23/05/18/514f4cc67a1941a3a823aa90a641d177.zip?fbclid=IwAR0Xm_YsHRshV8HUXAk4PMYSgd9PJIY3VsXaYvlg8f2mdmBFpEsr8usTriM

<br>


#### RMX3706_13.1.0.105(CN01)
GT NEO5 RMX3706 China Full OTA A.35

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-9f9a6359d687f81eacc10d2b17b77724/component-ota/23/05/05/070dca35a73f4183a4bb4f584f8e6027.zip?fbclid=IwAR074F5UN6C2O6pZahFD0LGAjvfosfwAjv50IcYOSEKD2lXkmP-ZDQtr6KU

<br>


#### RMX3706_13.1.0.104(CN01)
GT NEO5 RMX3706 China Full OTA A.34

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-69c2bb320aaeda56af51dfbf1f97fcaa/component-ota/23/04/27/8388a5bb4ae74c43b6752186304bc77e.zip?fbclid=IwAR03maoyc1URsqJCEO6SI82yFK-CMigEmvaTtTesXQbB7LYQMOFEohLhw_4

<br>


#### UNKONW
GT NEO5 RMX3706 China Full OTA A.25

https://gauss-compotacostauto-cn.allawnfs.com/remove-bf85f6c43fbd3773dba1fbe18fde02d4/component-ota/23/03/24/77c363c10d6e4ebb81cbbc4484235b29.zip?fbclid=IwAR1uQh5N2jGmiLW-ThnNSr4ZxLq1Q4XK_GVkIoKYVPcRbfmR44UhKY9A84A

<br>


#### UNKONW
GT NEO5 RMX3706 China Full OTA A.24

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-334eb367a908bdd5f9638c86e0f0f992/component-ota/23/03/17/c6fccd130bd548a98bb4b8e032400616.zip?fbclid=IwAR10mpSsFoC4Y3ewxujhOml1ek0mOqnnKNOtwrLA4dtD5S4a-zUYAD4dERo

<br>




<br>
<br>
<br>
<br>


#真我 GT Neo5 固件 
#真我 GT Neo5 官方固件 
#真我 GT Neo5 ROM 
#Realme GT Neo5 固件 
#Realme GT Neo
#Realme Neo5 固件 
#Realme Neo5 ROM
#GT Neo5 固件
#GT Neo5 ROM
#Neo5 固件
#Neo5 ROM

