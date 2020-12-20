---
title: Richieste sulla privacy con l'Adobe Campaign Standard  (ACS) - Panoramica
description: L'esercitazione spiega come creare le richieste Pprivacy tramite l'interfaccia Adobe Campaign Standard (ACS) .
feature: GDPR, CCAP
topic: Privacy
kt: 1480
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 556bff4c94e16d3a94561dee1ccb311bc003b631
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 20%

---


# Richieste di privacy con l&#39;interfaccia utente  Adobe Campaign Standard

 Adobe Campaign offre ai responsabili del trattamento dei dati tre metodi per eseguire l&#39;accesso alla privacy ed eliminare le richieste di dati PII in conformità con atti di privacy quali GDPR (General Data Protection Regulation) e CCPA (California Consumer Privacy Act):

* **Mediante l&#39;integrazione con il servizio di base sulla privacy: le richieste di** privacy inviate  [!UICONTROL Privacy Service] a tutte le soluzioni di Experience Cloud vengono gestite automaticamente da Campaign tramite un flusso di lavoro dedicato. Fare riferimento a [ Adobe Experience Platform Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html) per informazioni su come creare richieste di privacy dal servizio di base sulla privacy

* **Mediante l&#39;API:**  Adobe Campaign fornisce un&#39;API che consente il processo automatico delle richieste di privacy utilizzando REST

* **Tramite l&#39;interfaccia Adobe Campaign :** per ogni richiesta di privacy, il controller dei dati crea una nuova richiesta di privacy in  Adobe Campaign

>[!NOTE]
>
> **MODIFICHE CON ACS 19.4:**
> 
> L&#39; [integrazione Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html) è il metodo da utilizzare per tutte le richieste di accesso ed eliminazione. A partire dalla versione 19.4, l&#39;utilizzo dell&#39;API e dell&#39;interfaccia di Campaign per le richieste di accesso ed eliminazione è diventato obsoleto. Per ulteriori informazioni sulle funzioni obsolete e rimosse dei Campaign Standard, fare riferimento a [questa pagina](https://helpx.adobe.com/it/campaign/kb/acs-deprecated-and-removed-features.html).
>
>**Rinuncia alla vendita di informazioni personali (CCPA)**
>
>A partire dalla versione 19.4, nell’interfaccia e nell’API di Campaign compare un campo di rinuncia CCPA pronto all’uso. Per utilizzare queste informazioni in 19.3, è necessario creare questo campo in  Adobe Campaign Standard. Per ulteriori informazioni, vedere la [documentazione dettagliata](https://helpx.adobe.com/it/campaign/kb/acs-privacy.html#ccpa).
>
> Puoi controllare la tua versione cliccando sull’icona ? in alto a destra nell’interfaccia e selezionando Informazioni.

## Tutorials video

### Prerequisiti per le richieste di privacy

1. [Creazione di uno spazio dei nomi](/help/privacy/namespaces-for-privacy-requests.md)
1. [Modifica di risorse personalizzate](/help/privacy/custom-resources-for-privacy-requests.md)

### Creazione, tracciamento ed esecuzione delle richieste di privacy tramite l&#39;interfaccia utente  Adobe Campaign

* [Creazione e tracciamento delle richieste di privacy tramite l&#39;interfaccia utente  Adobe Campaign](/help/privacy/create-and-track-privacy-requests.md)
* [Esegui richieste di privacy](/help/privacy/execute-privacy-requests.md)

## Risorse aggiuntive

* [Linee guida generali sulla privacy per Campaign](https://helpx.adobe.com/it/campaign/kb/campaign-privacy-overview.html)
* [CCPA per ACS](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ccpa)
* [ Adobe Experience Platform Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html)
* [Documentazione  Adobe Campaign Standard REST API](https://final-docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#privacy-management)
