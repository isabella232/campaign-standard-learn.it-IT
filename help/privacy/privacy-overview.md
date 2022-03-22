---
title: Richieste di accesso ai dati personali con Adobe Campaign Standard (ACS) - Panoramica
description: Questo tutorial spiega come creare richieste relative alla privacy tramite l’interfaccia di Adobe Campaign Standard.
feature: Privacy Tools
kt: 1480
doc-type: feature video
activity: use
team: TM
recommendations: noDisplay
exl-id: fb766403-694c-4a7b-b3d1-4a418df85891
source-git-commit: 57dbf456625d22cd2e4526d92e5a8c20a048d339
workflow-type: ht
source-wordcount: '349'
ht-degree: 100%

---

# Richieste di accesso a dati personali dall’interfaccia utente di Adobe Campaign Standard

Adobe Campaign offre ai titolari del trattamento tre metodi per eseguire le richieste di accesso e cancellazione di dati personali sensibili in conformità con atti sulla privacy come il GDPR (General Data Protection Regulation, Regolamento generale sulla protezione dei dati) e il CCPA (California Consumer Privacy Act, legge sulla privacy dei consumatori della California):

* **Tramite l’integrazione del servizio core Privacy:** le richieste di accesso ai dati personali inviate da [!UICONTROL Privacy Service] a tutte le soluzioni Experience Cloud vengono gestite automaticamente da Campaign tramite un flusso di lavoro dedicato. Per informazioni su come creare richieste di privacy dal servizio core Privacy, fai riferimento a [Adobe Experience Platform Privacy Service](https://www.adobe.io/apis/experienceplatform/gdpr.html)

* **Tramite API:** Adobe Campaign fornisce un’API per abilitare il processo automatico per le richieste relative alla privacy utilizzando REST

* **Tramite l’interfaccia di Adobe Campaign:** per ogni richiesta relativa alla privacy, il titolare del trattamento crea una nuova richiesta in Adobe Campaign.

>[!NOTE]
>
> **MODIFICHE INTRODOTTE IN ACS 19.4:**
> 
> L’integrazione di [Privacy Service](https://www.adobe.io/apis/experienceplatform/gdpr.html) è il metodo da utilizzare per tutte le richieste di accesso ed eliminazione. A partire dalla versione 19.4, l’utilizzo dell’API e dell’interfaccia di Campaign per le richieste di accesso ed eliminazione diventa obsoleto. Per ulteriori informazioni sulle funzioni obsolete e rimosse da Campaign Standard, consulta [questa pagina](https://experienceleague.adobe.com/docs/campaign-standard/using/release-notes/deprecated-features.html?lang=it).
>
>**Rinuncia alla vendita di informazioni personali (CCPA)**
>
> Nell’interfaccia e nell’API di Campaign compare un campo di rinuncia CCPA pronto all’uso.
>
> Puoi controllare la tua versione, fai clic su **?** in alto a destra nell’interfaccia e seleziona Informazioni.

## Tutorial video

### Prerequisiti per le richieste di accesso ai dati personali

1. [Creare uno spazio dei nomi](/help/privacy/namespaces-for-privacy-requests.md)
1. [Modificare le risorse personalizzate](/help/privacy/custom-resources-for-privacy-requests.md)

### Creare, tracciare ed eseguire richieste relative alla privacy tramite l’interfaccia utente di Adobe Campaign

* [Creare e tenere traccia delle richieste relative alla privacy tramite l’interfaccia utente di Adobe Campaign](/help/privacy/create-and-track-privacy-requests.md)
* [Eseguire richieste di privacy](/help/privacy/execute-privacy-requests.md)

## Risorse aggiuntive

* [Linee guida generali sulla privacy per Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/privacy/privacy-management.html?lang=it#getting-started)
* [CCPA per ACS](https://experienceleague.adobe.com/docs/campaign-standard/using/getting-started/privacy/privacy-requests.html?lang=it#privacy-requests)
* [Adobe Experience Platform Privacy Service](https://www.adobe.io/apis/experienceplatform/gdpr.html)
* [Documentazione API REST di Adobe Campaign Standard](https://final-docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#privacy-management)
