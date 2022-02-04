---
title: Comprendere il connettore dati Adobe Experience Platform
description: Adobe Experience Platform Data Connector aiuta i clienti esistenti a rendere i loro dati disponibili su Adobe Experience Platform mappando i dati XTK (dati acquisiti in Campaign) su Experience Data Model (XDM) su Adobe Experience Platform.
feature: People Core Service Integration
kt: 2826
thumbnail: 27304.jpg
doc-type: feature video
activity: understand
team: TM
exl-id: 686961f9-5374-4cc6-8b36-7ee0584ea720
source-git-commit: cccc2cd4141d4da4d06132af8bab3f15f7ecc853
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Comprendere Adobe Experience Platform [!UICONTROL Data Connector]

>[!NOTE]
>
>Questa funzionalità è in versione beta e soggetta a frequenti aggiornamenti e modifiche senza preavviso.
>
>Rivolgiti a [!UICONTROL Adobe Customer Support] se prevedi di implementare questa funzionalità.

## Panoramica

Adobe Experience Platform [!UICONTROL Data Connector] aiuta i clienti esistenti a rendere i loro dati disponibili su Adobe Experience Platform mappando i dati XTK (dati acquisiti in Adobe Campaign) in [!DNL Experience Data Model] (XDM) dati su Adobe Experience Platform.

Il connettore è unidirezionale e invia i dati da Adobe Campaign Standard a Adobe Experience Platform. I dati non vengono mai inviati da Adobe Experience Platform ad Adobe Campaign Standard.

Adobe Experience Platform [!UICONTROL Data Connector] è destinato agli ingegneri di dati che conoscono Adobe Campaign Standard [!UICONTROL custom resources] e scopri in che modo lo schema dei dati generali del cliente dovrebbe essere all’interno di Adobe Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12)

*Questo video offre una panoramica di Adobe Experience Platform [!UICONTROL Data Connector] (09:35 min)*

>[!NOTE]
>
>Il trasferimento preconfigurato di [!UICONTROL subscription events] non è supportato. Per trasferire [!UICONTROL subscription events], puoi creare XDM e set di dati corrispondenti in Adobe Experience Platform, quindi configurare una mappatura dati personalizzata per questi dati.
>
>Esistente [!UICONTROL experience events] non può essere acquisito in Adobe Experience Platform, ma generato in modo continuo [!UICONTROL experience events] vengono trasmesse in streaming a Adobe Experience Platform.

## Passaggi chiave per eseguire una mappatura dei dati

Le seguenti esercitazioni descrivono i passaggi chiave per eseguire una mappatura dei dati tra Campaign Standard e Adobe Experience Platform:

1. [Mappatura di risorse personalizzate](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [Mappatura di eventi Experience](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [Mappatura dei dati della tabella di seed](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [Modifica della mappatura dei dati](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [Verificare lo stato di un processo di acquisizione dati](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

