# Android Device Model to Marketing Name

Providing Human-friendly Name for Android Devices

It will convert Build.MODEL to the marketing name of the device, for example "SM-G9200" to "Galaxy S6".

# How to use this library in your application

## 1. add "multiple-images-selector" dependency

This library is now available in jcenter.

Add "device-model-to-marketing-name" as dependency to your project:

    compile 'com.zfdang.devicemodeltomarketingname:device-model-to-marketing-name:1.0.0'

## 2. Use it in your application:

    // Build.MODEL = "SM-G9200"
    String marketingName = DeviceMarketingName.getInstance(this).getDeviceMarketingName(false);
    // marketingName is now "Galaxy S6"
    String marketingNameWithBrand = DeviceMarketingName.getInstance(this).getDeviceMarketingName(true);
    // marketingNameWithBrand is now "Samsung-Galaxy S6"

## 3. Contribute to this library

Now all Build.MODEL <-> Marketing Name are extracted from Supported devices of Google Play:

https://support.google.com/googleplay/android-developer/answer/6154891?hl=en

The extracted results are stored as Java properties:

[device_model_to_marketing_name/src/main/assets/branding.properties](https://github.com/zfdang/android-device-model-to-marketing-name/blob/master/device_model_to_marketing_name/src/main/assets/branding.properties)
[device_model_to_marketing_name/src/main/assets/marketingName.properties](https://github.com/zfdang/android-device-model-to-marketing-name/blob/master/device_model_to_marketing_name/src/main/assets/marketingName.properties)
  
You can add entries to these two files to enrich the database.

NOTE: please make sure all strings are escaped properly: 
    
    http://stackoverflow.com/questions/2406975/how-to-escape-the-equals-sign-in-properties-files


