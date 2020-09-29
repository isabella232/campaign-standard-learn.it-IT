---
title: 'Passaggio 3: registra le estensioni con la tua app mobile'
description: In questa parte aggiungeremo il codice per registrare le estensioni UserProfile, Identity, Lifecycle e Segnale.
feature: Push
topics: Mobile
kt: 4827
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 13b4f1d395dfe53f9fc5263e7b06be700e30b986
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# Passaggio 3: registra le estensioni con la tua app mobile

In questa parte aggiungeremo il codice per registrare le estensioni Profilo utente, Identità, Ciclo di vita e Segnale. Queste estensioni fanno parte di [[!UICONTROL Mobile Core Extensions]](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core). Dovremo anche registrare l&#39;estensione Adobe Campaign Standard  come mostrato nel codice seguente.

Apri il progetto in [!DNL Android] studio. Eliminate l&#39;intero codice nell&#39;app principale **tranne la prima riga dell&#39;istruzione** pacchetto.

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

Linea 32 è necessario fornire l&#39;ID del file dell&#39;ambiente della[!UICONTROL  Launch] proprietà. È possibile accedervi dalla [!UICONTROL environment tab] proprietà [!UICONTROL Launch] .

![launch-id](assets/launch-id-property.PNG)
