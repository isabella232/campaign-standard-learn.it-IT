---
title: Risoluzione dei problemi per gli addetti al marketing
description: Conoscere gli errori più comuni può aiutare a risolvere più velocemente i problemi e aumentare la produttività. Questi suggerimenti per la risoluzione dei problemi consentono di risolvere in modo efficace errori simili in fase di esecuzione.
version: Standard
feature: Workflows
role: User
level: Beginner, Intermediate, Experienced
doc-type: Article
last-substantial-update: 2023-05-18T00:00:00Z
jira: KT-13256
thumbnail: KT-13256.jpeg
source-git-commit: bc9e83e1864b02208f9cd7fe591c77bf6d049a37
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 1%

---


# Risoluzione dei problemi per gli addetti al marketing: 5 Errori comuni di workflow e consegna

Da: [Suraj Patra](https://www.linkedin.com/in/suraj-p-51612053/){target="_blank"}, Consulente senior, Meijer

In qualità di Senior Engineer e di esperto di clienti sui prodotti Adobe Experience Cloud negli ultimi cinque anni, posso consentire agli utenti aziendali di [Meijer](https://www.meijer.com/){target="_blank"}, una catena di supercentri americana fondata nel 1934, per condurre campagne complesse e di marketing e transazionali con ACS. Alcuni progetti su cui ho lavorato includono campagne personalizzate per memorizzare offerte e dettagli degli ordini per la personalizzazione, integrate con Adobe Audience Manager, e informazioni sui clienti per l’acquisizione dei segmenti.


Nel mio tempo usando ACS, mi sono imbattuto in errori che possono richiedere molto tempo e frustranti per risolvere i problemi. Conoscere gli errori più comuni può aiutare a risolvere più velocemente i problemi e aumentare la produttività. Di seguito sono riportati i miei suggerimenti per la risoluzione dei problemi per aiutarti a risolvere in modo efficace gli errori simili che si verificano.

## Errore di mancata corrispondenza del tipo di dati

**Codice di errore:**
`PGS-220000 PostgreSQL error: ERROR: operator does not exist: character varying = bigint`

**Causa:**
Questi tipi di errori vengono visualizzati in un flusso di lavoro quando tenti di eseguire la riconciliazione utilizzando campi di tipi di dati diversi. Ad esempio, quando carichi un file utilizzando un file di caricamento con un campo stringa e tenti di riconciliare il campo stringa con un campo di profilo con un tipo di dati int.

![tipo di dati-mismatch-error](/help/assets/kt-13256/data-type-mismatch.png)

**Soluzione:**
Modifica il tipo di dati del campo nell’attività &quot;Load file&quot; con quello corrispondente. Apri l’attività &quot;Load file&quot;. Passa alla scheda &quot;DEFINIZIONE COLONNA&quot; e modifica il tipo di dati del campo desiderato.


![data-type-mismatch-solution](/help/assets/kt-13256/data-type-mismatch-solution.png)

## Errore di personalizzazione della consegna

**Codice di errore:**
`The schema for profiles specified in the transition ('') is not compatible with the schema defined in the delivery template ('nms:recipient'). They should be identical.`

**Causa:**
Questo errore viene visualizzato quando si invia un’e-mail a un indirizzo, ma l’e-mail o qualsiasi altro identificatore non viene riconciliato con un profilo. Per inviare una comunicazione e-mail, l’e-mail o l’identificatore deve essere sempre collegato a un profilo.

Utilizza l’attività di riconciliazione come mostrato di seguito:

![flusso di lavoro con attività di riconciliazione](/help/assets/kt-13256/del-persn-error-wf.png)

**Soluzione:**
Deve esistere un ID comune dal file caricato con la tabella dei destinatari. Questa chiave comune unisce il file di caricamento alla tabella dei destinatari all’interno dell’attività di riconciliazione. Le e-mail potrebbero non essere inviate a record non presenti nella tabella dei destinatari che richiede questo passaggio di riconciliazione all’interno del flusso di lavoro. In questo modo, puoi riconciliare l’attività del file di caricamento in arrivo con un identificatore come ID e-mail dal profilo. La `nms:recipient` schema si riferisce alla tabella di profilo e la riconciliazione dei record in arrivo con profilo la rende disponibile durante la preparazione dell’e-mail.

Fai riferimento alla schermata per l’attività di riconciliazione come mostrato di seguito.

![flusso di lavoro con dettagli di riconciliazione](/help/assets/kt-13256/del-persn-error-wf-solution.png)

Ulteriori informazioni [riconciliazione](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/data-management-activities/reconciliation.html?lang=en).

## Errore set di dati del campo comune

**Codice di errore:**
`The document types of inbound events (''and'') are incompatible (step 'Exclusion'). Unable to perform the operation. `

**Causa:**
Questo problema si verifica quando si utilizza il **attività di esclusione** nei flussi di lavoro ACS. L&#39;errore si verifica quando si eseguono ed escludono in base all&#39;ID, quando il set primario e il set escluso non hanno gli stessi nomi di campo.


![Errore set di dati del campo comune](/help/assets/kt-13256/dataset-error.png)

**Soluzione:**

Esistono due modi per risolvere questo errore:

1. Utilizza lo stesso nome di campo sia nel campo primario che in quello escluso e utilizza lo stesso campo come ID

   OPPURE

1. Utilizzare il metodo di esclusione JOINS per selezionare il campo in base al quale si desidera escludere i record.

![Errore del set di dati del campo comune - Soluzione ](/help/assets/kt-13256/dataset-error-solution.png)

## Errore di eliminazione del nome campo

**Codice di errore:**
`XTK-170036 Unable to parse expression 'i__name'`

**Causa:**

I punti di errore possono verificarsi in un **attività di arricchimento**. Uno dei più comuni è mostrato di seguito.

![Errore di eliminazione del nome campo](/help/assets/kt-13256/field-name-dropped-error.png)

Questo accade quando modifichi manualmente un nome di espressione nell’attività . L’immagine mostra che l’espressione è stata modificata da `name `a `i__name`.

**Soluzione:**

Puoi risolvere questo errore in tre modi:

1. Cambia il nome in base all&#39;espressione originariamente presente.

2. Se desideri utilizzare un nuovo nome, modifica i valori nelle attività nella **attività di arricchimento**.

3. Se non ricordi cosa è cambiato, la migliore scommessa è ricreare l&#39;attività.

## Errore di eliminazione tabella temporanea 

**Codice di errore:**
`XTK-170024 The temporary schema "temp:deliveryEmail1" is not defined in the current context.`

**Causa:**
Si tratta di un errore comune nei flussi di lavoro complicati che comportano un arricchimento o un’altra attività. Probabilmente significa che alcuni dei flussi di lavoro attività non vengono salvati correttamente durante più modifiche al flusso di lavoro.

![Errore di eliminazione tabella temporanea ](/help/assets/kt-13256/temp-table-dropped-error.png)

**Soluzione:**
Ci sono molti modi in cui questo errore può verificarsi, quindi non c&#39;è una semplice correzione. Se si tratta di un flusso di lavoro semplice, è meglio riconfigurare l’attività. In un flusso di lavoro complicato, è meglio copiare le attività del flusso di lavoro in un nuovo flusso di lavoro, salvarle ed eseguirle nuovamente.