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
	
    -----------------------IMMENSITY FORK IVAN-----------------------

	rm -rf kernel/xiaomi/sm8250   
	git clone https://github.com/VoidUI-Devices/kernel_xiaomi_sm8250.git kernel/xiaomi/sm8250
    
    
    
**Xiaomi Hardware**

	rm -rf hardware/xiaomi
	git clone https://github.com/Yohan-Black/hardware_xiaomi.git hardware/xiaomi


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


