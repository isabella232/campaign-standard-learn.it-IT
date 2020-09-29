---
title: Processo di transizione - Passaggio a piattaforme di posta elettronica
description: 'Quando si spostano i provider di servizi e-mail (ESP), non è possibile effettuare transizioni anche con gli indirizzi IP esistenti. È importante seguire le best practice per sviluppare una reputazione positiva all’avvio successivo. Poiché i nuovi indirizzi IP che utilizzerete non hanno ancora una reputazione, gli ISP non sono in grado di fidarsi pienamente della posta che proviene da loro e devono essere cauti in ciò che consentono di essere consegnati ai loro clienti. '
feature: null
topics: Deliverability
kt: null
doc-type: article
activity: understand
team: TM
translation-type: tm+mt
source-git-commit: f4dbccc1fea3db4dbddec0d4329b359993b62d20
workflow-type: tm+mt
source-wordcount: '1686'
ht-degree: 0%

---


# Processo di transizione - Passaggio a piattaforme di posta elettronica

Quando si spostano i provider di servizi e-mail (ESP), non è possibile effettuare transizioni anche con gli indirizzi IP esistenti. È importante seguire le best practice per sviluppare una reputazione positiva all’avvio successivo. Poiché i nuovi indirizzi IP che utilizzerete non hanno ancora una reputazione, gli ISP non sono in grado di fidarsi pienamente della posta che proviene da loro e devono essere cauti in ciò che consentono di essere consegnati ai loro clienti.

Pensate a quello che fate quando incontrate qualcuno di nuovo. In genere, è necessario creare fiducia al posto di fidarsi di loro immediatamente. Non pensate che il vostro marchio aiuterà automaticamente con quella fiducia, perché gli spammer useranno il vostro nome per fare cose cattive. Gli ISP devono rivalutare le procedure di invio, dal momento che l&#39;azione è più importante nella recapito delle e-mail.

Stabilire una reputazione positiva è un processo. Ma una volta stabilito, piccoli indicatori negativi avranno meno impatto su voi e sulla vostra consegna di posta.

![Il processo di transizione](assets/transition-process.png)

La quantità di tempo per riscaldare gli indirizzi IP e i domini può variare, ma fino a otto settimane di benchmark è comune per i mittenti tipici per stabilire una reputazione al massimo livello 1 ISP ([!DNL Gmail], [!DNL Microsoft], [!DNL Verizon]/[!DNL Yahoo]/[!DNL AOL], ecc.).
Nelle sezioni successive verranno approfondite alcune aree chiave su cui concentrare l&#39;attenzione sull&#39;integrazione.

## Infrastruttura

Il successo della realizzazione dipende da una solida base. L&#39;infrastruttura e-mail è un elemento fondamentale. Un&#39;infrastruttura e-mail costruita correttamente include più componenti: dominio(i) e indirizzo(i) IP. Questi componenti sono come la macchina che sta dietro alle e-mail inviate e spesso rappresentano l&#39;àncora per l&#39;invio di reputazione. I consulenti sulla possibilità di realizzare l&#39;implementazione assicurano che questi elementi siano configurati correttamente, ma a causa dell&#39;elemento di reputazione è importante che tu disponga di questa conoscenza di base.

### Configurazione e strategia del dominio

I tempi sono cambiati, e alcuni ISP (come [!DNL Gmail] e [!DNL Yahoo]) ora incorporano la reputazione del dominio come punto aggiuntivo quando si tratta di allegare la reputazione dell&#39;email a un mittente. La reputazione del dominio è basata sul dominio di invio anziché sull&#39;indirizzo IP. Ciò significa che il tuo marchio ha la precedenza quando si tratta di decisioni relative ai filtri ISP.

Parte del processo di onboarding per i nuovi mittenti su  Adobe Campaign include la configurazione dei domini di invio e la verifica che l&#39;infrastruttura sia stabilita correttamente. È necessario collaborare con un esperto per individuare i domini che si intende utilizzare a lungo termine. Di seguito sono riportati alcuni suggerimenti che definiscono una buona strategia per il dominio:

* Con il dominio scelto devi essere il più chiaro e riflessivo possibile sul marchio, in modo che gli utenti non identifichino erroneamente la posta come spam. Alcuni esempi sono [!DNL newsletter.foo.com], [!DNL receipts.foo.com]e così via.
* Non devi usare il tuo dominio padre o aziendale, in quanto potrebbe influenzare la consegna della posta da parte dell’organizzazione a ISP.
* Prendere in considerazione l&#39;utilizzo di un sottodominio del dominio padre per legittimare il dominio di invio.
* Separa i tuoi sottodomini per le categorie di messaggi transazionali e di marketing. Questo aiuterà il flusso di traffico delle e-mail su una base più affidabile, come gli ISP cercano questo metodo di invio, che è una procedura consigliata per le e-mail ed è nota.

