---
title: 'Passaggio 1: creazione di un’app Android e configurazione per l’utilizzo di Firebase Cloud Messaging'
description: In questa parte verranno creati [!DNL Android] App da ricevere [!UICONTROL Push notifications] inviato da Adobe Campaign Standard. Per ricevere le notifiche push, l’app deve essere registrata con Google [!DNL Firebase Cloud Service].
feature: Push
user: Admin
level: Experienced
jira: KT-4825
doc-type: tutorial
activity: use
team: TM
recommendations: noDisplay
exl-id: f087d9f2-cce9-4903-977f-3c5b47522c06
source-git-commit: 0ad82fb0533ed8fc2a85c2a32c7e54deef14d05a
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 3%

---

# Passaggio 1: creazione [!DNL Android] App e configurazione per l’utilizzo [!DNL Firebase Cloud Messaging]

In questa parte verranno creati [!DNL Android] App da ricevere [!UICONTROL Push notifications] inviato da Adobe Campaign Standard. Per ricevere le notifiche push, l’app deve essere registrata con Google [!DNL Firebase Cloud Service].

1. Accedi al tuo [!DNL Firebase] account.

   [!DNL Firebase] è la piattaforma mobile di Google che consente di sviluppare rapidamente app di alta qualità. Se non si dispone di [!DNL Firebase] account, creane uno [da qui](https://firebase.google.com).

2. Launch [!DNL Android Studio]
3. Clic **[!UICONTROL File]** > **[!UICONTROL New]** > **[!UICONTROL New Project].**
4. Seleziona **[!UICONTROL Empty Activity]** e fai clic su **[!UICONTROL Next].**

   ![progetto android](assets/android-project.PNG)

5. Specifica un nome significativo per il progetto.

   Ai fini di questa demo abbiamo denominato il nostro progetto come *[!DNL ACSPushTutorial]*

   ![android-project-configuration](assets/android-project-configuration.PNG)

6. Accettare i nomi dei pacchetti predefiniti e fare clic su **[!DNL Finish]** per creare il progetto.
7. La struttura del progetto deve essere simile alla schermata seguente

   ![android-project-structure](assets/android-project-structure.PNG)

8. Fai clic su **[!UICONTROL Tools]** > **[!UICONTROL Firebase].** (il progetto viene aggiunto a [!DNL Firebase])
9. Fai clic su **[!UICONTROL Set up Firebase Cloud Messaging].**

   ![configurare firebase](assets/android-project-firebase-messaging.PNG)

10. Fai clic su **[!UICONTROL Connect to Firebase].**
11. Dopo aver connesso l’app a Firebase, fai clic su **[!UICONTROL Add FCM to your app].**
12. Fai clic su **[!UICONTROL Accept Changes].**

   Quando aggiungi FCM all’app, la procedura guidata richiede l’autorizzazione per apportare alcune modifiche al progetto.

   ![[!DNL add-fcm-to-your-app]](assets/firebase-add-fcm-to-app.PNG)

Una volta completata l’integrazione dell’app con Firebase, dovresti ricevere un messaggio simile a quello mostrato di seguito:

![[!DNL fcm-successfull]](assets/android-firebase-success.PNG)

[Assicurati che il progetto sia elencato in [!DNL Firebase ]console](https://console.firebase.google.com/)

## Configura [!UICONTROL Push Channel] Impostazioni

1. Accedi a [!DNL Firebase] console
2. Apri **[!UICONTROL ACSPushTutorial]** progetto.
3. Fai clic su **icona ingranaggio** e apri le impostazioni del progetto

   ![project-settings](assets/firebase-project-settings.PNG)

4. Passa alla scheda **[!UICONTROL Cloud Messaging]** scheda.
5. Copia la chiave del server

   ![chiave server](assets/firebase-server-key.PNG)

6. Accedi all’istanza di Adobe Campaign Standard
7. Clic **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile App].**
8. Seleziona la scheda appropriata **[!UICONTROL Mobile Application Property].**
9. Fai clic su **[!DNL Android]icona** nel **[!UICONTROL Push Channel settings]** sezione.
10. Incolla la chiave del server nel campo chiave del server.

Se tutto va bene, dovresti visualizzare un messaggio di SUCCESSO.

![push-channel-settings](assets/push-channel-settings.PNG)

Per riepilogare, è stata creata una [!DNL Android App] e ha collegato [!DNL Android App] con [!DNL Firebase]. Abbiamo quindi collegato l’app mobile in Adobe Campaign con [!DNL Android App] incollando [!DNL Android] Chiave server dell’app nell’app mobile in Adobe Campaign Standard.
