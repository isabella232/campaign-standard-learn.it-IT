---
title: Altre metriche importanti per la realizzazione
description: Uno dei modi migliori per identificare un problema di reputazione di invio è attraverso le metriche. Esaminiamo alcune metriche chiave di recapito per monitorare e come utilizzarle per identificare un problema di reputazione.
feature: null
topics: Deliverability
kt: 5256
doc-type: article
activity: understand
team: TM
translation-type: tm+mt
source-git-commit: 7aa32d583ac2ea756945a17634fb477d7b94cb7f
workflow-type: tm+mt
source-wordcount: '1367'
ht-degree: 0%

---


# Altre metriche importanti per la realizzazione

Uno dei modi migliori per identificare un problema di reputazione di invio è attraverso le metriche. Esaminiamo alcune metriche chiave di recapito per monitorare e come utilizzarle per identificare un problema di reputazione.

## Bounce

I rimbalzi sono il risultato di un tentativo di consegna e di un errore in cui l&#39;ISP fornisce avvisi di errore. L&#39;elaborazione di gestione dei rimbalzi è una parte fondamentale dell&#39;igiene degli elenchi. Dopo che un dato messaggio e-mail è stato rimbalzato più volte in una riga, questo processo lo contrassegna per la soppressione. Il numero e il tipo di rimbalzi necessari per attivare la soppressione variano da sistema a sistema. Questo processo impedisce ai sistemi di continuare a inviare indirizzi e-mail non validi. I dati Bounces sono uno dei dati chiave utilizzati dagli ISP per determinare la reputazione IP. Tenere d&#39;occhio questa metrica è molto importante. &quot;Consegnato&quot; e &quot;Rimbalzato&quot; è probabilmente il modo più comune per misurare la distribuzione dei messaggi di marketing: più alta è la percentuale consegnata, meglio è. Verranno esaminati due diversi tipi di rimbalzi.

## Rimbalzi netti

I rimbalzi netti sono errori permanenti generati dopo che un ISP determina come non realizzabile un tentativo di invio a un indirizzo utente iscritto. In  Adobe Campaign, i rimbalzi rigidi classificati come non consegnabili vengono aggiunti alla quarantena, il che significa che non verranno tentati di nuovo. In alcuni casi, se la causa del fallimento non è nota, viene ignorato un duro rimbalzo. Di seguito sono riportati alcuni esempi comuni di rimbalzi duri:

* L&#39;indirizzo non esiste
* Account disattivato
* Sintassi non valida
* Dominio non valido

## Rimbalzi morbidi

