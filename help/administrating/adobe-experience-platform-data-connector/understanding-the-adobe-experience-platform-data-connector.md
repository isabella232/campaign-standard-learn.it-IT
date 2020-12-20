---
title: Informazioni su Adobe Experience Platform Data Connector
description: Adobe Experience Platform Data Connector aiuta i clienti esistenti a rendere disponibili i loro dati su Adobe Experience Platform mappando i dati XTK (dati acquisiti in Campaign) a dati XDM (Experience Data Model) su Adobe Experience Platform.
feature: Adobe Experience Platform Data Connector
topics: ACoP
kt: 2826
thumbnail: 27304.jpg
doc-type: feature video
activity: understand
team: TM
translation-type: tm+mt
source-git-commit: 11263e247184ddc6a8e3df6a8ed0899907fbb366
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 10%

---


# Informazioni sull&#39;Adobe Experience Platform [!UICONTROL Data Connector]

>[!NOTE]
>
>Questa funzionalità è attualmente in versione beta e soggetta a frequenti aggiornamenti e modifiche senza preavviso.
>
>Per implementare questa funzionalità, contattate [!UICONTROL Adobe Customer Support].

## Panoramica

Adobe Experience Platform [!UICONTROL Data Connector] aiuta i clienti esistenti a rendere disponibili i propri dati su Adobe Experience Platform mappando i dati XTK (i dati acquisiti  Adobe Campaign) su [!DNL Experience Data Model] (XDM) dati su Adobe Experience Platform.

Il connettore è unidirezionale e invia i dati da  Adobe Campaign Standard ad Adobe Experience Platform. I dati non vengono mai inviati dall&#39;Adobe Experience Platform a  Adobe Campaign Standard.

Adobe Experience Platform [!UICONTROL Data Connector] è destinato agli sviluppatori di dati che comprendono  Adobe Campaign Standard [!UICONTROL custom resources] e che hanno un&#39;idea di come lo schema di dati complessivo del cliente dovrebbe essere all&#39;interno di Adobe Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12)

*Questo video offre una panoramica sull&#39;Adobe Experience Platform  [!UICONTROL Data Connector] (09:35 min)*

>[!NOTE]
>
>Il trasferimento out-of-the-box di [!UICONTROL subscription events] non è supportato. Per trasferire [!UICONTROL subscription events], è possibile creare XDM e dataset corrispondenti in Adobe Experience Platform, quindi configurare una mappatura dati personalizzata per questi dati.
>
>Impossibile assimilare [!UICONTROL experience events] esistente in Adobe Experience Platform, ma [!UICONTROL experience events] generato in corso verrà trasmesso in streaming ad Adobe Experience Platform.

## Passaggi chiave per eseguire una mappatura dati

Le seguenti esercitazioni descrivono i passaggi chiave per eseguire una mappatura dati tra Campaign Standard e Adobe Experience Platform:

1. [Mappatura delle risorse personalizzate](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [Mappatura di eventi Experience](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [Mappatura dei dati della tabella dei semi](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [Modifica della mappatura dei dati](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [Verifica dello stato di un processo di inserimento dei dati](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

## Risorse aggiuntive

* [Informazioni sul Connettore dati di Adobe Experience Platform](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-about-data-connector.html)
* [Panoramica di Experience Data Model](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-data-model-overview.html)
* [Definizione mappature](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-definition.html)
* [Attivazione mappature](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-activation.html)
* [Attivazione dell’acquisizione dati tramite API](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-triggering-data-ingestion.html)
