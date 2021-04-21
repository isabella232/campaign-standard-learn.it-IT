---
title: 'Passaggio 1: creazione dell''app Android e configurazione per l''utilizzo di Firebase Cloud Messaging'
description: In questa parte creeremo [!DNL Android] App to receive [!UICONTROL Push notifications] inviati da Adobe Campaign Standard. Per ricevere le notifiche push, l’app deve essere registrata con Google’s [!DNL Firebase Cloud Service].
feature: Push
kt: 4825
doc-type: tutorial
activity: use
team: TM
exl-id: f087d9f2-cce9-4903-977f-3c5b47522c06
translation-type: tm+mt
source-git-commit: ada0b029245190f53d58fa93c79c161719bfe9fd
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 3%

---

# Passaggio 1: creazione di [!DNL Android] app e configurazione per utilizzare [!DNL Firebase Cloud Messaging]

In questa parte creerai [!DNL Android] un&#39;app per ricevere [!UICONTROL Push notifications] inviati da Adobe Campaign Standard. Per ricevere le notifiche push, l’app deve essere registrata con Google [!DNL Firebase Cloud Service].

1. Accedi al tuo account [!DNL Firebase].

   [!DNL Firebase] è la piattaforma mobile di Google che ti aiuta a sviluppare rapidamente app di alta qualità. Se non disponi di un account [!DNL Firebase], creane uno [da qui](https://firebase.google.com).

2. Launch [!DNL Android Studio]
3. Fare clic su **[!UICONTROL File]** > **[!UICONTROL New]** > **[!UICONTROL New Project].**
4. Seleziona **[!UICONTROL Empty Activity]** e fai clic su **[!UICONTROL Next].**

   ![progetto android](assets/android-project.PNG)

5. Fornisci un nome significativo al progetto.

   Ai fini della presente demo, il nostro progetto è denominato *[!DNL ACSPushTutorial]*

   ![android-project-configuration](assets/android-project-configuration.PNG)

6. Accetta i nomi dei pacchetti predefiniti e fai clic su **[!DNL Finish]** per creare il progetto.
7. La struttura del progetto deve avere un aspetto simile alla schermata sottostante

   ![android-project-structure](assets/android-project-structure.PNG)

8. Fai clic su **[!UICONTROL Tools]** > **[!UICONTROL Firebase].** (questo aggiunge il progetto a  [!DNL Firebase])
9. Fai clic su **[!UICONTROL Set up Firebase Cloud Messaging].**

   ![imposta firebase](assets/android-project-firebase-messaging.PNG)

10. Fai clic su **[!UICONTROL Connect to Firebase].**
11. Dopo aver connesso l&#39;app a Firebase, fai clic su **[!UICONTROL Add FCM to your app].**
12. Fai clic su **[!UICONTROL Accept Changes].**

   Quando aggiungi FCM all’app, la procedura guidata richiede l’autorizzazione per apportare alcune modifiche al progetto.

   ![[!DNL add-fcm-to-your-app]](assets/firebase-add-fcm-to-app.PNG)

Una volta completata con successo l’app con Firebase, riceverai un messaggio come quello mostrato di seguito:

![[!DNL fcm-successfull]](assets/android-firebase-success.PNG)

[Accertati che il progetto sia elencato  [!DNL Firebase ]nella console](https://console.firebase.google.com/)

## Configurare le impostazioni [!UICONTROL Push Channel]

1. Accedi alla console [!DNL Firebase]
2. Apri il progetto **[!UICONTROL ACSPushTutorial]** .
3. Fai clic sull’ **icona a forma di ingranaggio** e apri le impostazioni del progetto

   ![impostazioni progetto](assets/firebase-project-settings.PNG)

4. Passa alla scheda **[!UICONTROL Cloud Messaging]** .
5. Copia la chiave server

   ![chiave server](assets/firebase-server-key.PNG)

6. Accedi alla tua istanza Adobe Campaign Standard
7. Fare clic su **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile App].**
8. Selezionare il **[!UICONTROL Mobile Application Property]appropriato.**
9. Fai clic sull&#39;icona **[!DNL Android]** nella sezione **[!UICONTROL Push Channel settings]** .
10. Incolla la chiave server nel campo chiave server .

Se tutto va bene dovresti vedere un messaggio SUCCESS.

![impostazioni dei canali push](assets/push-channel-settings.PNG)

Per riepilogare, abbiamo creato un [!DNL Android App] e collegato il [!DNL Android App] con [!DNL Firebase]. Abbiamo quindi connesso l’app mobile in Adobe Campaign con la [!DNL Android App] incollando la chiave server dell’ [!DNL Android] nell’app mobile in Adobe Campaign Standard.
