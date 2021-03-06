---
summary: Extend the functionalities of your mobile apps by using plugins.
tags: runtime-mobile; support-application_development; support-Mobile_Apps; support-Mobile_Apps-featured
---

# Mobile Plugins

When developing a mobile app you often want to use the capabilities of the mobile device, such as the GPS or notifications. You can achieve this in OutSystems using plugins. A plugin is a module that acts as a wrapper for an Apache Cordova plugin and enables you to use native mobile features.

You can find [ready-to-use plugins in Forge](<https://www.outsystems.com/forge/#category=plug-ins>), which contains both officially supported plugins and plugins created by the OutSystems Community. If you want to create your own plugins for use in mobile apps, do it by [wrapping an Apache Cordova plugin into a module](<using-cordova-plugins.md>).

## Using a mobile plugin

[Install the plugin](<../../getting-started/component.md>) in the environment as any other component. Use the client actions of the plugin module to call the native capabilities of the device within your application. The plugin must support the mobile platforms (iOS, Android) for which you are creating an app or the app generation will fail.

Each time you add, remove, or modify the plugin in an app, OutSystems [rebuilds the native shell](<../../deliver-mobile/mobile-app-update-scenarios.md#Situations_When_the_User_Must_Install_a_New_Build>) which you then have to distribute to the end users for installation.

You must [include the plugin license](<../../deliver-mobile/compliance-with-third-party-licenses.md#Include_the_Third_Party_Licenses_Used_by_Plug-ins_or_Components>) in your app to respect the license agreements of that plugin. These license agreements are usually placed in the About page of the app that uses them.

## What are the supported plugins provided by OutSystems { #Supported_Plugins }

This is the list of officially supported mobile plugins. Some of these plugins are already supported when distributing your app as a Progressive Web App (PWA).

Plugin | Description | Supported in PWA
-------|-------------|---
[AppShield](<https://www.outsystems.com/forge/component-overview/9379//>) | Protect your mobile apps from tampering. OutSystems AppShield hardens the native mobile build, enabling the app to detect attempts of modification and misuse. | —
[Card IO](<https://www.outsystems.com/forge/component/1438/card-io-plugin/>) | Automatically get the details of a credit card just by taking a picture. | —
[Camera](<http://www.outsystems.com/forge/component-discussions/1390/Camera+Plugin>) | Enable your application to access the camera capabilities of the device. | Yes
[Calendar](<https://www.outsystems.com/forge/component/1566/calendar-plugin/>) | Access the calendar of your device. | —
[Contacts](<http://www.outsystems.com/forge/component-discussions/1394/Contacts+Plugin>) | Access the contacts of your device. | —
[Ciphered Local Storage](<https://www.outsystems.com/forge/component-details/1500/ciphered-local-storage-plugin/>) | Keep your mobile application's sensitive data safe using a ciphered Local Storage database. | —
[InApp Browser](<https://www.outsystems.com/forge/component/1558/inappbrowser-plugin/>) | Open external URLs directly in your application. | —
[OneSignal Notifications](<http://www.outsystems.com/forge/component/2119/onesignal-plugin/>) | Push Notifications using OneSignal, with deep-linking and actions. | —
[Pushwoosh Notifications](<http://www.outsystems.com/forge/component/1556/pushwoosh-plugin/>) | Push Notifications using Pushwoosh, with deep-linking and actions. | —
[Touch ID](<https://www.outsystems.com/forge/component-details/1431/Touch+ID+Plugin/>) | Use authentication with Touch ID in your application. | —
[QR/Barcode scanner](<https://www.outsystems.com/forge/component/1403/barcode-plugin/>) | Scan barcodes and QR codes. | —
[SSL Pinning](<https://www.outsystems.com/forge/component-discussions/1873/SSL+Pinning+Plugin>) | Provide an extra layer of security to HTTPS communications by adding a verification of the server certificate against hashes of public keys. | —
[Key Store](<https://www.outsystems.com/forge/component/1550/Key+Store+Plugin/>) | Store small amounts of sensitive information on your device. The keystore secures data by encrypting the data before storing it, and the platform itself carefully controls access to stored items. | —
[Local Notifications](<http://www.outsystems.com/forge/component/1541/local-notifications-plugin/>) | Send app notifications to the device when the application isn't running in the foreground. | —
[Location](<https://www.outsystems.com/forge/component/1395/location-plugin/>) | Access the GPS capabilities of the user's device. For example the latitude, longitude and the altitude of the user's device. | Yes

**Included plugins in OutSystems Now (discontinued)**

The plugins included in the OutSystems Now mobile app, now discontinued, are the following:

* Camera, Card IO, Local Notifications, QR/Barcode scanner, Location, Contacts, InApp Browser, Touch ID, Calendar, Key Store

## Built-in plugins

Mobile apps generated by OutSystems have a native shell with the following plugins which OutSystems uses internally. You may see the names of these plugins in the [native mobile shell logs](<../../managing-the-applications-lifecycle/monitor-and-troubleshoot/monitoring-an-environment.md>).

Plugin | Description
-------|-----------------
OS Cache       | Allows your application to run offline or with bad network conditions.
OS Cordova Loader | Loads the Cordova engine on your app.
OS Deeplinks   | Allows opening hyperlinks to specific screens of your app.
OS DB Upgrader | Manages the local storage of your app.
OS Manifest    | Provides a parser for the app manifest.
OS Pre-Bundle  | Handles the content of pre-bundled resources on your app.
OS Security    | Provides the required APIs for the security layer.
Mobile AppFeedback | Enables the user to invoke App Feedback for submitting feedback about the app. (Only present in the native shell if the App Feedback feature is [enabled](<../../managing-the-applications-lifecycle/app-feedback/user-feedback-enable.md>) in the mobile app.)
NetworkStatus  | Allows your application to know when the device is online, offline and the type of network available (for example, Wifi, 3G, 4G).
