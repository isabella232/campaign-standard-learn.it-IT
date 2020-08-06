---
title: Passaggio 2 - Integrazione dell'SDK di Mobile
description: In questa parte, integreremo l'app Android con Mobile SDK. Per integrare l’SDK per dispositivi mobili con l’app Android
feature: Push
topics: Mobile
kt: 4826
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: c3ff1a137fb8ee9506a11f82e1a27d010bbd97e6
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# STEP 2 - Integrazione [!UICONTROL Mobile SDK] con l&#39;app Android

In questa parte, integreremo l&#39; [!DNL Android] app con [!UICONTROL Mobile SDK]. Per effettuare l&#39;integrazione [!UICONTROL mobile SDK] con l&#39; [!DNL Android] app, attenetevi alla seguente procedura:

* Apri il progetto *ACSPushTutorial* in [!DNL Android Studio]
* Creare una nuova classe Java denominata *MainApp* che si estende [!DNL android.app.Application]
* La struttura del progetto deve essere simile a quella riportata di seguito

![main-app](assets/android-main-app.PNG)

* Espandete la [!DNL Gradle Scripts] cartella. Fare doppio clic sul modulo [!DNL build.gradle] . Incolla le seguenti dipendenze nella sezione delle dipendenze del [!DNL build.gradle] file. Il [!DNL build.gradle] file deve essere simile a quello riportato di seguito

```java
implementation 'com.adobe.marketing.mobile:campaign:1.+'
implementation 'com.adobe.marketing.mobile:userprofile:1.+'
implementation 'com.adobe.marketing.mobile:sdk-core:1.+'
```

![gradazione modulo](assets/module-build-gradle.PNG)

* Sincronizzate il [!DNL Android] progetto facendo clic sul pulsante Sinc. ora per sincronizzare il progetto

## Modifica [!DNL AndroidManifest.xml]{#modify-android-manifest}

Aprite *AndroidManifest.xml* e incollate le seguenti 2 righe dopo l’elemento manifest e prima dell’elemento application. Questo consente alla tua app di comunicare con il mondo esterno

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

Copiate la riga seguente nell’elemento[!DNL android:name=".MainApp"]ApplicazioneSalvate l’ [!DNL AndroidManifest.xml]aspetto [!DNL AndroidManifest.xml] desiderato

```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.acspushtutorial">
    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />

<application
    android:name=".MainApp"
    android:allowBackup="true"
    android:icon="@mipmap/ic_launcher"
    android:label="@string/app_name"
    android:roundIcon="@mipmap/ic_launcher_round"
    android:supportsRtl="true"
    android:theme="@style/AppTheme">

<activity android:name=".MainActivity">
<intent-filter>
    <action android:name="android.intent.action.MAIN" />
    <category android:name="android.intent.category.LAUNCHER" />
</intent-filter>
</activity>
</application>

</manifest>
```
