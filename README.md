# Android Device Model to Marketing Name

Providing Human-friendly Name for Android Device

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

  device_model_to_marketing_name/src/main/assets/branding.properties
  device_model_to_marketing_name/src/main/assets/marketingName.properties
  
You can add entry to these two files to enrich the database.



