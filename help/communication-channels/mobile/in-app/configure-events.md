---
title: Configurare gli eventi
description: '"Scopri in che modo gli eventi definiscono quale azione avviata dall’utente attiverà un messaggio in-app da visualizzare. "'
feature: In-app
kt: 2548
thumbnail: 26245.jpg
doc-type: feature video
activity: use
team: TM
exl-id: 2c7937f4-b0da-46e5-934e-c660012c2c6f
role: Business Practitioner, Developer
level: Beginner, Intermediate
translation-type: tm+mt
source-git-commit: ada0b029245190f53d58fa93c79c161719bfe9fd
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 3%

---

# Configura [!UICONTROL Events] {#configuring-events}

Durante la configurazione di un messaggio [!UICONTROL In-App], è necessario definire quale azione avviata dall’utente attiva la visualizzazione del messaggio. Queste azioni sono denominate [!UICONTROL events]. Sono disponibili tre categorie di [!UICONTROL events]: [!UICONTROL Mobile Application events], [!UICONTROL Life Cycle events] e [!UICONTROL Analytics events].

## [!UICONTROL Mobile Application Events] {#mobile-application-events}

[!UICONTROL Mobile Application events] sono  [!UICONTROL custom events] implementati nella tua app mobile.

Gli esempi sono:

* Un cliente ha visualizzato un elemento
* Un cliente aggiunge un articolo al carrello
* Abbandono del carrello
* Un cliente ha acquistato qualcosa

Devi configurare questi [!UICONTROL events] in Adobe Campaign. Il video seguente descrive come eseguire questa operazione.

>[!VIDEO](https://video.tv.adobe.com/v/26245?quality=12)

## [!UICONTROL Life Cycle events]  {#life-cycle-events}

[!UICONTROL Lifecycle events] sono preconfigurati  [!UICONTROL events]. Sono disponibili le seguenti [!UICONTROL events]:

* [!UICONTROL launched]
* [!UICONTROL upgraded]
* [!UICONTROL crashed]

Un esempio di caso d’uso potrebbe essere un messaggio che introduce nuove funzioni dopo un aggiornamento o una promozione dell’evento.

>[!NOTE]
>
>È necessario configurare [!UICONTROL Lifecycle module] nell’app mobile. Per ulteriori informazioni su [Come aggiungere il ciclo di vita all&#39;app](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle), vedi qui

## [!UICONTROL Analytics Events] {#analytics-events}

Le tre categorie seguenti sono supportate a seconda degli strumenti utilizzati nella tua app mobile:

* Adobe Analytics
* [!UICONTROL Context data]
* [!UICONTROL View state]

>[!NOTE]
>
>[!UICONTROL Analytics events] richiedere una licenza Adobe Analytics. Dopo aver configurato l&#39; [[!DNL Analytics] estensione](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#configure-analytics-extension-in-launch) e aggiunto [Analytics all&#39;app](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#add-analytics-to-your-app), questi eventi diventano disponibili nella configurazione [!UICONTROL In-App] in ACS.

## Risorse aggiuntive

* [Abilitare le metriche del ciclo di vita (documentazione)](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
