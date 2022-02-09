---
title: 'Passaggio 1: creazione dell''app Android e configurazione per l''utilizzo di Firebase Cloud Messaging'
description: In questa parte creeremo [!DNL Android] App da ricevere [!UICONTROL Push notifications] inviato da Adobe Campaign Standard. Per ricevere le notifiche push, l’app deve essere registrata con Google [!DNL Firebase Cloud Service].
feature: Push
kt: 4825
doc-type: tutorial
activity: use
team: TM
recommendations: noDisplay
exl-id: f087d9f2-cce9-4903-977f-3c5b47522c06
source-git-commit: 57dbf456625d22cd2e4526d92e5a8c20a048d339
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 2%

---

# Passaggio 1 - Creazione [!DNL Android] App e configurazione da utilizzare [!DNL Firebase Cloud Messaging]

In questa parte creerai [!DNL Android] App da ricevere [!UICONTROL Push notifications] inviato da Adobe Campaign Standard. Per ricevere le notifiche push, l’app deve essere registrata con Google [!DNL Firebase Cloud Service].

1. Accedi al tuo [!DNL Firebase] conto.

   [!DNL Firebase] è una piattaforma mobile Google che ti aiuta a sviluppare rapidamente app di alta qualità. Se non hai una [!DNL Firebase] account, creane uno [da qui](https://firebase.google.com).

2. Launch [!DNL Android Studio]
3. Fai clic su **[!UICONTROL File]** > **[!UICONTROL New]** > **[!UICONTROL New Project].**
4. Seleziona **[!UICONTROL Empty Activity]** e fai clic su **[!UICONTROL Next].**

   ![progetto android](assets/android-project.PNG)

5. Fornisci un nome significativo al progetto.

   Ai fini di questa demo abbiamo nominato il nostro progetto come *[!DNL ACSPushTutorial]*

   ![android-project-configuration](assets/android-project-configuration.PNG)

6. Accetta i nomi dei pacchetti predefiniti e fai clic su **[!DNL Finish]** per creare il progetto.
7. La struttura del progetto deve avere un aspetto simile alla schermata sottostante

   ![android-project-structure](assets/android-project-structure.PNG)

8. Fai clic su **[!UICONTROL Tools]** > **[!UICONTROL Firebase].** (viene aggiunto il progetto a [!DNL Firebase])
9. Fai clic su **[!UICONTROL Set up Firebase Cloud Messaging].**

   ![imposta firebase](assets/android-project-firebase-messaging.PNG)

10. Fai clic su **[!UICONTROL Connect to Firebase].**
11. Una volta che l’app è stata connessa a Firebase, fai clic su **[!UICONTROL Add FCM to your app].**
12. Fai clic su **[!UICONTROL Accept Changes].**

   Quando aggiungi FCM all’app, la procedura guidata richiede l’autorizzazione per apportare alcune modifiche al progetto.

   ![[!DNL add-fcm-to-your-app]](assets/firebase-add-fcm-to-app.PNG)

Una volta completata con successo l’app con Firebase, riceverai un messaggio come quello mostrato di seguito:

![[!DNL fcm-successfull]](assets/android-firebase-success.PNG)

[Accertati che il progetto sia elencato in [!DNL Firebase ]console](https://console.firebase.google.com/)

## Configura [!UICONTROL Push Channel] Impostazioni

1. Accedi a [!DNL Firebase] console
2. Apri **[!UICONTROL ACSPushTutorial]** progetto.
3. Fai clic sul pulsante **icona ingranaggio** e apri le impostazioni del progetto

   ![impostazioni progetto](assets/firebase-project-settings.PNG)

4. Passa alla scheda **[!UICONTROL Cloud Messaging]** scheda .
5. Copia la chiave server

   ![chiave server](assets/firebase-server-key.PNG)

6. Accedi alla tua istanza Adobe Campaign Standard
7. Fai clic su **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile App].**
8. Selezionare il **[!UICONTROL Mobile Application Property].**
9. Fai clic sul pulsante **[!DNL Android]icona** in **[!UICONTROL Push Channel settings]** sezione .
10. Incolla la chiave server nel campo chiave server .

Se tutto va bene dovresti vedere un messaggio SUCCESS.

![impostazioni dei canali push](assets/push-channel-settings.PNG)

Per riassumere, abbiamo creato un [!DNL Android App] e collegato [!DNL Android App] con [!DNL Firebase]. Abbiamo quindi connesso l’app mobile in Adobe Campaign con [!DNL Android App] incollando il [!DNL Android] Chiave server dell’app in all’app mobile in Adobe Campaign Standard.
