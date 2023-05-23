---
title: 'Passaggio 2: integrare l’SDK per dispositivi mobili'
description: In questa parte, integreremo l’app Android con Mobile SDK. Integrare Mobile SDK con l’app Android
feature: Push
kt: 4826
doc-type: tutorial
activity: use
team: TM
recommendations: noDisplay
exl-id: 0fa53536-8330-4e96-be2f-afc078609bcd
source-git-commit: 57dbf456625d22cd2e4526d92e5a8c20a048d339
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 3%

---

# PASSAGGIO 2 - Integrare [!UICONTROL Mobile SDK] con app Android

In questa parte, integreremo [!DNL Android] app con [!UICONTROL Mobile SDK]. Per integrare [!UICONTROL mobile SDK] con [!DNL Android] , segui i seguenti passaggi:

* Apri *ACSPushTutorial* progetto in [!DNL Android Studio]
* Crea una nuova classe Java denominata *MainApp* che si estende [!DNL android.app.Application]
* La struttura del progetto a questo punto dovrebbe essere simile a quella riportata di seguito

![main-app](assets/android-main-app.PNG)

* Espandi [!DNL Gradle Scripts] cartella. Fai doppio clic su [!DNL build.gradle] del modulo. Incolla le dipendenze seguenti nella sezione dipendenze della sezione [!DNL build.gradle] file. Il tuo [!DNL build.gradle] Il file dovrebbe ora avere un aspetto simile al seguente

<!--
Removed `{.line-numbers}` below
-->

```java
implementation 'com.adobe.marketing.mobile:campaign:1.+'
implementation 'com.adobe.marketing.mobile:userprofile:1.+'
implementation 'com.adobe.marketing.mobile:sdk-core:1.+'
```

![module-gradle](assets/module-build-gradle.PNG)

* Sincronizza [!DNL Android] progetto facendo clic sul pulsante sincronizza ora per sincronizzare il progetto

## Modifica [!DNL AndroidManifest.xml]{#modify-android-manifest}

Apri *AndroidManifest.xml* e incolla le due righe seguenti dopo l&#39;elemento manifest e prima dell&#39;elemento application. Questo consente all’app di comunicare con il mondo esterno

<!--
Removed `{.line-numbers}` below
-->

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

Copia la riga seguente nell’elemento applicativo
[!DNL android:name=".MainApp"]
Salva [!DNL AndroidManifest.xml]
Il tuo [!DNL AndroidManifest.xml] dovrebbe avere questo aspetto

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
