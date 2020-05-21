---
title: Informazioni sul connettore dati Adobe Experience Platform
description: Adobe Experience Platform Data Connector aiuta i clienti esistenti a rendere disponibili i loro dati su Adobe Experience Platform mappando i dati XTK (i dati acquisiti in Campaign) su dati XDM (Experience Data Model) in Adobe Experience Platform.
feature: Adobe Experience Platform Data Connector
topics: ACoP
kt: 2826
doc-type: feature video
activity: understand
team: TM
translation-type: tm+mt
source-git-commit: cb5d5bc58137fd374eafe165c6ea13288a60d7db
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 4%

---


# Informazioni su Adobe Experience Platform [!UICONTROL Data Connector]

>[!NOTE]
>
>Questa funzionalità è attualmente in versione beta e soggetta a frequenti aggiornamenti e modifiche senza preavviso.
>Per [!UICONTROL Adobe Customer Support] implementare questa funzionalità, contattate il vostro riferimento commerciale.

## Panoramica

Adobe Experience Platform [!UICONTROL Data Connector] aiuta i clienti esistenti a rendere disponibili i loro dati su Adobe Experience Platform mappando i dati XTK (i dati acquisiti in Adobe Campaign) su dati [!DNL Experience Data Model] (XDM) su Adobe Experience Platform.

Il connettore è unidirezionale e invia i dati da Adobe Campaign Standard ad Adobe Experience Platform. I dati non vengono mai inviati da Adobe Experience Platform ad Adobe Campaign Standard.

Adobe Experience Platform [!UICONTROL Data Connector] è destinato ai data engineering che comprendono Adobe Campaign Standard [!UICONTROL custom resources] e che comprendono in che modo lo schema di dati complessivo del cliente dovrebbe essere all&#39;interno di Adobe Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12)

*Questo video offre una panoramica di Adobe Experience Platform[!UICONTROL Data Connector](09:35 min)*

>[!NOTE]
>
>Il trasferimento out-of-the-box non [!UICONTROL subscription events] è supportato. Per trasferire [!UICONTROL subscription events], puoi creare XDM e dataset corrispondenti in Adobe Experience Platform, quindi configurare una mappatura dati personalizzata per questi dati.
>Gli elementi esistenti [!UICONTROL experience events] non possono essere trasferiti in Adobe Experience Platform, ma quelli generati in corso [!UICONTROL experience events] verranno trasmessi in streaming ad Adobe Experience Platform.

## Passaggi chiave per eseguire una mappatura dati

Le seguenti esercitazioni descrivono i passaggi chiave per eseguire una mappatura dei dati tra Campaign Standard e Adobe Experience Platform:

1. [Mappatura delle risorse personalizzate](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [Mapping di eventi esperienza](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [Mappatura dei dati della tabella dei semi](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [Modifica della mappatura dei dati](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [Verifica dello stato di un processo di assimilazione dei dati](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

## Risorse aggiuntive

* [Informazioni su Adobe Experience Platform Data Connector](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-about-data-connector.html)
* [Panoramica di Experience Data Model](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-data-model-overview.html)
* [Definizione mappature](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-definition.html)
* [Attivazione mappature](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-activation.html)
* [Attivazione dell’assimilazione dei dati tramite API](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-triggering-data-ingestion.html)
