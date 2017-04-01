## TWRP device tree for Samsung Galaxy Folder 2 G1600 (China)

Add to `.repo/local_manifests/eliteltechn.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
  <project path="device/samsung/eliteltechn"
	   name="Soft-Man/twrp_android_device_samsung_eliteltechn"
	   remote="github"
	   revision="android-7.1" />
  <project name="LineageOS/android_vendor_qcom_opensource_cryptfs_hw"
	   path="vendor/qcom/opensource/cryptfs_hw"
	   remote="github"
	   revision="cm-14.1" />
  <project path="kernel/samsung/msm8937"
	   name="Soft-Man/android_kernel_samsung_msm8937"
	   remote="github"
	   revision="cm-14.1" />
</manifest>
```

Then run `repo sync` to check it out.

To build:

```sh
. build/envsetup.sh
lunch omni_eliteltechn-eng
make recoveryimage
```
# twrp_android_device_samsung_eliteltechn
