---
title: STEP 4 - Imposta identificatore push
description: '**pushIdentifier** è una stringa che contiene il token dispositivo per le notifiche push. Si tratta dello stesso token inviato da Firebase e passato all’SDK tramite il metodo MobileCore.setPushIdentifier.'
feature: Push
topics: MOBILE
kt: 4828
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: aa01c2f8fe1560468d0d8f3fae6291bb82f9a21f
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# Passaggio 4 - Set [!DNL pushidentifier]

La stringa **[!DNL pushidentifier]** contiene il token dispositivo per [!DNL Push] le notifiche. Si tratta dello stesso token inviato dall’SDK [!DNL Firebase] e passato all’SDK tramite il [!DNL MobileCore.setPushIdentifier] metodo .

Apri il progetto in [!DNL Android ]studio. Eliminate l&#39;intero codice in [!DNL MainActivity] tranne la prima riga dell&#39;istruzione **** pacchetto.

Incollate il seguente codice in [!DNL MainActivity]:

<!--
Removed `{.line-numbers}` below
-->

```java
import androidx.annotation.NonNull;
import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.util.Log;
import android.widget.Toast;

import com.adobe.marketing.mobile.MobileCore;
import com.google.android.gms.tasks.OnCompleteListener;
import com.google.android.gms.tasks.Task;
import com.google.firebase.iid.FirebaseInstanceId;
import com.google.firebase.iid.InstanceIdResult;

public class MainActivity extends AppCompatActivity {

@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);

registerToken();
}

void registerToken() {
FirebaseInstanceId.getInstance().getInstanceId()
    .addOnCompleteListener(new OnCompleteListener<InstanceIdResult>() {
        @Override
        public void onComplete(@NonNull Task<InstanceIdResult> task) {
            if (!task.isSuccessful()) {
                Log.w("Message App", "getInstanceId failed", task.getException());
                return;
            }

// Get new Instance ID token
String token = task.getResult().getToken();

Log.d("Got token", token);

MobileCore.setPushIdentifier(token);
}
});
}

@Override
public void onResume() {
super.onResume();
MobileCore.setApplication(getApplication());
MobileCore.lifecycleStart(null);
}

@Override
public void onPause() {
super.onPause();
MobileCore.lifecyclePause();
}
}
```

## Test dell&#39;app

Ora è il momento giusto per testare l&#39;app, prima di andare oltre.

* Eseguite l&#39;app facendo clic sulla freccia verde o selezionando **[!DNL Run->Run'app']**.
* L&#39; [!DNL Android] emulatore dovrebbe iniziare e l&#39;app dovrebbe essere in esecuzione con [!DNL "Hello World" ]testo.
* Aprite la [!DNL logcat] finestra. Cercate &quot;[!DNL Got]&quot;. Dovresti vedere il token ricevuto da [!DNL Firebase] scritto nel registro come mostrato di seguito. La stringa lunga dopo &quot;[!DNL Got token]&quot; è quella [!DNL pushidentifier ]che viene inviata a  Adobe Campaign.

![logcat-token](assets/logcat-got-token.PNG)

### Controllare gli utenti iscritti all&#39;applicazione mobile

Effettuate il login alla vostra istanza di Adobe Campaign Standard .
Spostarsi **[!UICONTROL Administration->Channels->Mobile App(AEP SDK)]**. Aprite l’applicazione mobile appropriata. Tab to the [!UICONTROL Mobile Application Subscribers] tab. Dovresti vedere un [!UICONTROL registration token ]elenco.

![abbonati a mobile-application](assets/mobile-application-subscribers.PNG)

>[!NOTE]
>
>Se non vedete il token di registrazione nella [!UICONTROL Mobile Application Subscribers] scheda STOP qui prima di continuare.
