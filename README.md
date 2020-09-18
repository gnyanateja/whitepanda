# AppyhighUtils

To import this library, Add the following line to your app level build.gradle file.

implementation 'com.github.PrasadVennamAppy:AppyhighUtils:{latestVersion}

This library consists of following modules

    1)CleverTap Events
    2)Push Notifications(CleverTap and Firebase)
    3)InApp Notifications(CleverTap and Firebase)
    4)Ads (Interstitial and Native)
    5)Dynamic Linking
    6)Apxor Events
  
## CleverTap Events

A boolean value 'onlyFirebase' needs to be provided as parameter while using this module

'onlyFirebase'  - true  - Only Firebase Cloud Messaging is used for events
'onlyFirebase'  - false - Both CleverTap and Firebase Cloud Messaging can be used for events

## Push Notifications

CleverTap and Firebase can be used for push notifications in this library.

Add the following import statement to the top of your file  

```
import com.appyhigh.mylibrary.push.MyFirebaseMessaging

```


## InApp Notifications

## Ads

## Dynamic Linking

Add the following import statement to the top of your file  

```
import com.appyhigh.mylibrary.share.ShareDynamicLink

```

1. To receive Dynamic Links, add the following intent-filter to your *AndroidManifest.xml* file

```
<intent-filter>
    <action android:name="android.intent.action.VIEW"/>
    <category android:name="android.intent.category.DEFAULT"/>
    <category android:name="android.intent.category.BROWSABLE"/>
    <data
        android:host="example.com"
        android:scheme="https"/>
</intent-filter>
```

2. To create and share dynamic links that opens the link on your app, call the *createShortLink* method as shown
```
createShortLink(link: String, domain: String, packageName: String?, linkMessage: String, context: Context)
params:
link        - deepLink
domain      - domainLink
packageName - packageName of your project
linkMessage - extra message that you want while sharing your link
context     - current state of application/object

```

4. To receive the deep link, call the *getDynamicLink* method as shown
```
getDynamicLink(intent: Intent):Uri?
return type : Uri
```
  

## Apxor Events

