---
title: 'Passaggio 3: registrare le estensioni con la tua app mobile'
description: In questa parte aggiungeremo il codice per registrare le estensioni UserProfile, Identity, Lifecycle e Signal.
feature: Push
kt: 4827
doc-type: tutorial
activity: use
team: TM
exl-id: d8c0d8c6-2e04-4c27-b27a-d0de79dd953b
source-git-commit: ada0b029245190f53d58fa93c79c161719bfe9fd
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 11%

---

# Passaggio 3: registrare le estensioni con la tua app mobile

In questa parte aggiungeremo il codice per registrare le estensioni Profilo utente, Identità, Ciclo di vita e Segnale . Queste estensioni fanno parte di [[!UICONTROL Mobile Core Extensions]](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core). Sarà inoltre necessario registrare l’estensione Adobe Campaign Standard come mostrato nel codice seguente.

Apri il progetto in [!DNL Android] studio. Elimina l&#39;intero codice in MainApp **ad eccezione della prima riga che è l&#39;istruzione package**.

Incolla il seguente codice in MainApp

<!--
Removed `{.line-numbers}` below
-->

```java
import [!DNL android].app.Application;
import android.util.Log;

import com.adobe.marketing.mobile.AdobeCallback;
import com.adobe.marketing.mobile.Campaign;
import com.adobe.marketing.mobile.Identity;
import com.adobe.marketing.mobile.InvalidInitException;
import com.adobe.marketing.mobile.Lifecycle;
import com.adobe.marketing.mobile.LoggingMode;
import com.adobe.marketing.mobile.MobileCore;
import com.adobe.marketing.mobile.Signal;
import com.adobe.marketing.mobile.UserProfile;

public class MainApp extends Application {

@Override
public void onCreate() {
super.onCreate();

MobileCore.setApplication(this);
MobileCore.setLogLevel(LoggingMode.DEBUG);

try{
    Campaign.registerExtension();
    UserProfile.registerExtension();
    Identity.registerExtension();
    Lifecycle.registerExtension();
    Signal.registerExtension();
    MobileCore.start(new AdobeCallback () {
        @Override
        public void call(Object o) {
            MobileCore.configureWithAppID("copy your launch property id here");
        }
    });
} catch (InvalidInitException e) {
    Log.d("ACS Exception", "exception");
}
}
}
```

Linea 32 è necessario fornire[!UICONTROL  Launch] ID file di ambiente della proprietà. È accessibile dal [!UICONTROL environment tab] del tuo [!UICONTROL Launch] proprietà.

![launch-id](assets/launch-id-property.PNG)
