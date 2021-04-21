---
title: 'Attività segnale esterno : chiama un flusso di lavoro con parametri'
description: Scopri come avviare un flusso di lavoro da un altro per supportare percorsi di clienti più complessi e allo stesso tempo come monitorare e reagire meglio ai problemi.
feature: Attività di esecuzione
kt: 2750
thumbnail: 27249
doc-type: feature video
activity: use
team: TM
exl-id: d3996185-681c-4906-85f0-0543ab767519
role: Business Practitioner, Developer
level: Experienced
translation-type: tm+mt
source-git-commit: ada0b029245190f53d58fa93c79c161719bfe9fd
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 9%

---

# [!UICONTROL External Signal activity ]- Chiamare un flusso di lavoro con i parametri

[!UICONTROL External Signal activity] viene utilizzato per organizzare e orchestrare diversi processi che fanno parte dello stesso percorso di clienti in flussi di lavoro diversi. Consente di avviare un flusso di lavoro a partire da un altro, permettendo di supportare customer journey più complessi e al tempo stesso di monitorare e reagire meglio in caso di problemi.

In ACS 19.2 il [!UICONTROL External Signal activity] può non solo chiamare un flusso di lavoro, ma anche trasmettere parametri al flusso di lavoro (un nome di pubblico per il target, un nome di file da importare, una parte del contenuto del messaggio, ecc.) al flusso di lavoro da un altro flusso di lavoro o da una chiamata API REST per l’integrazione con i sistemi esterni.

Questo include anche una nuova attività **Test** in cui puoi eseguire test su questa funzionalità.

Il video seguente spiega i passaggi di configurazione necessari per:

1. **Ricevere** parametri esterni da un sistema esterno, come un sistema di gestione dei contenuti (CRM):

   * Dichiarare i parametri nell’attività Segnale esterno
   * Configura la chiamata API per definire i parametri e attivare il flusso di lavoro External Signal Activity. Per ulteriori informazioni su come configurare una chiamata API, consulta [Attivazione di un’attività segnale](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#triggering-a-signal-activity).

1. **Personalizza un flusso di lavoro con parametri**  esterni (variabili di eventi):

   Una volta attivato il flusso di lavoro, i parametri vengono acquisiti nelle variabili degli eventi del flusso di lavoro e possono essere utilizzati all’interno del flusso di lavoro. Consulta la [documentazione](https://helpx.adobe.com/campaign/standard/automating/using/calling-a-workflow-with-external-parameters.html) per tutte le attività che possono essere personalizzate con le variabili dell&#39;evento:

   * Configurare l’attività di test (novità nella versione 19.2)
   * Configurare l’attività Read audience e Email Delivery

1. **Configurare un’** attività finale per chiamare un flusso di lavoro con parametri esterni

>[!VIDEO](https://video.tv.adobe.com/v/27249/?quality=12)

## Risorse aggiuntive

* [Segnale esterno (documentazione)](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/calling-workflow-external-parameters/calling-a-workflow-with-external-parameters.html)
