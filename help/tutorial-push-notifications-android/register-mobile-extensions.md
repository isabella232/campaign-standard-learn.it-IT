---
title: 'Passaggio 3: registrare le estensioni con la tua app mobile'
description: In questa parte viene aggiunto il codice per registrare le estensioni UserProfile, Identity, Lifecycle e Signal.
feature: Push
jira: KT-4827
doc-type: tutorial
activity: use
team: TM
exl-id: d8c0d8c6-2e04-4c27-b27a-d0de79dd953b
source-git-commit: c84867ef59a10448a377a959d0b67ae71343a4aa
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 13%

---

# Passaggio 3: registrare le estensioni con la tua app mobile

In questa parte viene aggiunto il codice per registrare le estensioni Profilo utente, Identità, Ciclo di vita e Segnale. Dobbiamo anche registrare l’estensione Adobe Campaign Standard come mostrato nel codice seguente.

Apri il progetto in [!DNL Android] studio. Elimina l’intero codice in MainApp **tranne la prima riga, che è l&#39;istruzione del pacchetto**.

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

Riga 32 è necessario specificare[!UICONTROL  Launch] ID del file di ambiente della proprietà. È possibile accedervi dalla sezione [!UICONTROL environment tab] del tuo [!UICONTROL Launch] proprietà.

![launch-id](assets/launch-id-property.PNG)
