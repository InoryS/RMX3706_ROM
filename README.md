# RMX3706_CN_ROM
- Offical ROM  官方固件   OTA
- RMX3706      
- Realme GT NEO5 150W CN
- 真我 GT Neo5 150W
- GT Neo5 150W
- China mainland version
- https://www.realme.com/realme-gt-neo-5

<br>
<br>


# Search OTA download link by yourself
#### Use this

https://github.com/R0rt1z2/realme-ota

#### Query command

Realme UI 4 `realme-ota -r 1 RMX3706 RMX3706_11.A.00_0000_000000000000 4 0`

Realme UI 5 `realme-ota -r 1 RMX3706 RMX3706_11.C.00_0000_000000000000 5 0`

Realme UI 6 `realme-ota -r 1 RMX3706 RMX3706_11.F.00_0000_000000000000 6 0`

```
positional arguments:
  product_model         Product Model (ro.product.name).
  ota_version           OTA Version (ro.build.version.ota).
  {1,2,3,4,5,6}         RealmeUI Version (ro.build.version.realmeui).
  nv_identifier         NV (carrier) identifier (ro.build.oplus_nv_id) (ifnone, provide 0 or omit).
```

Execute `getprop <prop>` in the mobile terminal to get the corresponding information

Such as `getprop ro.build.version.ota`



#### For more info

- https://forum.xda-developers.com/t/global-eu-collection-of-firmware-files.4478153
- https://www.facebook.com/groups/1497997480377295/permalink/2616632928513739

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
- Connect your phone and computer using USB in fastboot mode
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

**If you got 403**

  - Try replacing the beginning of the url with `https://gauss-compotacostauto-cn.allawnfs.com` or `https://gauss-otacostmanual-cn.allawnfs.com`
  - Try use `wget` to download
  - Try download on your phone

<br>
<br>
<br>
<br>



#### RMX3706_15.0.0.440(CN01)
GT NEO5 RMX3706 China Full OTA F.17

Realme UI 6， Andriod 15

"md5": "b57512da7ef1089861ffafb37e4bc0ec",

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-ef03f3149ad0ba470da7a63837a11049/component-ota/25/02/22/ebe6fbf3b699458d994dadc759f11dbc.zip

<br>




#### RMX3706_15.0.0.430(CN01)
GT NEO5 RMX3706 China Full OTA F.16

Realme UI 6， Andriod 15

"md5": "a44d2187f0beb2411e95c7df76e81bb8",

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-f2d3ec4ab9070574a866e13738b07df0/component-ota/25/01/22/495a04ff65084aa7bde013ca02f973d8.zip

<br>



#### RMX3706_15.0.0.320(CN01)
GT NEO5 RMX3706 China Full OTA F.09

**Realme UI 6， Andriod 15**

"md5": "46cf54308dc13ef82f10c04c1df62bde",

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-d49b6040676ee68834d326cb2510a5db/component-ota/24/12/16/4c9b6ca7b32a4db896c0b4586368b540.zip

<br>



#### RMX3706_14.0.0.903(CN01)
GT NEO5 RMX3706 China Full OTA C.41

Realme UI 5， Andriod 14

"md5": "de985d14e23e536409389f02bc920b24",

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-d26869f1a3a309e9678b19ffe7ed4d38/component-ota/24/09/25/cec0b7c349f0401495ba9101e8690d06.zip

<br>

#### RMX3706_14.0.0.901(CN01)
GT NEO5 RMX3706 China Full OTA C.39

Realme UI 5， Andriod 14

"md5": "44d14ed93e57beb88d2390f32fee34d7",

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-c81e15b2714b9eaa06d68f1b94b6761b/component-ota/24/08/30/daab7edcd3df4bcbb3ae288fca3496e5.zip

<br>



#### RMX3706_14.0.0.900(CN01)
GT NEO5 RMX3706 China Full OTA C.38

Realme UI 5， Andriod 14

"md5": "fb895096e5cefa5687b2bd5a75d1425b",

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-7975476401d481149ae66a6c5ee1e2a0/component-ota/24/08/16/a549203fc660495a92537f06555fc982.zip

<br>


#### RMX3706_14.0.0.801(CN01)
GT NEO5 RMX3706 China Full OTA C.35

This version adds the device name censor.

At least we appreciate that it dares to write this, other manufacturers don't even dare to write it in the update log...

Realme UI 5， Andriod 14

"md5": "d6dd4e6167401303bb66d60b956046a5",

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-4e85f6f99ab2ea15b050ca4afcf0cc3c/component-ota/24/06/20/c728b060454c4d74b1f5f90c38b4e37a.zip

<br>





#### RMX3706_14.0.0.800(CN01)
GT NEO5 RMX3706 China Full OTA C.34

Realme UI 5， Andriod 14

"md5": "10f58615848c548e3e7ee4ee460f9f39",

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-fe87552a1a9f74397f7a7056704c6801/component-ota/24/06/06/b61491a0f9f44387958858a213f8f9ab.zip

<br>




#### RMX3706_14.0.0.601(CN01)
GT NEO5 RMX3706 China Full OTA C.32

Realme UI 5， Andriod 14

"md5": "b9a0c7ca24161755437b374f83aec246",

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-90457138d710a585b3bc7ec4b8e6a30c/component-ota/24/04/11/125a48e052f047f6b651db2223a67874.zip

