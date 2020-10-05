---
title: Risoluzione dei problemi relativi al Pannello di controllo Campaign
description: Il Pannello di controllo Campaign ti consente di monitorare e gestire lo storage SFTP per istanza e di aggiungere indirizzi IP all’elenco Consentiti.
feature: Control Panel
topics: null
kt: 2938
doc-type: article
activity: use
team: PM
translation-type: ht
source-git-commit: 2fd2e62663f4b09ce7afc6387b53e194fbcafde8
workflow-type: ht
source-wordcount: '327'
ht-degree: 100%

---


# Risoluzione dei problemi del [!UICONTROL Control Panel]

Scopri come risolvere i problemi durante l’utilizzo del Pannello di controllo Campaign.

## Accesso e home page

Problemi relativi ad accesso e home page.

### Sintomo: impossibile accedere ad Adobe Experience Cloud

**Procedura:**
l’utente deve individuare il proprio [!DNL IMS Org ID] (xxx). L’amministratore deve aggiungere l’utente al [!UICONTROL product profile] di [!DNL “Campaign-xxx-Admins”] per ogni istanza da gestire. Se l’utente è un amministratore di tutte le istanze, potrebbe comunque dover aggiungere se stesso come *[!UICONTROL user]*.

### Sintomo: nella [!UICONTROL Adobe Experience Cloud Home] non vengono visualizzati i collegamenti di un utente per l’accesso al [!UICONTROL Control Panel]

**Causa:**
gli utenti non vedranno i collegamenti finché non saranno stati aggiunti come utenti al [!UICONTROL product profile] `Campaign-xxx-Administrators/Admin`

**Procedura:**
l’amministratore deve aggiungere l’utente al [!UICONTROL product profile] *[!DNL Campaign-xxx-Admins]* per ogni istanza da gestire. Se l’utente è un amministratore di tutte le istanze, potrebbe comunque dover aggiungere se stesso come *[!UICONTROL user]*.

### Sintomo: un’istanza non è elencata nel [!UICONTROL Control Panel]

**Causa:**
probabilmente l’utente deve essere aggiunto come *[!UICONTROL user]* al profilo di prodotto `Campaign-xxx-Administrators/Admin` per l’istanza mancante

**Procedura:**
l’amministratore deve aggiungere l’utente al profilo di prodotto `Campaign-xxx-Admins` per ogni istanza da gestire. Se l’utente è un amministratore di tutte le istanze, potrebbe comunque dover aggiungere se stesso come *[!UICONTROL user]*.

### Video utili

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12&captions=ita)
*Controllare l’[!DNL IMS Org ID](00:26 min)*

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12&captions=ita)
*Come aggiungere un amministratore al[!UICONTROL product profile]di *[!DNL administrators]*per poter utilizzare il[!UICONTROL Control Panel](01:03 min)*

### Documentazione utile

* [Scopri il [!UICONTROL Control Panel]](https://helpx.adobe.com/it/campaign/kb/control-panel-overview.html)
* [Gestione delle autorizzazioni per il [!UICONTROL Control Panel]](https://helpx.adobe.com/it/campaign/kb/control-panel-access.html)

## Stabilimento di una connessione al server SFTP (client o API)

La connessione ai server SFTP richiede:

* [!UICONTROL allow listing] l’indirizzo IP da cui desideri connetterti al server SFTP
* Una coppia di chiavi privata/pubblica che deve essere registrata con Adobe Campaign
* Il software client SFTP, se ti connetti direttamente al server SFTP

### Documentazione utile

* [Accesso al server SFTP](https://docs.adobe.com/content/help/it-IT/control-panel/using/control-panel-home.html#LoggingintoyourSFTPserver)

