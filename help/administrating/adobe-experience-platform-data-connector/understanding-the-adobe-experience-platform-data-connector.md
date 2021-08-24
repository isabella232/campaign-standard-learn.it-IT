---
title: Comprendere il connettore dati Adobe Experience Platform
description: Adobe Experience Platform Data Connector aiuta i clienti esistenti a rendere i loro dati disponibili su Adobe Experience Platform mappando i dati XTK (dati acquisiti in Campaign) su Experience Data Model (XDM) su Adobe Experience Platform.
feature: Integrazione del servizio core People
kt: 2826
thumbnail: 27304.jpg
doc-type: feature video
activity: understand
team: TM
exl-id: 686961f9-5374-4cc6-8b36-7ee0584ea720
source-git-commit: 2ba22e7e7d193278fd06cb4b2dc80f650f754ec8
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 4%

---

# Comprendere Adobe Experience Platform [!UICONTROL Data Connector]

>[!NOTE]
>
>Questa funzionalità è in versione beta e soggetta a frequenti aggiornamenti e modifiche senza preavviso.
>
>Per implementare questa funzionalità, contatta [!UICONTROL Adobe Customer Support] .

## Panoramica

Adobe Experience Platform [!UICONTROL Data Connector] aiuta i clienti esistenti a rendere i loro dati disponibili su Adobe Experience Platform mappando i dati XTK (dati acquisiti in Adobe Campaign) su [!DNL Experience Data Model] (XDM) su Adobe Experience Platform.

Il connettore è unidirezionale e invia i dati da Adobe Campaign Standard a Adobe Experience Platform. I dati non vengono mai inviati da Adobe Experience Platform ad Adobe Campaign Standard.

Adobe Experience Platform [!UICONTROL Data Connector] è destinato ai data engineer che conoscono Adobe Campaign Standard [!UICONTROL custom resources] e conoscono lo schema generale dei dati del cliente all&#39;interno di Adobe Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12)

*Questo video offre una panoramica del Adobe Experience Platform  [!UICONTROL Data Connector] (09:35 min)*

>[!NOTE]
>
>Il trasferimento predefinito di [!UICONTROL subscription events] non è supportato. Per trasferire [!UICONTROL subscription events], puoi creare XDM e set di dati corrispondenti in Adobe Experience Platform, quindi configurare una mappatura dati personalizzata per questi dati.
>
>Impossibile acquisire [!UICONTROL experience events] esistente in Adobe Experience Platform, ma i [!UICONTROL experience events] generati in corso vengono inviati in streaming a Adobe Experience Platform.

## Passaggi chiave per eseguire una mappatura dei dati

Le seguenti esercitazioni descrivono i passaggi chiave per eseguire una mappatura dei dati tra Campaign Standard e Adobe Experience Platform:

1. [Mappatura di risorse personalizzate](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [Mappatura di eventi Experience](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [Mappatura dei dati della tabella di seed](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [Modifica della mappatura dei dati](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [Controllare lo stato di un processo di inserimento dei dati](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

## Risorse aggiuntive

* [Informazioni sul Connettore dati di Adobe Experience Platform](https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/adobe-experience-platform/data-connector/aep-about-data-connector.html)

