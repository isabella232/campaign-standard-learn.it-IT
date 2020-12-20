---
title: Passaggio 1 - Creazione di app Android e configurazione per l'utilizzo di Firebase Cloud Messaging
description: In questa parte creeremo [!DNL Android] App to receive [!UICONTROL Push notifications] inviati da  Adobe Campaign Standard. Per ricevere le notifiche push, l'app deve essere registrata con Google's [!DNL Firebase Cloud Service].
feature: Push
topics: Mobile
kt: 4825
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: cdd78e97f2769503d3d4f26933ccc7f35e9b20b9
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 2%

---


# Passaggio 1 - Creazione di [!DNL Android] app e configurazione per utilizzare [!DNL Firebase Cloud Messaging]

In questa parte si crea [!DNL Android] App per ricevere [!UICONTROL Push notifications] inviati da  Adobe Campaign Standard. Per ricevere le notifiche push, l&#39;app deve essere registrata con Google [!DNL Firebase Cloud Service].

1. Accedi al tuo account [!DNL Firebase].

   [!DNL Firebase] è la piattaforma mobile di Google che ti aiuta a sviluppare rapidamente app di alta qualità. Se non si dispone di un account [!DNL Firebase], crearne uno [da qui](https://firebase.google.com).

2. Lancio [!DNL Android Studio]
3. Fare clic su **[!UICONTROL File]** > **[!UICONTROL New]** > **[!UICONTROL New Project].**
4. Seleziona **[!UICONTROL Empty Activity]** e fai clic su **[!UICONTROL Next].**

   ![android-project](assets/android-project.PNG)

5. Specifica un nome significativo per il progetto.

   Ai fini di questa demo, il nostro progetto è stato denominato *[!DNL ACSPushTutorial]*

   ![android-project-configuration](assets/android-project-configuration.PNG)

6. Accettate i nomi dei pacchetti predefiniti e fate clic su **[!DNL Finish]** per creare il progetto.
7. La struttura del progetto deve essere simile a quella della schermata sottostante

   ![android-project-structure](assets/android-project-structure.PNG)

8. Fai clic su **[!UICONTROL Tools]** > **[!UICONTROL Firebase].** (il progetto viene aggiunto a  [!DNL Firebase])
9. Fai clic su **[!UICONTROL Set up Firebase Cloud Messaging].**

   ![setup firebase](assets/android-project-firebase-messaging.PNG)

10. Fai clic su **[!UICONTROL Connect to Firebase].**
11. Una volta che l&#39;app è connessa a Firebase, fai clic su **[!UICONTROL Add FCM to your app].**
12. Fai clic su **[!UICONTROL Accept Changes].**

   Quando si aggiunge FCM all&#39;app, la procedura guidata richiede l&#39;autorizzazione per apportare alcune modifiche al progetto.

   ![[!DNL add-fcm-to-your-app]](assets/firebase-add-fcm-to-app.PNG)

Dopo l&#39;integrazione con Firebase, riceverai un messaggio simile a quello mostrato di seguito:

![[!DNL fcm-successfull]](assets/android-firebase-success.PNG)

[Accertatevi che il progetto sia elencato  [!DNL Firebase ]nella console](https://console.firebase.google.com/)

## Configurare le impostazioni [!UICONTROL Push Channel]

1. Accedere alla console [!DNL Firebase]
2. Apri il progetto **[!UICONTROL ACSPushTutorial]**.
3. Fare clic sull&#39;icona **ingranaggio** e aprire le impostazioni del progetto

   ![project-settings](assets/firebase-project-settings.PNG)

4. Passare alla scheda **[!UICONTROL Cloud Messaging]**.
5. Copiare la chiave del server

   ![server-key](assets/firebase-server-key.PNG)

6. Effettua il login alla tua istanza  Adobe Campaign Standard
7. Fare clic su **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile App].**
8. Selezionare la **[!UICONTROL Mobile Application Property]appropriata.**
9. Fare clic sull&#39;icona **[!DNL Android]** nella sezione **[!UICONTROL Push Channel settings]**.
10. Incollate la chiave server nel campo chiave del server.

Se tutto va bene dovresti vedere un messaggio di SUCCESSO.

![push-channel-settings](assets/push-channel-settings.PNG)

Per riassumere, abbiamo creato un [!DNL Android App] e collegato il [!DNL Android App] con [!DNL Firebase]. Abbiamo quindi collegato l&#39;app mobile in  Adobe Campaign con la [!DNL Android App] incollando la chiave server dell&#39;app [!DNL Android] nell&#39;app mobile in  Adobe Campaign Standard.
