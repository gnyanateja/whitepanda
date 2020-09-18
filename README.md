# AppyhighUtils

To import this library, Add the following line to your app level build.gradle file.

implementation 'com.github.PrasadVennamAppy:AppyhighUtils:[![](https://jitpack.io/v/PrasadVennamAppy/AppyhighUtils.svg)](https://jitpack.io/#PrasadVennamAppy/AppyhighUtils)

This library consists of following modules

    1)Push notifications
    2)InApp notifications
    2)Ads
    3)Dynamic Linking
    4)Apxor Events
  
## Push notifications

CleverTap module and Firebase Cloud Messaging can be used for push notifications in this library.
A boolean value 'onlyFirebase' needs to be provided as parameter while using this module

'onlyFirebase'  - true  - Only Firebase Cloud Messaging is used for push notifications
'onlyFirebase'  - false - Both CleverTap and Firebase Cloud Messaging can be used for push notifications
