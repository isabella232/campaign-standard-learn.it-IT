---
title: Introduzione ai messaggi in-app
description: Il canale di messaggistica in-app  Adobe Campaign Standard (ACS) consente di presentare all'utente messaggi in-app pertinenti in base al contesto in risposta al comportamento in tempo reale di un cliente all'interno dell'applicazione mobile.
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
ht-degree: 19%

---


# Introduzione ai [!UICONTROL In-App] messaggi {#introduction}

Il [!UICONTROL In-App Messaging] canale consente di visualizzare un messaggio quando l&#39;utente è attivo all&#39;interno dell&#39;applicazione mobile. Questo canale richiede l&#39;integrazione delle applicazioni mobili con [!UICONTROL Adobe Experience Platform SDK].

Questa esercitazione spiega i passaggi necessari per impostare le proprietà mobili, l&#39; [!UICONTROL Launch] estensione per il [!UICONTROL In-App Messaging] canale, nonché come preparare, personalizzare e inviare [!UICONTROL In-App] messaggi in  Adobe Campaign Standard. I collegamenti consentono di seguire le esercitazioni video su ciascuno degli argomenti evidenziati.

## Prerequisiti {#prerequisites}

1. Make sure you can access the **[!UICONTROL In-App]** channel. Se non riesci ad accedere a questi canali, contatta il team dell’account.
1. Verify that your **user** has the necessary **permissions** in Adobe Campaign Standard and [!UICONTROL Launch].

   1. In  Adobe Campaign Standard, accertatevi che l&#39;utente IMS sia parte dei [!UICONTROL Standard User] gruppi e [!UICONTROL Administrator] .\
      Questo passaggio consente all&#39;utente di accedere a  Adobe Campaign Standard, passare alla pagina dell&#39;app mobile SDK del Experience Platform  e visualizzare le proprietà dell&#39;app mobile creata in [!UICONTROL Launch].
   1. In [!UICONTROL Launch], accertatevi che l&#39;utente IMS faccia parte di un profilo di [!UICONTROL Launch] prodotto.\
      Questo passaggio consente all&#39;utente di accedere [!UICONTROL Launch] per creare e visualizzare le proprietà. Per ulteriori informazioni sui profili di prodotto in [!UICONTROL Launch], consulta [Creazione del profilo](https://docs.adobelaunch.com/launch-reference/administration/user-permissions#3-create-your-product-profile)di prodotto. Nel profilo di prodotto non dovrebbero essere impostate autorizzazioni per la società o le proprietà, ma l&#39;utente dovrebbe essere ancora in grado di effettuare l&#39;accesso.

1. In  Adobe Experience Platform Launch:

   1. Crea l’applicazione mobile creando una proprietà mobile e strumenti la tua app mobile con  Experience Platform SDK.
   1. Installate l’estensione **Adobe Campaign Standard** per l’applicazione mobile.

Per ulteriori informazioni sulle estensioni, consulta [Configurare l’estensione Campaign Standard in  lancio](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard) Adobe nella [!UICONTROL Adobe Launch ]documentazione.

## Passaggi per impostare [!UICONTROL In-App] i messaggi {#steps-to-set-up}

1. [Configurare un’applicazione mobile utilizzando Adobe Experience Platform SDK](/help/communication-channels/mobile/configure-mobile-apps-using-aep-sdk.md).

1. [Configurare gli eventi](/help/communication-channels/mobile/in-app/configure-events.md).

## Creazione, gestione e pubblicazione di [!UICONTROL In-App] consegne {#create-manage-publish}

Potete creare consegne in-app una sola volta facendo clic sulla **[!UICONTROL Create an In-App Message]** scheda dalla homepage, dalla pagina [!UICONTROL Marketing Activities], oppure potete [creare una distribuzione in-app all&#39;interno di un flusso di lavoro](/help/communication-channels/mobile/in-app/in-app-activity.md).

Quando configurate la consegna, potete scegliere tra tre opzioni per eseguire il targeting degli utenti, in base a diversi modelli di consegna:

1. [**Trasmettete un messaggio **](/help/communication-channels/mobile/in-app/broadcast-in-app-message.md)in-app per indirizzare tutti gli utenti di un&#39;app mobile.

   questo tipo di messaggio ti consente di inviare messaggi a tutti gli utenti (correnti o futuri) della tua app mobile anche se non dispongono di un profilo esistente in Adobe Campaign. La personalizzazione non è pertanto possibile quando si personalizzano i messaggi in quanto il profilo utente non esiste necessariamente in  Adobe Campaign.

1. Esegue il targeting di tutti gli utenti in base al loro profilo dell&#39;app mobile.

   questo tipo di messaggio ti consente di eseguire il targeting per tutti gli utenti noti o anonimi di un’app mobile con un profilo mobile in Adobe Campaign. Questo tipo di messaggi può essere personalizzato utilizzando solo attributi non personali e non riservati e non richiede un handshake sicuro tra l’SDK di mobile e il servizio di messaggistica in-app di Adobe Campaign. Quindi, la strategia di personalizzazione si basa su ciò che hai imparato sugli utenti dalla loro interazione con il dispositivo. Ad esempio, eseguite il targeting per tutti gli utenti che hanno avviato l&#39;app più di 5 volte nell&#39;ultima settimana.

1. [**Esegue il targeting degli utenti in base al profilo **](/help/communication-channels/mobile/in-app/target-users-based-on-campaign-profile.md)Campaign.

   questo tipo di messaggio ti consente di eseguire il targeting dei profili Adobe Campaign (profili di gestione delle relazioni con i clienti) che sono abbonati alla tua app mobile. Il messaggio può essere personalizzato con tutti gli attributi di profilo disponibili in  Adobe Campaign, ma richiede una stretta di mano sicura tra l&#39;SDK di Mobile e il servizio di messaggistica in-app di Campaign per garantire che i messaggi con informazioni personali e riservate siano utilizzati solo da utenti autorizzati.

Questo modello è utile per supportare i casi di utilizzo di orchestrazione tra canali, nei quali hai già eseguito il targeting degli utenti su altri canali come E-mail o Push e in base alla loro risposta, vuoi interagire con loro con un messaggio in-app.

## Report sulle consegne in-app {#report}

Una volta pubblicata la consegna, potete [generare rapporti sulla consegna](/help/communication-channels/mobile/in-app/in-app-reporting.md)in-app.

## Risorse aggiuntive

* [Rapporto in-app](https://docs.adobe.com/content/help/en/campaign-standard/using/reporting/list-of-reports/in-app-report.html)
* [Impostazione di una proprietà mobile](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property)
* [Configurazione di un’applicazione mobile mediante gli SDK Adobe Experience Platform](https://docs.adobe.com/content/help/it-IT/campaign-standard/using/administrating/configuring-channels/configuring-a-mobile-application.html)
* [Preparazione e invio di un messaggio in-app](https://docs.adobe.com/content/help/en/campaign-standard/using/communication-channels/in-app-messaging/preparing-and-sending-an-in-app-message.html)
* [Personalizzazione di un messaggio in-app](https://docs.adobe.com/content/help/en/campaign-standard/using/communication-channels/in-app-messaging/customizing-an-in-app-message.html)
* [Invio di un messaggio in-app all’interno di un flusso di lavoro](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/channel-activities/in-app-delivery.html)
* [Abilita metriche del ciclo di vita](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
