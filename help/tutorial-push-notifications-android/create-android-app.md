---
title: Passaggio 1 - Creazione di app Android e configurazione per l'utilizzo di Firebase Cloud Messaging
description: In questa parte creeremo [!DNL Android] App per ricevere [!UICONTROL Push notifications] inviato da Adobe Campaign Standard. Per ricevere le notifiche push, l'app deve essere registrata con il [!DNL Firebase Cloud Service] di Google.
feature: Push
topics: Mobile
kt: 4825
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: afe1ae6c8d73b7b776e0eec327fa16db76c23ce1
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 1%

---


# Passaggio 1 - Creazione di [!DNL Android] app e configurazione da utilizzare [!DNL Firebase Cloud Messaging]

In questa parte, creerai [!DNL Android] l&#39;app da ricevere [!UICONTROL Push notifications] inviata da Adobe Campaign Standard. Per ricevere le notifiche push, l&#39;app deve essere registrata presso Google [!DNL Firebase Cloud Service].

1. Accedi al tuo [!DNL Firebase] account.

   [!DNL Firebase] è la piattaforma mobile di Google che ti aiuta a sviluppare rapidamente app di alta qualità. Se non hai un [!DNL Firebase] account, creane uno [da qui](https://firebase.google.com).

2. Launch [!DNL Android Studio]
3. Click **[!UICONTROL File]** > **[!UICONTROL New]** > **[!UICONTROL New Project].**
4. Selezionate **[!UICONTROL Empty Activity]** e fate clic su **[!UICONTROL Next].**

   ![android-project](assets/android-project.PNG)

5. Specifica un nome significativo per il progetto.

   Ai fini di questa demo abbiamo nominato il nostro progetto come *[!DNL ACSPushTutorial]*

   ![android-project-configuration](assets/android-project-configuration.PNG)

6. Accettate i nomi dei pacchetti predefiniti e fate clic **[!DNL Finish]** per creare il progetto.
7. La struttura del progetto deve essere simile a quella della schermata sottostante

   ![android-project-structure](assets/android-project-structure.PNG)

8. Clic **[!UICONTROL Tools]** > **[!UICONTROL Firebase].**(il progetto viene aggiunto a[!DNL Firebase])
9. Clic **[!UICONTROL Set up Firebase Cloud Messaging].**

   ![setup firebase](assets/android-project-firebase-messaging.PNG)

10. Clic **[!UICONTROL Connect to Firebase].**
11. Dopo aver connesso l&#39;app a Firebase, fai clic su **[!UICONTROL Add FCM to your app].**
12. Clic **[!UICONTROL Accept Changes].**

   Quando si aggiunge FCM all&#39;app, la procedura guidata richiede l&#39;autorizzazione per apportare alcune modifiche al progetto.

   ![[!DNL add-fcm-to-your-app]](assets/firebase-add-fcm-to-app.PNG)

Dopo l&#39;integrazione con Firebase, riceverai un messaggio simile a quello mostrato di seguito:

![[!DNL fcm-successfull]](assets/android-firebase-success.PNG)

[Accertatevi che il progetto sia elencato in [!DNL Firebase ] console](https://console.firebase.google.com/)

## Configura [!UICONTROL Push Channel] impostazioni

1. Accesso alla [!DNL Firebase] console
2. Apri il **[!UICONTROL ACSPushTutorial]** progetto.
3. Fate clic sull&#39;icona **dell&#39;** ingranaggio e aprite le impostazioni del progetto

   ![project-settings](assets/firebase-project-settings.PNG)

4. Passa alla **[!UICONTROL Cloud Messaging]** scheda.
5. Copiare la chiave del server

   ![server-key](assets/firebase-server-key.PNG)

6. Accedi alla tua istanza di Adobe Campaign Standard
7. Click **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile App].**
8. Selezionare la voce appropriata **[!UICONTROL Mobile Application Property].**
9. Fate clic sull&#39; **[!DNL Android]icona **nella **[!UICONTROL Push Channel settings]**sezione.
10. Incollate la chiave server nel campo chiave del server.

Se tutto va bene dovresti vedere un messaggio di SUCCESSO.

![push-channel-settings](assets/push-channel-settings.PNG)

Per riassumere, abbiamo creato un [!DNL Android App] e collegato il [!DNL Android App] con [!DNL Firebase]. Abbiamo quindi connesso l&#39;app mobile in Adobe Campaign con l&#39;app [!DNL Android App] incollando la chiave server dell&#39; [!DNL Android] app nell&#39;app mobile in Adobe Campaign Standard.
