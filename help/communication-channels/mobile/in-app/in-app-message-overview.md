---
title: Introduzione ai messaggi in-app
description: Il canale di messaggistica in-app del Adobe Campaign Standard  (ACS) consente di presentare all'utente messaggi in-app pertinenti in base al contesto in risposta al comportamento in tempo reale di un cliente all'interno dell'applicazione mobile.
feature: In-App
topics: Mobile
kt: 1911
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 82fb2d39dc61a55c0aa20ca1fa215f35a7dd9088
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 1%

---


# Introduzione ai [!UICONTROL In-App] messaggi {#introduction}

Il [!UICONTROL In-App Messaging] canale consente di visualizzare un messaggio quando l&#39;utente è attivo all&#39;interno dell&#39;applicazione mobile. Questo canale richiede l&#39;integrazione delle applicazioni mobili con [!UICONTROL Adobe Experience Platform SDK].

Questa esercitazione spiega i passaggi necessari per impostare le proprietà mobili, l&#39; [!UICONTROL Launch] estensione per il [!UICONTROL In-App Messaging] canale, nonché come preparare, personalizzare e inviare [!UICONTROL In-App] messaggi in  Adobe Campaign Standard. I collegamenti consentono di seguire le esercitazioni video su ciascuno degli argomenti evidenziati.

## Prerequisiti {#prerequisites}

1. Assicuratevi di poter accedere al **[!UICONTROL In-App]** canale. Se non riuscite ad accedere a questi canali, contattate il team di account.
1. Verificate che l&#39; **utente** disponga delle **autorizzazioni** necessarie in  Adobe Campaign Standard e [!UICONTROL Launch].

   1. In  Adobe Campaign Standard, accertatevi che l&#39;utente IMS sia parte dei [!UICONTROL Standard User] gruppi e [!UICONTROL Administrator] .\
      Questo passaggio consente all&#39;utente di accedere  Adobe Campaign Standard, passare alla pagina dell&#39;app mobile SDK del Experience Platform  e visualizzare le proprietà dell&#39;app mobile creata in [!UICONTROL Launch].
   1. In [!UICONTROL Launch], accertatevi che l&#39;utente IMS faccia parte di un profilo di [!UICONTROL Launch] prodotto.\
      Questo passaggio consente all&#39;utente di accedere [!UICONTROL Launch] per creare e visualizzare le proprietà. Per ulteriori informazioni sui profili di prodotto in [!UICONTROL Launch], consulta [Creazione del profilo](https://docs.adobelaunch.com/launch-reference/administration/user-permissions#3-create-your-product-profile)di prodotto. Nel profilo di prodotto non dovrebbero essere impostate autorizzazioni per la società o le proprietà, ma l&#39;utente dovrebbe essere ancora in grado di effettuare l&#39;accesso.

1. In  Adobe Experience Platform Launch:

   1. Crea l’applicazione mobile creando una proprietà mobile e strumenti la tua app mobile con  Experience Platform SDK.
   1. Installate l’estensione **Adobe Campaign Standard** per l’applicazione mobile.

Per ulteriori informazioni sulle estensioni, consulta [Configurare l’estensione Campaign Standard in  lancio](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard) Adobe nella [!UICONTROL Adobe Launch ]documentazione.

## Passaggi per impostare [!UICONTROL In-App] i messaggi {#steps-to-set-up}

1. [Configura un’applicazione mobile utilizzando  SDK](/help/communication-channels/mobile/configure-mobile-apps-using-aep-sdk.md)per Adobi Experience Platform.

1. [Configurare gli eventi](/help/communication-channels/mobile/in-app/configure-events.md).

## Creazione, gestione e pubblicazione di [!UICONTROL In-App] consegne {#create-manage-publish}

Potete creare consegne in-app una sola volta facendo clic sulla **[!UICONTROL Create an In-App Message]** scheda dalla homepage, dalla pagina [!UICONTROL Marketing Activities], oppure potete [creare una distribuzione in-app all&#39;interno di un flusso di lavoro](/help/communication-channels/mobile/in-app/in-app-activity.md).

Quando configurate la consegna, potete scegliere tra tre opzioni per eseguire il targeting degli utenti, in base a diversi modelli di consegna:

1. [**Trasmettete un messaggio **](/help/communication-channels/mobile/in-app/broadcast-in-app-message.md)in-app per indirizzare tutti gli utenti di un&#39;app mobile.

   Questo tipo di messaggio consente di inviare messaggi a tutti gli utenti (correnti o futuri) dell’applicazione mobile anche se non dispongono di un profilo esistente nel  Adobe Campaign. La personalizzazione non è quindi possibile quando si personalizzano i messaggi in quanto il profilo utente non esiste necessariamente nel  Adobe Campaign.

1. Target tutti gli utenti in base al loro profilo app mobile.

   Questo tipo di messaggio consente di eseguire il targeting di tutti gli utenti noti o anonimi di un&#39;app mobile con un profilo mobile  Adobe Campaign. Questo tipo di messaggi può essere personalizzato utilizzando solo attributi non personali e non sensibili e non richiede un handshake protetto tra Mobile SDK e  Adobe Campaign  servizio di messaggistica in-app. Quindi, la strategia di personalizzazione si basa su ciò che hai imparato sugli utenti dalla loro interazione con il dispositivo. Ad esempio, eseguite il targeting per tutti gli utenti che hanno avviato l&#39;app più di 5 volte nell&#39;ultima settimana.

1. [**Utenti Target in base al profilo **](/help/communication-channels/mobile/in-app/target-users-based-on-campaign-profile.md)Campaign.

   Questo tipo di messaggio consente di eseguire il targeting  profili di Adobe Campaign (profili CRM) che hanno effettuato l&#39;iscrizione all&#39;applicazione mobile. Il messaggio può essere personalizzato con tutti gli attributi di profilo disponibili nel  Adobe Campaign, ma richiede una stretta di mano sicura tra l&#39;SDK di Mobile e il servizio di messaggistica in-app di Campaign per garantire che i messaggi con informazioni personali e riservate siano utilizzati solo dagli utenti autorizzati.

Questo modello è utile per supportare i casi di utilizzo di orchestrazione tra canali, nei quali hai già eseguito il targeting degli utenti su altri canali come E-mail o Push e in base alla loro risposta, vuoi interagire con loro con un messaggio in-app.

## Report sulle consegne in-app {#report}

Una volta pubblicata la consegna, potete [generare rapporti sulla consegna](/help/communication-channels/mobile/in-app/in-app-reporting.md)in-app.

## Risorse aggiuntive

* [Rapporto in-app](https://docs.adobe.com/content/help/en/campaign-standard/using/reporting/list-of-reports/in-app-report.html)
* [Impostazione di una proprietà mobile](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property)
* [Configurazione di un’applicazione mobile mediante  SDK per Adobi Experience Platform](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html)
* [Preparazione e invio di un messaggio in-app](https://docs.adobe.com/content/help/en/campaign-standard/using/communication-channels/in-app-messaging/preparing-and-sending-an-in-app-message.html)
* [Personalizzazione di un messaggio in-app](https://docs.adobe.com/content/help/en/campaign-standard/using/communication-channels/in-app-messaging/customizing-an-in-app-message.html)
* [Invio di un messaggio in-app in un flusso di lavoro](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/channel-activities/in-app-delivery.html)
* [Abilita metriche del ciclo di vita](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
