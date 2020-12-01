---
title: Attività segnale esterno - Richiama un flusso di lavoro con i parametri
description: L'attività Segnale Esterno viene utilizzata per organizzare e orchestrare diversi processi che fanno parte dello stesso percorso del cliente in flussi di lavoro diversi. Consente di avviare un flusso di lavoro a partire da un altro, permettendo di supportare customer journey più complessi e al tempo stesso di monitorare e reagire meglio in caso di problemi.
feature: External Signal Activity
topics: Workflows
kt: 2750
thumbnail: 27249
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 11263e247184ddc6a8e3df6a8ed0899907fbb366
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 19%

---


# [!UICONTROL External Signal activity ]- Chiama un flusso di lavoro con i parametri

The [!UICONTROL External Signal activity] is used to organize and orchestrate different processes that are part of the same customer journey into different workflows. Consente di avviare un flusso di lavoro a partire da un altro, permettendo di supportare customer journey più complessi e al tempo stesso di monitorare e reagire meglio in caso di problemi.

In ACS 19.2 [!UICONTROL External Signal activity] non solo è possibile chiamare un flusso di lavoro, ma anche trasmettere i parametri al flusso di lavoro (un nome di audience a destinazione, un nome di file da importare, una parte del contenuto del messaggio, ecc.) al flusso di lavoro da un altro flusso di lavoro o da una chiamata REST API per l&#39;integrazione con i sistemi esterni.

Questo include anche una nuova attività **Test** in cui è possibile eseguire test su questa funzionalità.

Il seguente video illustra i passaggi di configurazione necessari per:

1. **Ricevere parametri** esterni da un sistema esterno, come un sistema di gestione dei contenuti (CRM):

   * Dichiarare i parametri nell&#39;attività segnale esterno
   * Configura la chiamata API per definire i parametri e attivare il flusso di lavoro Attività segnale esterno. Per ulteriori informazioni su come configurare una chiamata API, consulta [Attivazione di un’attività](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#triggering-a-signal-activity)di segnale.

1. **Personalizzare un flusso di lavoro con parametri** esterni (variabili di eventi):

   Una volta attivato il flusso di lavoro, i parametri vengono assimilati nelle variabili di eventi del flusso di lavoro e possono essere utilizzati all&#39;interno del flusso di lavoro. Consultate la [documentazione](https://helpx.adobe.com/campaign/standard/automating/using/calling-a-workflow-with-external-parameters.html) per tutte le attività che possono essere personalizzate con le variabili dell&#39;evento:

   * Configurare l&#39;attività di test (novità in 19.2)
   * Configurare l&#39;attività di lettura dell&#39;audience e di distribuzione tramite e-mail

1. **Configurare un&#39;attività** finale per chiamare un flusso di lavoro con parametri esterni

>[!VIDEO](https://video.tv.adobe.com/v/27249/?quality=12)

## Risorse aggiuntive

* [Segnale esterno (documentazione)](https://docs.adobe.com/content/help/it-IT/campaign-standard/using/managing-processes-and-data/data-management-activities/external-api.html)
