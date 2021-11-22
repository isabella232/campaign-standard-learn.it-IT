---
title: STEP 4 - Imposta identificatore push
description: Il **pushIdentifier** è una stringa che contiene il token dispositivo per le notifiche push. Si tratta dello stesso token inviato da Firebase e passato all'SDK utilizzando il metodo MobileCore.setPushIdentifier .
feature: Push
kt: 4828
doc-type: tutorial
activity: use
team: TM
exl-id: 08387b84-edaa-45ee-ae66-53bcbd5c7c39
source-git-commit: 5a2f8c9a78bf5100b272f9b4461131545b3aeb8b
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Passaggio 4 - Imposta [!DNL pushidentifier]

La **[!DNL pushidentifier]** è una stringa che contiene il token dispositivo per [!DNL Push] notifiche. È lo stesso token inviato da [!DNL Firebase] e viene passato all&#39;SDK utilizzando [!DNL MobileCore.setPushIdentifier] metodo .

Apri il progetto in [!DNL Android™ ]studio. Elimina l&#39;intero codice in [!DNL MainActivity] **ad eccezione della prima riga che è l&#39;istruzione package**.

Incolla il seguente codice in [!DNL MainActivity]:

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

## Verificare l’app

Ora è il momento di testare l’app prima di procedere ulteriormente.

* Esegui l’app facendo clic sulla freccia verde o seleziona **[!DNL Run->Run'app']**.
* La [!DNL Android™] l&#39;emulatore dovrebbe iniziare e dovresti vedere l&#39;app in esecuzione con [!DNL "Hello World" ]testo.
* Apri [!DNL logcat] finestra. Cerca &quot;[!DNL Got]&quot;. Dovresti visualizzare il token ricevuto da [!DNL Firebase] scritto nel registro come mostrato di seguito. La stringa lunga dopo &quot;[!DNL Got token]&quot; è [!DNL pushidentifier ]viene inviato ad Adobe Campaign.

![token](assets/logcat-got-token.PNG)

### Controlla utenti abbonati a un&#39;applicazione mobile

Accedi alla tua istanza Adobe Campaign Standard.
Naviga **[!UICONTROL Administration->Channels->Mobile App(Experience Platform SDK)]**. Apri l’applicazione mobile appropriata. Passa alla scheda [!UICONTROL Mobile Application Subscribers] scheda . Dovresti visualizzare un [!UICONTROL registration token ]elencati.

![abbonati a mobile-application](assets/mobile-application-subscribers.PNG)

>[!NOTE]
>
>Se non vedi il token di registrazione nel [!UICONTROL Mobile Application Subscribers] premere STOP prima di procedere ulteriormente.
