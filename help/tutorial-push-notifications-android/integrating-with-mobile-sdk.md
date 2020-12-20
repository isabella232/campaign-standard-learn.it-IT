---
title: Passaggio 2 - Integrazione di Mobile SDK
description: In questa parte, integreremo l'app Android con Mobile SDK. Per integrare l’SDK per dispositivi mobili con l’app Android
feature: Push
topics: Mobile
kt: 4826
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 13b4f1d395dfe53f9fc5263e7b06be700e30b986
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 3%

---

# STEP 2 - Integrare [!UICONTROL Mobile SDK] con l&#39;app Android

In questa parte, integreremo l&#39;app [!DNL Android] con [!UICONTROL Mobile SDK]. Per integrare [!UICONTROL mobile SDK] con l&#39;app [!DNL Android], attenetevi alla seguente procedura:

* Aprire il progetto *ACSPushTutorial* in [!DNL Android Studio]
* Creare una nuova classe Java denominata *MainApp* che si estende[!DNL android.app.Application]
* La struttura del progetto deve essere simile a quella riportata di seguito

![main-app](assets/android-main-app.PNG)

* Espandete la cartella [!DNL Gradle Scripts]. Fare doppio clic su [!DNL build.gradle] del modulo. Incollate le seguenti dipendenze nella sezione delle dipendenze del file [!DNL build.gradle]. Il file [!DNL build.gradle] deve essere simile a quello riportato di seguito

<!--
Removed `{.line-numbers}` below
-->

```java
implementation 'com.adobe.marketing.mobile:campaign:1.+'
implementation 'com.adobe.marketing.mobile:userprofile:1.+'
implementation 'com.adobe.marketing.mobile:sdk-core:1.+'
```

![gradazione modulo](assets/module-build-gradle.PNG)

* Sincronizzate il progetto [!DNL Android] facendo clic sul pulsante Sinc. ora per sincronizzare il progetto

## Modifica [!DNL AndroidManifest.xml]{#modify-android-manifest}

Aprite *AndroidManifest.xml* e incollate le 2 righe seguenti dopo l&#39;elemento manifest e prima dell&#39;elemento application. Questo consente alla tua app di comunicare con il mondo esterno

<!--
Removed `{.line-numbers}` below
-->

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

Copiate la riga seguente nell’elemento applicazione
[!DNL android:name=".MainApp"]
Salva la tua [!DNL AndroidManifest.xml]
Il tuo [!DNL AndroidManifest.xml] dovrebbe essere simile a questo

<!--
Removed `{.line-numbers}` below
-->

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
