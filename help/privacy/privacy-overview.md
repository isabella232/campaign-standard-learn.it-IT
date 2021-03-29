---
title: Richieste di accesso ai dati personali con Adobe Campaign Standard (ACS) - Panoramica
description: Questo tutorial spiega come creare richieste di accesso ai dati personali tramite l’interfaccia di Adobe Campaign Standard (ACS).
feature: GDPR, CCAP
topic: Privacy
kt: 1480
doc-type: feature video
activity: use
team: TM
translation-type: ht
source-git-commit: 556bff4c94e16d3a94561dee1ccb311bc003b631
workflow-type: ht
source-wordcount: '371'
ht-degree: 100%

---


# Richieste di accesso a dati personali dall’interfaccia utente di Adobe Campaign Standard

Adobe Campaign offre ai titolari del trattamento tre metodi per eseguire le richieste di accesso e cancellazione di dati personali sensibili in conformità con atti sulla privacy come il GDPR (General Data Protection Regulation, Regolamento generale sulla protezione dei dati) e il CCPA (California Consumer Privacy Act, legge sulla privacy dei consumatori della California):

* **Tramite l’integrazione del servizio core Privacy:** le richieste di accesso ai dati personali inviate da [!UICONTROL Privacy Service] a tutte le soluzioni Experience Cloud vengono gestite automaticamente da Campaign tramite un flusso di lavoro dedicato. Per scoprire come creare richieste di accesso a dati personali dal servizio core Privacy, consulta la documentazione di [Adobe Experience Platform Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html?lang=it).

* **Tramite API:** Adobe Campaign fornisce un’API che consente il processo automatico delle richieste di accesso a dati personali utilizzando REST.

* **Tramite l’interfaccia di Adobe Campaign:** per ogni richiesta di accesso a dati personali, il titolare del trattamento crea una nuova richiesta in Adobe Campaign.

>[!NOTE]
>
> **MODIFICHE INTRODOTTE IN ACS 19.4:**
> 
> L’integrazione di [Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html?lang=it) è il metodo da utilizzare per tutte le richieste di accesso ed eliminazione. A partire dalla versione 19.4, l’utilizzo dell’API e dell’interfaccia di Campaign per le richieste di accesso ed eliminazione diventa obsoleto. Per ulteriori informazioni sulle funzioni obsolete e rimosse da Campaign Standard, consulta [questa pagina](https://helpx.adobe.com/it/campaign/kb/acs-deprecated-and-removed-features.html).
>
>**Rinuncia alla vendita di informazioni personali (CCPA)**
>
>A partire dalla versione 19.4, nell’interfaccia e nell’API di Campaign compare un campo di rinuncia CCPA pronto all’uso. Nella versione 19.3, è necessario creare tale campo in Adobe Campaign Standard per sfruttare queste informazioni. Per ulteriori informazioni, consulta la [documentazione dettagliata](https://helpx.adobe.com/it/campaign/kb/acs-privacy.html#ccpa).
>
> Puoi controllare la tua versione cliccando sull’icona ? in alto a destra nell’interfaccia e selezionando Informazioni.

## Tutorial video

### Prerequisiti per le richieste di accesso ai dati personali

1. [Creare uno spazio dei nomi](/help/privacy/namespaces-for-privacy-requests.md)
1. [Modificare le risorse personalizzate](/help/privacy/custom-resources-for-privacy-requests.md)

### Creare, tracciare ed eseguire richieste di accesso ai dati personali tramite l’interfaccia utente di Adobe Campaign

* [Creare e tenere traccia delle richieste di accesso ai dati personali tramite l’interfaccia utente di Adobe Campaign](/help/privacy/create-and-track-privacy-requests.md)
* [Eseguire richieste di accesso ai dati personali](/help/privacy/execute-privacy-requests.md)

## Risorse aggiuntive

* [Linee guida generali sulla privacy per Campaign](https://helpx.adobe.com/it/campaign/kb/campaign-privacy-overview.html)
* [CCPA per ACS](https://helpx.adobe.com/it/campaign/kb/acs-privacy.html#ccpa)
* [Adobe Experience Platform Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html?lang=it)
* [Documentazione API REST di Adobe Campaign Standard](https://final-docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#privacy-management)
