---
title: Problemi con le riprese del Pannello di controllo Campaign
description: Il Pannello di controllo Campaign consente di monitorare e gestire lo storage SFTP per istanza e  indirizzi IP del elenco consentiti.
feature: Control Panel
topics: null
kt: 2938
doc-type: article
activity: use
team: PM
translation-type: tm+mt
source-git-commit: b277b1ad17d9c03b307f8483d776b796e6c0cbef
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 1%

---


# Risoluzione dei problemi relativi al Pannello di controllo Campaign [!UICONTROL}

Scoprite come risolvere i problemi durante l&#39;utilizzo del Pannello di controllo Campaign.

## Login e homepage

Problemi che si verificano con login e homepage.

### Sintomo: Impossibile accedere ad Adobe Experience Cloud

**Procedura:**
L&#39;utente deve individuare il proprio [!DNL IMS Org ID] (xxx). L&#39;amministratore deve aggiungere l&#39;utente al [!UICONTROL product profile] [!DNL “Campaign-xxx-Admins”] modulo per ogni istanza che desidera gestire. Se l&#39;utente è un amministratore di tutte le istanze, potrebbe comunque dover aggiungere se stesso come *[!UICONTROL user]*.

### Sintomo: I collegamenti [!UICONTROL Adobe Experience Cloud Home] per accedere [!UICONTROL Control Panel] non vengono visualizzati per un utente

**Causa:**
Gli utenti non vedranno i collegamenti finché non saranno stati aggiunti come utenti a [!UICONTROL product profile] `Campaign-xxx-Administrators/Admin`

**Procedura:**
L&#39;amministratore deve aggiungere l&#39;utente al [!UICONTROL product profile] *[!DNL Campaign-xxx-Admins]* modulo per ogni istanza che desidera gestire. Se l&#39;utente è un amministratore di tutte le istanze, potrebbe comunque dover aggiungere se stesso come *[!UICONTROL user]*.

### Sintomo: Un&#39;istanza non è elencata nella variabile [!UICONTROL Control Panel]

**Causa:**
Probabilmente l’utente deve essere aggiunto come profilo di *[!UICONTROL user]* prodotto `!DNL Campaign-xxx-Administrators/Admin` per l’istanza mancante

**Procedura:**
L’amministratore deve aggiungere l’utente al profilo di prodotto `Campaign-xxx-Admins` per ogni istanza da gestire. Se l&#39;utente è un amministratore di tutte le istanze, potrebbe comunque dover aggiungere se stesso come *[!UICONTROL user]*.

### Video utili

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12)
*Check[!DNL IMS Org ID](00:26 min)*

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12)
*Come aggiungere un amministratore al[!UICONTROL product profile]sistema *[!DNL administrators]*per poter utilizzare[!UICONTROL Control Panel](01:03 min)*

### Documentazione utile

* [Scopri le [!UICONTROL Control Panel]](https://helpx.adobe.com/campaign/kb/control-panel-overview.html)
* [Gestione delle autorizzazioni per [!UICONTROL Control Panel]](https://helpx.adobe.com/campaign/kb/control-panel-access.html)

## Connessione al server SFTP (client o API)

La connessione ai server SFTP richiede:

* [!UICONTROL allow listing] l&#39;indirizzo IP da cui ci si connette al server SFTP
* Coppia di chiave pubblica/privata che deve essere registrata con  Adobe Campaign
* Se ti connetti direttamente al server SFTP, avrai bisogno anche del software client SFTP

### Documentazione utile

* [Accesso al server SFTP](https://helpx.adobe.com/campaign/kb/control-panel-sftp.html#LoggingintoyourSFTPserver)