### Strategia IP

È importante creare una strategia IP ben strutturata per contribuire a creare una reputazione positiva. Il numero di IP e la configurazione varia a seconda del modello aziendale e degli obiettivi di marketing. Collabora con un esperto per sviluppare una strategia chiara per iniziare subito. Considerate questi elementi importanti da notare:

* Troppi IP possono innescare problemi di reputazione, in quanto è una tattica comune di spammers per le scarpe da neve, che è una tattica utilizzata dagli spammers dove il traffico è diffuso su molti IP per massimizzare la consegna della posta spam. Anche se non siete uno spammer, potete assomigliare a uno se utilizzate troppi IP, soprattutto se questi IP non hanno avuto alcun traffico precedente.
* Un numero insufficiente di IP può causare problemi di throughput e causare problemi di reputazione. La quantità di risorse varia a seconda dell&#39;ISP. Quanto e quanto rapidamente un ISP è disposto ad accettare è tipicamente basato sulla propria infrastruttura e l&#39;invio di soglie di reputazione.
* Separare il traffico per i tipi di messaggi è fondamentale. È importante, come minimo, separare le attività di marketing e la posta transazionali su pool IP separati.
* A seconda della strategia di posta elettronica, potrebbe essere consigliabile separare diversi prodotti o flussi di marketing su diversi pool IP se la tua reputazione è drasticamente diversa. Anche alcuni esperti di marketing si suddividono per regione. Separare l&#39;IP per il traffico con una reputazione inferiore non risolve il problema di reputazione, ma previene i problemi con la vostra &quot;buona&quot; reputazione e-mail di consegna. Dopo tutto, non vuoi sacrificare il tuo buon pubblico per un pubblico più rischioso.

### Ciclo di feedback

Dietro le quinte,  Adobe Campaign sta elaborando i dati relativi a rimbalzi, reclami, annullamento dell&#39;iscrizione e altro ancora. La configurazione di questi cicli di feedback è un aspetto importante per la recapito. I reclami possono danneggiare una reputazione, quindi devi rimuovere gli indirizzi e-mail che registrano i reclami dal pubblico di destinazione. È importante notare che [!DNL Gmail] non fornisce questi dati indietro. Le intestazioni di annullamento dell’iscrizione e il filtraggio del coinvolgimento nell’elenco sono particolarmente importanti per [!DNL Gmail] gli abbonati, che ora costituiscono la maggior parte dei database degli abbonati.

### Autenticazione

L&#39;autenticazione è il processo utilizzato dagli ISP per convalidare l&#39;identità di un mittente. I due protocolli di autenticazione più comuni sono [!DNL Sender Policy Framework (SPF)] e [!DNL DomainKeys Identified Mail] (DKIM). Questi non sono visibili all’utente finale, ma aiutano gli ISP a filtrare le e-mail dai mittenti verificati. [!DNL Domain-based Message Authentication Reporting and Conformance] (DMARC) sta guadagnando popolarità, anche se le sue politiche non sono ancora state integrate da tutti i provider di servizi Internet nei loro sistemi di reputazione.

#### **SPF**

[!DNL Sender Policy Framework (SPF)] è un metodo di autenticazione che consente al proprietario di un dominio di specificare quali server di posta elettronica utilizzare per inviare posta da tale dominio.

#### **DKIM**

[!DNL Domain Keys Identified Mail (DKIM)] è un metodo di autenticazione utilizzato per rilevare gli indirizzi del mittente falsato (comunemente denominati [!DNL spoofing]). Se DKIM è abilitato, il ricevitore può confermare se il mittente è autorizzato a inviare posta da quel dominio.

#### **DMARC**

[!DNL Domain-based Message Authentication, Reporting and Conformance (DMARC)] è un metodo di autenticazione che consente ai proprietari del dominio di proteggere il proprio dominio da un uso non autorizzato. DMARC utilizza SPF o DKIM o entrambi per consentire al proprietario di un dominio di controllare cosa accade alla posta che non riesce l&#39;autenticazione: consegnati, messi in quarantena o rifiutati.

## Criteri di targeting

Quando si invia un nuovo traffico, è possibile eseguire il targeting degli utenti più attivi durante le prime fasi del riscaldamento dell&#39;IP. Questo aiuta a stabilire una reputazione positiva dall&#39;inizio per costruire in modo efficace la fiducia prima di entrare in contatto con i tipi di pubblico meno coinvolti. Di seguito è riportata una formula di base per il coinvolgimento:

