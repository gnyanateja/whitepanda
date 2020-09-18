# AppyhighUtils

To import this library, Add the following line to your app level build.gradle file.

implementation 'com.github.PrasadVennamAppy:AppyhighUtils:{latestVersion}

This library consists of following modules

    1)CleverTap Events
    2)Push Notifications (CleverTap and Firebase)
    3)InApp Notifications (CleverTap and Firebase)
    4)Ads (Interstitial and Native)
    5)Dynamic Linking
    6)Apxor Events
  
## CleverTap Events

A boolean value 'onlyFirebase' needs to be provided as parameter while using this module

'onlyFirebase'  - true  - Only Firebase Cloud Messaging is used for events
'onlyFirebase'  - false - Both CleverTap and Firebase Cloud Messaging can be used for events

## Push Notifications (CleverTap and Firebase)

CleverTap and Firebase can be used for push notifications in this library.

Add the following import statement to the top of your file  

```
import com.appyhigh.mylibrary.push.MyFirebaseMessaging

```


## InApp Notifications (CleverTap and Firebase)

## Ads (Interstitial and Native)

Add the following import statement to the top of your file  

```
import com.appyhigh.mylibrary.ads.AdUtils

```
Add the following lines inside the application tag in *AndroidManifest.xml* file
```
<meta-data
            android:name="com.google.android.gms.ads.APPLICATION_ID"
            android:value="ca-app-pub-3940256099942544~3347511713"/>

```
### Interstitial Ads

1.To add a new Interstitial Ad, call the *newInterstitialAd* method as shown

```
newInterstitialAd(ad_unit: String,activity: AppCompatActivity,screen: String, closeListener: AdCloseListener): InterstitialAd

return type : InterstitialAd

params:
ad_unit       - String,
activity      - AppCompatActivity,
screen        - String,
closeListener - AdCloseListener

```
2.To load an Interstitial Ad, call the *loadInterstitial* method as shown

```
loadInterstitial(mInterstitialAd: InterstitialAd)

params:
mInterstitialAd - InterstitialAd

```
3.To try to load the add once again, call the *tryToLoadAdOnceAgain* method as shown
```
tryToLoadAdOnceAgain(ad_unit: String, activity: AppCompatActivity, listener: AdCloseListener)

params:
ad_unit       - String,
activity      - AppCompatActivity,
listener      - AdCloseListener
```
### Native Ads

1.To load the template of Native Ad, call the *loadTemplateNativeAd* method as shown
```
loadTemplateNativeAd(context: Context, id: String, templateView: TemplateView, screen: String)

params:
context       - Context,
id            - String,
templateView  - TemplateView,
screen        - String
```
2.To populate the unifiedNative Ad, call the *unifiedNativeAd* method as shown
```
populateUnifiedNativeAdView(unifiedNativeAd: UnifiedNativeAd, adView: UnifiedNativeAdView)

params:
unifiedNativeAd - UnifiedNativeAd,
adView          - UnifiedNativeAdView

```
3.To load the other Native Ad, call the *loadOtherAd* method as shown
```
loadOtherAd(context: Context, id: String, nativeAdArea: LinearLayout, screen: String)

params:
context       - Context,
id            - String,
nativeAdArea  - LinearLayout,
screen        - String
```

## Dynamic Linking

Add the following import statement to the top of your file  

```
import com.appyhigh.mylibrary.share.ShareDynamicLink

```
1. Create a Domain Link in your linked firebase account to use Dynamic Linking

2. To receive Dynamic Links, add the following intent-filter to your *AndroidManifest.xml* file

```
<intent-filter>
    <action android:name="android.intent.action.VIEW"/>
    <category android:name="android.intent.category.DEFAULT"/>
    <category android:name="android.intent.category.BROWSABLE"/>
    <data
        android:host="your_domainLink"
        android:scheme="https"/>
</intent-filter>
```

3. To create and share dynamic links that opens the link on your app, call the *createShortLink* method as shown
```
createShortLink(link: String, domain: String, packageName: String?, linkMessage: String, context: Context)

params:
link        - deepLink of your project
domain      - domainLink of your project which you already created on the linked firebase account
packageName - packageName of your project
linkMessage - extra message that you want while sharing your link
context     - Context

```

4. To receive the deep link, call the *getDynamicLink* method as shown
```
getDynamicLink(intent: Intent):Uri?

return type : Uri

params:
intent      - Intent
```
  

## Apxor Events

