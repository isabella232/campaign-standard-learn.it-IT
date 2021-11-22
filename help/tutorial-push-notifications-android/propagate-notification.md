---
title: 'Passaggio 5: propagare le notifiche'
description: In questa parte, propagheremo il messaggio ricevuto da Adobe Campaign utilizzando Android Notification Manager.Firebase
feature: Push
kt: 4829
doc-type: tutorial
activity: use
team: TM
exl-id: b0e01224-4ddc-4999-b8c6-794e49245428
source-git-commit: ada0b029245190f53d58fa93c79c161719bfe9fd
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 1%

---

# Aggiungi servizio per inviare la notifica

In questa parte, propagheremo il messaggio ricevuto da Adobe Campaign utilizzando [!DNL Android Notification Manager]. [!DNL Notification manager] viene utilizzato per notificare all’utente gli eventi che si verificano.
Questo è il modo in cui si informa l&#39;utente che qualcosa è successo in background:

* Launch [!DNL Android Studio]
* Apri *[!DNL ACSPushTutorial]* progetto
* Espandi la struttura del progetto
* Fai clic con il pulsante destro del mouse sulla cartella del pacchetto ([!DNL com.example.acspushtutorial]) e [!DNL New ->Java Class]
* Denomina questa classe *[!DNL MyService]* e assicurati che si estenda [!DNL FirebaseMessagingService]
* Crea *[!DNL sendNotification]* in questa classe. In questo metodo è necessario impostare il contenuto e il canale della notifica utilizzando un [!DNL NotificationCompat.Builder] oggetto. Per visualizzare la notifica, invoca [!DNL NotificationManagerCompat.notify()], trasmettendolo un ID univoco per la notifica e il risultato di [!DNL NotificationCompat.Builder.build()].

<!--
Removed `{.line-numbers}` below
-->

```java
package com.example.pushmessaging;
import android.app.NotificationChannel;
import android.app.NotificationManager;
import android.app.PendingIntent;
import android.content.Context;
import android.content.Intent;
import android.media.RingtoneManager;
import android.net.Uri;
import android.os.Build;
import android.util.Log;

import androidx.core.app.NotificationCompat;

import com.google.firebase.messaging.FirebaseMessagingService;
import com.google.firebase.messaging.RemoteMessage;

import java.util.Map;

public class MyService extends FirebaseMessagingService {
@Override
public void onMessageReceived(RemoteMessage remoteMessage)
{
Map<String,String> data  = remoteMessage.getData();
Log.d("data payload: ", data.toString());
sendNotification(remoteMessage);
}


private void sendNotification(RemoteMessage message) {
Intent intent = new Intent(this, MainActivity.class);
intent.addFlags(Intent.FLAG_ACTIVITY_CLEAR_TOP);
PendingIntent pendingIntent = PendingIntent.getActivity(this, 0 /* Request code */, intent, PendingIntent.FLAG_ONE_SHOT);

String channelId = "0";
Uri defaultSoundUri = RingtoneManager.getDefaultUri(RingtoneManager.TYPE_NOTIFICATION);
NotificationCompat.Builder notificationBuilder =
        new NotificationCompat.Builder(this, channelId)
                .setSmallIcon(R.drawable.ic_launcher_background)
                .setContentTitle("Message from AEM")
                .setContentText(message.getData().get("body"))
                .setAutoCancel(true)
                .setSound(defaultSoundUri)
                .setContentIntent(pendingIntent);

NotificationManager notificationManager =
        (NotificationManager) getSystemService(Context.NOTIFICATION_SERVICE);

// Since android Oreo notification channel is needed.
if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.O) {
    NotificationChannel channel = new NotificationChannel(channelId,
            "Channel human readable title",
            NotificationManager.IMPORTANCE_DEFAULT);
    notificationManager.createNotificationChannel(channel);
}

notificationManager.notify(0 /* ID of notification */, notificationBuilder.build());
}
}
```

## Modifica [!DNL AndroidManifest.xml]

Aggiungi il servizio creato al tuo [!DNL AndroidManifest.xml]. Il finale [!DNL AndroidManifest.xml] dovrebbe essere simile al seguente:

<!--
Removed `{.line-numbers}` below
-->

```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.pushmessaging">

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
        <service
            android:name=".MyService"
            android:exported="false">
            <intent-filter>
                <action android:name="com.google.firebase.MESSAGING_EVENT" />
            </intent-filter>
        </service>

        <activity android:name=".MainActivity">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

</manifest>
```

## Eseguire l’app

Esegui l’app facendo clic sul pulsante **freccia verde** sulla barra degli strumenti o dalla [!DNL Run] menu.