I rimbalzi morbidi sono errori temporanei che gli ISP generano quando hanno difficoltà a consegnare la posta. Gli errori temporanei verranno ripetuti più volte (con scostamento in base all&#39;utilizzo di impostazioni di consegna Adobe Campaign personalizzate o predefinite) per tentare di ottenere un esito positivo. Indirizzi che rimbalzano continuamente morbido non verranno aggiunti alla quarantena fino a quando non è stato tentato il numero massimo di tentativi (che variano di nuovo a seconda delle impostazioni). Alcune cause comuni di rimbalzi morbidi includono:

* Cassetta postale completa
* Ricezione del server e-mail in background
* Problemi di reputazione del mittente

![tipi bounce](assets/bounce-types.png)

>[!NOTE]
>
>I rimbalzi sono un indicatore chiave di un problema di reputazione perché possono evidenziare un&#39;origine dati non corretta (rimbalzo duro) o un problema di reputazione con un ISP (rimbalzo morbido).
I rimbalzi contenuti si verificano spesso nell’ambito dell’invio di e-mail e dovrebbero essere risolti durante l’elaborazione dei tentativi prima di essere identificati come un problema di effettiva recapito. Se il tasso di rimbalzo morbido è superiore al 30% per un singolo ISP e non viene risolto entro 24 ore, è consigliabile sollevare un problema con il proprio consulente di recapito  Adobe Campaign.

## Reclami

I reclami vengono registrati quando un utente indica che un&#39;e-mail è indesiderata o imprevista. Questa azione dell’utente iscritto viene generalmente registrata tramite il client di posta elettronica dell’utente iscritto quando preme il pulsante dello spam o tramite un sistema di segnalazione di spam di terze parti.

### reclamo ISP

La maggior parte degli ISP di livello 1 e di livello 2 forniscono agli utenti un metodo di segnalazione dello spam, in quanto i processi di rinuncia e annullamento della sottoscrizione sono stati utilizzati in modo dannoso in passato per convalidare un indirizzo e-mail.  Adobe Campaign riceve questi reclami tramite FBL ISP. Questo viene stabilito durante il processo di configurazione per tutti gli ISP che forniscono FBL e consente  Adobe Campaign di aggiungere automaticamente indirizzi e-mail che si sono lamentati alla tabella di quarantena per la soppressione. I picchi nei reclami ISP possono essere un indicatore di scarsa qualità di elenco, metodi di raccolta di elenchi meno che ottimali, o politiche di coinvolgimento debole. Spesso sono anche indicati quando il contenuto non è rilevante.

### Denunce di terzi

Ci sono diversi gruppi anti-spam che consentono la segnalazione di spam a un livello più ampio. Le metriche di reclamo utilizzate da queste terze parti vengono utilizzate per assegnare tag al contenuto delle e-mail per identificare le e-mail di spam. Questo processo è noto anche come impronte digitali. Gli utenti di questi metodi di reclamo di terze parti sono generalmente più astuti riguardo l&#39;e-mail, quindi possono avere un impatto maggiore di altri reclami potrebbe avere se lasciato senza risposta.

>[!NOTE]
>
>I provider di servizi Internet raccolgono i reclami e li utilizzano per determinare la reputazione complessiva del mittente. Tutte le denunce dovrebbero essere soppresse e non più contattate il più rapidamente possibile e in conformità con le leggi e i regolamenti locali.

## Tracce spam

Un trap spam è un indirizzo usato per identificare un&#39;e-mail non autorizzata o non richiesta. Esistono delle trappole per lo spam che aiutano a identificare la posta dai mittenti fraudolenti o da quelli che non seguono le best practice relative alle e-mail. L&#39;indirizzo email della trappola dello spam generalmente non è pubblicato pubblicamente e sono quasi impossibili da identificare. L&#39;invio di e-mail a trappole spam può influenzare la vostra reputazione con diversi gradi di gravità a seconda del tipo di trappola e del provider di servizi Internet. Ulteriori informazioni sui diversi tipi di spam traps nelle sezioni seguenti.

### Riciclato

Le trappole di spam riciclate sono indirizzi che prima erano validi ma che non sono più utilizzati. Un modo chiave per mantenere gli elenchi il più puliti possibile è quello di inviare regolarmente e-mail a tutto l&#39;elenco e sopprimere adeguatamente le e-mail rimbalzate. In questo modo, gli indirizzi e-mail abbandonati verranno messi in quarantena e non saranno più utilizzati.

In alcuni casi, un indirizzo può essere riciclato entro 30 giorni. L&#39;invio regolare è un aspetto fondamentale della buona igiene degli elenchi, insieme alla soppressione regolare degli utenti inattivi. Le campagne di reinserimento fanno generalmente parte di sofisticati programmi di e-mail marketing. Questo stile di campagna consente al mittente di tentare di riconquistare gli utenti che altrimenti non sarebbero più inviati per posta.

### Typo

Una trappola di spam è un indirizzo che contiene un errore ortografico o una malformazione. Ciò si verifica spesso con errori ortografici noti di domini principali come [!DNL Gmail] (ad esempio: [!DNL gmail] è un errore ortografico comune). Gli ISP e altri operatori di liste di blocco registreranno i domini danneggiati noti da usare come trappola dello spam per identificare gli spammers e misurare la salute del mittente. Il modo migliore per impedire l&#39;intercettazione di messaggi di posta indesiderata è utilizzare un doppio processo di consenso per la raccolta di elenchi.

### Pristina

Una trappola di spam incontaminata è un indirizzo che non ha un utente finale e non ha mai avuto un utente finale. Si tratta di un indirizzo creato esclusivamente per identificare le e-mail di spam. Questo è il tipo di trappola per spam più incisivo, in quanto è praticamente impossibile da identificare e richiederebbe uno sforzo sostanziale per pulirlo dall&#39;elenco. La maggior parte delle liste nere utilizzano trappole incontaminate spam per elencare mittenti non affidabili. L&#39;unico modo per evitare che le trappole incontaminate infettino il più ampio elenco di e-mail di marketing è quello di utilizzare un doppio processo di opt-in per la raccolta di elenchi.

## Bulk

Per &quot;bulking&quot; si intende la consegna della posta nella cartella dello spam o della spazzatura di un ISP. È identificabile quando una frequenza di apertura inferiore a quella normale (e a volte anche una frequenza di clic) è associata a una velocità elevata. Le cause per cui le e-mail vengono inserite variano a seconda del provider di servizi Internet. In generale, tuttavia, se i messaggi vengono inseriti nella cartella di massa, un flag che influenza la reputazione di invio (ad esempio l&#39;igiene degli elenchi) richiede una rivalutazione. È un segnale della diminuzione della reputazione, un problema che deve essere risolto immediatamente prima che influisca su ulteriori campagne. Consulta il tuo  consulente Adobe Campaign per la fornitura di soluzioni a qualsiasi problema a seconda della tua situazione.

## Blocco

Un blocco si verifica quando gli indicatori di spam raggiungono soglie ISP proprietarie e l&#39;ISP inizia a bloccare la posta (visibile attraverso tentativi di posta indesiderata) da un mittente. Ci sono vari tipi di blocchi. In genere, i blocchi si verificano in modo specifico per un indirizzo IP, ma possono anche verificarsi a livello di dominio o entità mittente. La risoluzione di un blocco richiede competenze specifiche, quindi contattare il consulente  Adobe Campaign per l&#39;erogazione di assistenza.

## Blacklist

Una blacklist si verifica quando un gestore di liste nere di terze parti registra un comportamento simile allo spammer associato a un mittente. La causa di una blacklist viene a volte pubblicata dalla blacklist. Un elenco è generalmente basato sull&#39;indirizzo IP, ma in casi più gravi può essere basato su un intervallo IP o addirittura su un dominio di invio. La risoluzione di una blacklist deve coinvolgere il supporto del consulente  Adobe Campaign per la distribuzione al fine di risolvere e prevenire ulteriori inserzioni. Alcuni elenchi sono estremamente gravi e possono causare problemi di reputazione di lunga durata difficili da risolvere. Il risultato di una blacklist varia in base alla blacklist, ma ha il potenziale di impatto sulla consegna di tutte le e-mail.

## Risorse aggiuntive

* [Tipi e motivi di errori di consegna](https://docs.adobe.com/content/help/en/campaign-standard/using/testing-and-sending/monitoring-messages/understanding-delivery-failures.html#delivery-failure-types-and-reasons)
