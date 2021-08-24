---
title: Risoluzione dei problemi relativi al Pannello di controllo Campaign
description: Il Pannello di controllo Campaign ti consente di monitorare e gestire l’archiviazione SFTP per istanza e inserire nell'elenco Consentiti gli indirizzi IP.
feature: Pannello di controllo Campaign
kt: 2938
doc-type: article
activity: use
team: PM
exl-id: f546f791-a69b-4586-abfa-3e626b8feb17
source-git-commit: 481cbdcc9ac7446cc36fbff6e3d6e43fe333d30b
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 44%

---

# Risoluzione dei problemi del [!UICONTROL Control Panel]

Scopri come risolvere i problemi durante l’utilizzo del Pannello di controllo Campaign.

## Accesso e home page

Problemi relativi ad accesso e home page.

### Sintomo: Impossibile accedere a Adobe Experience Cloud

**Come procedere:**
l’utente deve individuare il proprio  [!DNL IMS Org ID] (xxx). L’amministratore deve aggiungere l’utente al [!UICONTROL product profile] [!DNL “Campaign-xxx-Admins”] per ogni istanza da gestire. Se l’utente è amministratore di tutte le istanze, deve aggiungere se stesso come *[!UICONTROL user]*.

### Sintomo: nella [!UICONTROL Adobe Experience Cloud Home] non vengono visualizzati i collegamenti di un utente per l’accesso al [!UICONTROL Control Panel]

**Causa:**
gli utenti non vedranno i collegamenti finché non saranno stati aggiunti come utenti al [!UICONTROL product profile] `Campaign-xxx-Administrators/Admin`

**Procedura:**
l’amministratore deve aggiungere l’utente al  [!UICONTROL product profile] *[!DNL Campaign-xxx-Admins]* per ogni istanza da gestire. Se l’utente è amministratore di tutte le istanze, deve aggiungere se stesso come *[!UICONTROL user]*.

### Sintomo: un’istanza non è elencata nel [!UICONTROL Control Panel]

**Causa:**
probabilmente l’utente deve essere aggiunto come profilo di  *[!UICONTROL user]* prodotto  `Campaign-xxx-Administrators/Admin` per l’istanza mancante

**Procedura:**
l’amministratore deve aggiungere l’utente al profilo di prodotto  `Campaign-xxx-Admins` per ogni istanza da gestire. Se l’utente è amministratore di tutte le istanze, deve aggiungere se stesso come *[!UICONTROL user]*.

### Video utili

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12)

*Check [!DNL IMS Org ID] (00:26 min)*

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12)

*Come aggiungere un amministratore al [!UICONTROL product profile] di [!DNL administrators] per poter utilizzare il [!UICONTROL Control Panel] (01:03 min)*

### Documentazione utile

* [Scopri il [!UICONTROL Control Panel]](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=it)
* [Gestione delle autorizzazioni per il [!UICONTROL Control Panel]](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=en)

## Stabilimento di una connessione al server SFTP (client o API)

La connessione ai server SFTP richiede:

* [!UICONTROL allow listing] l’indirizzo IP da cui desideri connetterti al server SFTP
* Coppia di chiavi privata/pubblica che deve essere registrata con Adobe Campaign
* Se ti connetti direttamente al server SFTP, devi disporre di un software client SFTP

### Documentazione utile {#helpful-docs}

* [Accesso al server SFTP](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=en)
