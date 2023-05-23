---
title: Introduzione ai messaggi in-app
description: Scopri come presentare all’utente messaggi in-app contestualmente rilevanti in risposta al comportamento in tempo reale di un cliente all’interno dell’app mobile.
feature: In App
kt: 1911
doc-type: feature video
activity: use
team: TM
exl-id: c51716eb-7239-4fc0-9ccf-9f5f0a5fae65
role: User
level: Beginner
source-git-commit: 57dbf456625d22cd2e4526d92e5a8c20a048d339
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 21%

---

# Introduzione a [!UICONTROL In-App] messaggi {#introduction}

Il [!UICONTROL In-App Messaging] canale consente di visualizzare un messaggio quando l’utente è attivo all’interno dell’app mobile. Questo canale richiede l’integrazione di applicazioni mobili con [!UICONTROL Adobe Experience Platform SDK].

Questo tutorial spiega i passaggi necessari per configurare le proprietà mobili, [!UICONTROL Launch] estensione per [!UICONTROL In-App Messaging] e come preparare, personalizzare e inviare [!UICONTROL In-App] messaggi in Adobe Campaign Standard. I collegamenti conducono alle esercitazioni video su ciascuno degli argomenti evidenziati.

## Prerequisiti {#prerequisites}

1. Assicurati di poter accedere al **[!UICONTROL In-App]** canale. Se non riesci ad accedere a questi canali, contatta il team dell’account.
1. Verifica che **utente** ha il necessario **autorizzazioni** in Adobe Campaign Standard e [!UICONTROL Launch].

   1. In Adobe Campaign Standard, assicurati che l’utente IMS faccia parte del [!UICONTROL Standard User] e [!UICONTROL Administrator] gruppi.

      Questo passaggio consente all’utente di accedere ad Adobe Campaign Standard, passare alla pagina dell’app mobile SDK di Experience Platform e visualizzare le proprietà dell’app mobile creata in [!UICONTROL Launch].

   1. In entrata [!UICONTROL Launch], assicurati che l’utente IMS faccia parte di un [!UICONTROL Launch] profilo di prodotto. Questo passaggio consente all’utente di accedere a [!UICONTROL Launch] per creare e visualizzare le proprietà. Nel profilo prodotto non dovrebbero essere impostate autorizzazioni per l’azienda o le proprietà, ma l’utente dovrebbe essere comunque in grado di accedere.

1. In Adobe Experience Platform Launch:

   1. Crea l’app mobile creando una proprietà mobile e dota l’app mobile di uno strumento con l’SDK Experience Platform.
   1. Installare **Adobe Campaign Standard** per la tua app mobile.

Per ulteriori informazioni sulle estensioni, consulta [Configurare l’estensione Campaign Standard in Adobe Launch](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard) nella documentazione di.

## Passaggi per impostare [!UICONTROL In-App] messaggi {#steps-to-set-up}

1. [Configurare un’app mobile mediante l’SDK di Adobe Experience Platform](/help/communication-channels/mobile/configure-mobile-apps-using-aep-sdk.md).
1. [Configurare gli eventi](/help/communication-channels/mobile/in-app/configure-events.md).

## Creare, gestire e pubblicare [!UICONTROL In-App] Consegne {#create-manage-publish}

Puoi creare consegne in-app una tantum facendo clic sul pulsante **[!UICONTROL Create an In-App Message]** dalla home page, dalla scheda [!UICONTROL Marketing Activities], oppure puoi [Creare una consegna in-app all’interno di un flusso di lavoro](/help/communication-channels/mobile/in-app/in-app-activity.md).

Durante l’impostazione della consegna, puoi scegliere tra diversi modelli di consegna per eseguire il targeting dei tuoi utenti:

1. [**Trasmettere un messaggio in-app**](/help/communication-channels/mobile/in-app/broadcast-in-app-message.md) per eseguire il targeting per tutti gli utenti di un’app mobile.

   questo tipo di messaggio ti consente di inviare messaggi a tutti gli utenti (correnti o futuri) della tua app mobile anche se non dispongono di un profilo esistente in Adobe Campaign. La personalizzazione non è quindi possibile quando si personalizzano i messaggi in quanto il profilo utente non esiste necessariamente in Adobe Campaign.

1. Puoi indirizzare l’attività a tutti gli utenti in base al loro profilo di app mobile.

   questo tipo di messaggio ti consente di eseguire il targeting per tutti gli utenti noti o anonimi di un’app mobile con un profilo mobile in Adobe Campaign. Questo tipo di messaggi può essere personalizzato utilizzando solo attributi non personali e non riservati e non richiede un handshake sicuro tra l’SDK di mobile e il servizio di messaggistica in-app di Adobe Campaign. Quindi, la strategia di personalizzazione si basa su ciò che hai imparato sugli utenti dalla loro interazione con il dispositivo. Ad esempio, esegui il targeting di tutti gli utenti che hanno avviato la loro app più di cinque volte nell’ultima settimana.

1. [**Eseguire il targeting degli utenti in base al loro profilo Campaign**](/help/communication-channels/mobile/in-app/target-users-based-on-campaign-profile.md).

   questo tipo di messaggio ti consente di eseguire il targeting dei profili Adobe Campaign (profili di gestione delle relazioni con i clienti) che sono abbonati alla tua app mobile. Il messaggio può essere personalizzato con tutti gli attributi di profilo disponibili in Adobe Campaign. Richiede un handshake sicuro tra l’SDK di Mobile e il servizio di messaggistica in-app di Campaign per garantire che i messaggi con informazioni personali e riservate siano utilizzati solo da utenti autorizzati.

Questo modello è utile per supportare casi di utilizzo di orchestrazione cross-channel, in cui hai già eseguito il targeting degli utenti su altri canali come e-mail o push. In base alla loro risposta, desideri quindi coinvolgerli con un messaggio in-app.

## Generare rapporti sulle consegne in-app {#report}

Una volta pubblicata la consegna, puoi [creare rapporti sulla consegna in-app](/help/communication-channels/mobile/in-app/in-app-reporting.md).
