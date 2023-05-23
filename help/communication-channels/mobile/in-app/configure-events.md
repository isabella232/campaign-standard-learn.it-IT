---
title: Configurare gli eventi
description: "Scopri in che modo gli eventi definiscono quale azione avviata dall’utente attiverà la visualizzazione di un messaggio in-app. "
feature: In App
kt: 2548
thumbnail: 26245.jpg
doc-type: feature video
activity: use
team: TM
exl-id: 2c7937f4-b0da-46e5-934e-c660012c2c6f
role: User, Developer
level: Beginner, Intermediate
source-git-commit: 89df23d00913d36b93d3be03b62c74320524f9c7
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 2%

---

# Configurare [!UICONTROL Events] {#configuring-events}

Durante la configurazione di un’ [!UICONTROL In-App] messaggio, è necessario definire quale azione avviata dall’utente attiva il messaggio da visualizzare. Queste azioni sono denominate [!UICONTROL events]. Tre categorie di [!UICONTROL events] sono disponibili: [!UICONTROL Mobile Application events], [!UICONTROL Life Cycle events], e [!UICONTROL Analytics events].

## [!UICONTROL Mobile Application Events] {#mobile-application-events}

[!UICONTROL Mobile Application events] sono [!UICONTROL custom events] che sono implementati nella tua app mobile.

Alcuni esempi:

* Un cliente ha visualizzato un articolo
* Un cliente aggiunge un articolo al carrello
* Abbandono carrello
* Un cliente ha acquistato qualcosa

Devi configurare questi [!UICONTROL events] in Adobe Campaign. Il video seguente illustra come eseguire questa operazione.

>[!VIDEO](https://video.tv.adobe.com/v/26245?quality=12&learn=on)

## [!UICONTROL Life Cycle events] {#life-cycle-events}

[!UICONTROL Lifecycle events] sono pronti all’uso [!UICONTROL events]. I seguenti elementi [!UICONTROL events] sono disponibili:

* [!UICONTROL launched]
* [!UICONTROL upgraded]
* [!UICONTROL crashed]

Un esempio di caso d’uso può essere un messaggio che introduce nuove funzioni dopo un aggiornamento o una promozione di evento.

>[!NOTE]
>
>Il [!UICONTROL Lifecycle module] deve essere configurato nell’app mobile. Consulta qui per ulteriori informazioni su [Come aggiungere il ciclo di vita all’app](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle)

## [!UICONTROL Analytics Events] {#analytics-events}

Le tre categorie seguenti sono supportate a seconda degli strumenti utilizzati nella tua app mobile:

* Adobe Analytics
* [!UICONTROL Context data]
* [!UICONTROL View state]

>[!NOTE]
>
>[!UICONTROL Analytics events] richiede una licenza Adobe Analytics. Una volta ottenuta la [[!DNL Analytics] estensione configurata](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#configure-analytics-extension-in-launch) e hanno aggiunto [Analytics per l’app](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#add-analytics-to-your-app), questi eventi diventano disponibili nel [!UICONTROL In-App] configurazione in ACS.