![Formula per l&#39;uso](assets/formula-for-enagement.png)

In genere, un tasso di coinvolgimento si basa su un periodo di tempo specifico. Questa metrica può variare drasticamente a seconda che la formula sia applicata a un livello globale o per specifici tipi di posta o campagne. I criteri di targeting specifici devono essere forniti collaborando con il vostro consulente  Adobe Campaign, dal momento che ogni mittente e ISP varia e di solito richiede un piano personalizzato.

## Considerazioni specifiche dell&#39;ISP durante il riscaldamento dell&#39;IP

Gli ISP hanno regole diverse e modi diversi di vedere il loro traffico. Ad esempio, [!DNL Gmail] è uno dei provider ISP più sofisticati perché guardano al coinvolgimento molto strettamente (aperture e clic) oltre a tutte le altre misure di reputazione. Questo richiede un piano personalizzato che si rivolga solo agli utenti più attivi all&#39;inizio. Anche altri ISP possono richiedere lo stesso. Consulta il tuo consulente  Adobe Campaign per un piano specifico.

## Volume

Il volume di posta che invii è fondamentale per ottenere una reputazione positiva. Mettetevi nei panni di un ISP — se iniziate a vedere una tonnellata di traffico da qualcuno che non conoscete, sarebbe allarmante. L&#39;invio di grandi volumi di posta è rischioso ed è sicuro di causare problemi di reputazione che spesso sono difficili da risolvere. Può essere frustrante, dispendioso in termini di tempo, e costoso tirarsi fuori dalla cattiva reputazione e costruire e bloccare i problemi derivanti dall&#39;invio troppo presto.

Le soglie del volume variano in base al provider di servizi Internet e possono anche variare in base alle metriche di coinvolgimento medie. Alcuni mittenti richiedono una rampa di volume molto bassa e lenta, mentre altri possono consentire una rampa più ripida in volume. Consigliamo di collaborare con un esperto, come un consulente  per la distribuzione Adobe Campaign, per sviluppare un piano volume personalizzato.

Elenco di suggerimenti e suggerimenti per una transizione fluida:

* **L&#39;autorizzazione** è la base di qualsiasi programma email di successo.
* **Avvio** basso e lento con volumi di invio ridotti e quindi aumentare man mano che si stabilisce la reputazione del mittente.
* Una strategia **di posta** tandem consente di aumentare il volume su Campaign e di terminare con l&#39;ESP corrente, senza interrompere il calendario delle e-mail.
* **Il coinvolgimento è importante** : iniziate con gli abbonati che aprono e fanno clic regolarmente sulle e-mail.
* **Seguire il piano** — le nostre raccomandazioni hanno aiutato centinaia di clienti di Campaign ad accelerare i loro programmi e-mail.
* **Monitorate l’account** e-mail di risposta. È una cattiva esperienza da parte del cliente usare [!DNL nore-ply@xyz.com] o non rispondere.
* Gli indirizzi inattivi possono avere un impatto negativo sulla recapito. **Riattiva e riattiva l&#39;autorizzazione** sulla piattaforma corrente, non sui nuovi IP.
* **Domini** - usa un dominio di invio che è un sottodominio del dominio effettivo della tua società. Ad esempio, se il dominio della società è [!DNL xyz.com], [!DNL email.xyz.com] fornisce agli ISP maggiore credibilità di [!DNL xyzemail.com]
* **Trasparenza** : i dettagli di registrazione per il dominio e-mail devono essere disponibili al pubblico e non devono essere privati.

In molte circostanze, la posta transazionale non segue il tradizionale approccio di riscaldamento promozionale. È ovviamente difficile controllare il volume della posta transazionale a causa della sua natura, in quanto in genere richiede un&#39;interazione da parte dell&#39;utente per attivare il tocco dell&#39;e-mail. In alcuni casi, la posta transazionale può semplicemente essere transitata senza un piano formale. In altri casi, potrebbe essere meglio spostare ogni tipo di messaggio nel tempo per aumentare lentamente il volume. Ad esempio, potete eseguire la transizione nel modo seguente:

1. Conferme di acquisto - coinvolgimento elevato in generale
2. abbandono del carrello - coinvolgimento medio-alto in generale
3. E-mail di benvenuto - elevato livello di coinvolgimento ma può contenere indirizzi non validi a seconda dei metodi di raccolta degli elenchi
4. E-mail Win-back - minore coinvolgimento in generale

## Risorse aggiuntive

* [Avvio di una nuova piattaforma](https://docs.adobe.com/content/help/en/campaign-standard/using/testing-and-sending/managing-deliverability/starting-new-platform.html)