<br>





#### RMX3706_14.0.0.411(CN01)
GT NEO5 RMX3706 China Full OTA C.30

Realme UI 5， Andriod 14

"md5": "0159c03b64534b4497f623b3f7a2c528",

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-c71351fcac7229e4413d997f3a51ab54/component-ota/24/03/12/19aa7fda942c43debf77594fd4c93164.zip

<br>






#### RMX3706_14.0.0.213(CN01)
GT NEO5 RMX3706 China Full OTA C.26

Realme UI 5， Andriod 14

"md5": "2A7FE33351D64A2E98673C6308818D89",

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-74653b15008d4a6e9ab25d0b9f2316b8/component-ota/24/01/31/d36129819eb14b63bf7a98ce8c479a74.zip

<br>




#### RMX3706_14.0.0.100(CN01)
GT NEO5 RMX3706 China Full OTA C.22

Realme UI 5， Andriod 14

"md5": "0f86c33a8bc465aaa6187de4abd6ea22",

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-cf397b85b5b35acaaf3a4bc34bd5dbe1/component-ota/23/12/07/9a762b4845d4443f9dd124afeefb6ebf.zip

<br>



#### RMX3706_13.1.0.118(SP01CN01)
GT NEO5 RMX3706 China Full OTA A.48

Realme UI 4， Andriod 13

"md5": "e027328b9c1f81382ec4d48b9e802914",

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-756c6b7d0b3eafb85e471fa0e1fc4ddc/component-ota/23/11/22/a0804b7122024c1cb271d50ad9d7b6fd.zip

<br>




#### RMX3706_13.1.0.117(CN01)
GT NEO5 RMX3706 China Full OTA A.47

Realme UI 4， Andriod 13

"md5": "d53fa3998d1db06b4031f93d5654fe0e",

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-8de444c66a7a78f85dda9cfbc4422464/component-ota/23/09/26/14d91e8fd66749588e8cdde57def0001.zip

<br>






#### RMX3706_13.1.0.116(CN01)
GT NEO5 RMX3706 China Full OTA A.46

Realme UI 4， Andriod 13

"md5": "aa4d5bf825b9de94ff379362e854da4b"

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-71ae671b3f99b7f84cfa0c7656c68830/component-ota/23/09/20/b5708664e4b94f82bef7737037a09a25.zip

<br>





#### RMX3706_13.1.0.115(CN01)
GT NEO5 RMX3706 China Full OTA A.45

Realme UI 4， Andriod 13

"md5": "b904eee2d3ecb9e8b735f692c064040c"

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-df6a0b9b22ae06b9f45091b92ea8a45c/component-ota/23/08/17/1067d355b9874ed1b55b24dd59da83a3.zip

<br>



#### RMX3706_13.1.0.114(CN01)
GT NEO5 RMX3706 China Full OTA A.44

Realme UI 4， Andriod 13

"md5": "de5b0a181839ba59d328c0d86e30430d"

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-d41a7ac050c5dc31e449c35a63ad6de5/component-ota/23/08/04/5183494c27674cebac324328b389f369.zip

<br>



#### RMX3706_13.1.0.113(CN01)
GT NEO5 RMX3706 China Full OTA A.43

Realme UI 4， Andriod 13

"md5": "f539faab627248d8715253a9387dce97"

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-dff6782d2a8b22eae1c974ada4ec1f79/component-ota/23/07/11/b0969f1b1f2b44edb28cf31f8fd310e7.zip

<br>


#### RMX3706_13.1.0.112(CN01)
GT NEO5 RMX3706 China Full OTA A.42

Realme UI 4， Andriod 13

"md5": "ceb08951636245973ae24f8603ee881f"

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-c84e764c61c9993bbd0af7bdd0cb74cd/component-ota/23/06/27/b979db22cbf74dce83e7e0441bb1a29d.zip

<br>


#### RMX3706_13.1.0.106(CN01)
GT NEO5 RMX3706 China Full OTA A.36

Realme UI 4， Andriod 13

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-7ddc446895f1f09b7a93f160bf8e0245/component-ota/23/05/18/514f4cc67a1941a3a823aa90a641d177.zip

<br>


#### RMX3706_13.1.0.105(CN01)
GT NEO5 RMX3706 China Full OTA A.35

Realme UI 4， Andriod 13

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-9f9a6359d687f81eacc10d2b17b77724/component-ota/23/05/05/070dca35a73f4183a4bb4f584f8e6027.zip

<br>


#### RMX3706_13.1.0.104(CN01)
GT NEO5 RMX3706 China Full OTA A.34

Realme UI 4， Andriod 13

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-69c2bb320aaeda56af51dfbf1f97fcaa/component-ota/23/04/27/8388a5bb4ae74c43b6752186304bc77e.zip

<br>


#### UNKONW
GT NEO5 RMX3706 China Full OTA A.25

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-bf85f6c43fbd3773dba1fbe18fde02d4/component-ota/23/03/24/77c363c10d6e4ebb81cbbc4484235b29.zip

<br>


#### UNKONW
GT NEO5 RMX3706 China Full OTA A.24

https://gauss-componentotacostmanual-cn.allawnfs.com/remove-334eb367a908bdd5f9638c86e0f0f992/component-ota/23/03/17/c6fccd130bd548a98bb4b8e032400616.zip

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

