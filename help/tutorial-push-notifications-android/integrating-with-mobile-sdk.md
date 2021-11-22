---
title: 'Passaggio 2: integrare l’SDK per dispositivi mobili'
description: In questa parte, integreremo l’app Android con Mobile SDK. Per integrare l’SDK mobile con l’app Android
feature: Push
kt: 4826
doc-type: tutorial
activity: use
team: TM
exl-id: 0fa53536-8330-4e96-be2f-afc078609bcd
source-git-commit: ada0b029245190f53d58fa93c79c161719bfe9fd
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 3%

---

# PASSAGGIO 2 - Integrazione [!UICONTROL Mobile SDK] con app Android

In questa parte, integreremo il [!DNL Android] app con [!UICONTROL Mobile SDK]. Per integrare [!UICONTROL mobile SDK] con [!DNL Android] app, segui i seguenti passaggi:

* Apri *ACSPushTutorial* progetto in [!DNL Android Studio]
* Crea una nuova classe java denominata *MainApp* che si estende [!DNL android.app.Application]
* A questo punto la struttura del progetto dovrebbe essere simile a quella riportata di seguito

![applicazione principale](assets/android-main-app.PNG)

* Espandi la [!DNL Gradle Scripts] cartella. Fai doppio clic sul pulsante [!DNL build.gradle] del modulo. Incolla le seguenti dipendenze nella sezione dipendenze del [!DNL build.gradle] file. Le [!DNL build.gradle] Il file dovrebbe ora essere simile al seguente

<!--
Removed `{.line-numbers}` below
-->

```java
implementation 'com.adobe.marketing.mobile:campaign:1.+'
implementation 'com.adobe.marketing.mobile:userprofile:1.+'
implementation 'com.adobe.marketing.mobile:sdk-core:1.+'
```

![gradle-modulo](assets/module-build-gradle.PNG)

* Sincronizza [!DNL Android] per sincronizzare il progetto, fai clic sul pulsante sincronizza ora

## Modifica [!DNL AndroidManifest.xml]{#modify-android-manifest}

Apri *AndroidManifest.xml* e incolla le seguenti 2 righe dopo l’elemento manifest e prima dell’elemento application . Questo consente all&#39;app di comunicare con il mondo esterno

<!--
Removed `{.line-numbers}` below
-->

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

Copia la seguente riga nell’elemento dell’applicazione
[!DNL android:name=".MainApp"]
Salva il tuo [!DNL AndroidManifest.xml]
Le [!DNL AndroidManifest.xml] dovrebbe essere così

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
