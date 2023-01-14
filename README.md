# Sync_Trees_Alioth
Links and dependencies used to compile for Alioth


**Device Tree**

 rm -rf device/xiaomi/alioth
 git clone https://github.com/Yohan-Black/device_xiaomi_alioth.git -b thirteen device/xiaomi/alioth

 rm -rf device/xiaomi/sm8250-common 
 git clone https://github.com/Yohan-Black/device_xiaomi_sm8250-common.git -b thirteen  device/xiaomi/sm8250-common 


**vendor tree**

 rm -rf vendor/xiaomi/alioth
 git clone https://github.com/Yohan-Black/vendor_xiaomi_alioth.git vendor/xiaomi/alioth

 rm -rf vendor/xiaomi/sm8250-common
 git clone https://github.com/Yohan-Black/vendor_xiaomi_sm8250-common.git -b thirteen  vendor/xiaomi/sm8250-common
	

**Kernels**
	
    -----------------------N0 kernel-----------------	

 rm -rf kernel/xiaomi/sm8250    
 git clone https://github.com/EmanuelCN/kernel_xiaomi_sm8250.git -b staging kernel/xiaomi/sm8250
    
    
**clang**
 
 	--------------Clang Zyc-----------------------------------
    
 rm -rf prebuilts/clang/host/linux-x86/clang-zyc
 git clone https://gitlab.com/GhosutoX/zyc-clang16.git prebuilts/clang/host/linux-x86/clang-zyc
    
    
**Xiaomi Harware**

 rm -rf hardware/xiaomi
 https://github.com/Yohan-Black/hardware_xiaomi.git


**HALS**

 rm -rf vendor/qcom/opensource/audio-hal/st-hal
 git clone https://github.com/PixelExperience/vendor_qcom_opensource_audio-hal_st-hal vendor/qcom/opensource/audio-hal/st-hal

 rm -rf vendor/qcom/opensource/interfaces
 git clone https://github.com/PixelExperience/vendor_qcom_opensource_interfaces -b thirteen vendor/qcom/opensource/interfaces

 rm -rf hardware/qcom-caf/sm8250/display 
 git clone https://github.com/VoidUI-Tiramisu/hardware_qcom-caf_sm8250_display.git hardware/qcom-caf/sm8250/display 

 rm -rf hardware/qcom-caf/sm8250/media 
 git clone https://github.com/VoidUI-Tiramisu/hardware_qcom-caf_sm8250_media.git hardware/qcom-caf/sm8250/media 

 rm -rf hardware/qcom-caf/sm8250/audio 
 git clone https://github.com/VoidUI-Tiramisu/hardware_qcom-caf_sm8250_audio.git hardware/qcom-caf/sm8250/audio 


**Source support to Import and adapt Xiaomi Proprietary vibrator hal, if the source does not have this support there will be no vibration on the device. also if the source does not support hal vibrator hal, it will terminate bootloop, check commits in device/common and revert**

 cd frameworks/native
 git fetch https://github.com/VoidUI-Tiramisu/frameworks_native.git aosp-13-r13
 git cherry-pick c771defb1c2c539a700cf14b784c6ea3580ce4ea
 cd ..
 cd ..

**In cause of bootloop by vibrator hal**

 cd device/xiaomi/sm8250-common
 git revert 8e488cfe4b372cbb4a28b119d0c15ed707866b46  (https://github.com/PalyrimOS-Devices/device_xiaomi_sm8250-common/commit/8e488cfe4b372cbb4a28b119d0c15ed707866b46)
 git revert 7a5a843f9bd87a331f689398bf28d1ca4c1e2a2c  (https://github.com/PalyrimOS-Devices/device_xiaomi_sm8250-common/commit/7a5a843f9bd87a331f689398bf28d1ca4c1e2a2c)