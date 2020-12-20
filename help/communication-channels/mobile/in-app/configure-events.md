---
title: Configurare gli eventi
description: 'Quando si configura un messaggio in-app in  eventi Adobe Campaign Standard (ACS), è possibile definire quale azione avviata dall''utente attiverà il messaggio da visualizzare. '
feature: In-App
topics: Mobile
kt: 2548
thumbnail: 26245.jpg
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 11263e247184ddc6a8e3df6a8ed0899907fbb366
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 3%

---


# Configura [!UICONTROL Events] {#configuring-events}

Quando si configura un messaggio [!UICONTROL In-App], è necessario definire quale azione avviata dall&#39;utente attiva la visualizzazione del messaggio. Tali azioni sono denominate [!UICONTROL events]. Sono disponibili tre categorie di [!UICONTROL events]: [!UICONTROL Mobile Application events], [!UICONTROL Life Cycle events] e [!UICONTROL Analytics events].

## [!UICONTROL Mobile Application Events] {#mobile-application-events}

[!UICONTROL Mobile Application events] sono implementate  [!UICONTROL custom events] nell’applicazione mobile.

Esempi:

* Un cliente ha visualizzato un elemento
* Un cliente aggiunge un articolo al carrello
* Abbandono del carrello
* Un cliente ha acquistato qualcosa

È necessario configurare questi [!UICONTROL events] in  Adobe Campaign. Il seguente video descrive come eseguire questa operazione.

>[!VIDEO](https://video.tv.adobe.com/v/26245?quality=12)

## [!UICONTROL Life Cycle events]  {#life-cycle-events}

[!UICONTROL Lifecycle events] sono pronte  [!UICONTROL events]. Sono disponibili le seguenti [!UICONTROL events]:

* [!UICONTROL launched]
* [!UICONTROL upgraded]
* [!UICONTROL crashed]

Un esempio può essere un messaggio che introduce nuove funzioni dopo un aggiornamento o una promozione dell’evento.

>[!NOTE]
>
>È necessario configurare [!UICONTROL Lifecycle module] nell&#39;applicazione mobile. Per ulteriori informazioni su [Come aggiungere il ciclo di vita all&#39;app](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle), vedi qui

## [!UICONTROL Analytics Events] {#analytics-events}

Le tre categorie seguenti sono supportate a seconda degli strumenti utilizzati nell’app mobile:

* Adobe Analytics
* [!UICONTROL Context data]
* [!UICONTROL View state]

>[!NOTE]
>
>[!UICONTROL Analytics events] richiede una licenza Adobe Analytics . Dopo aver configurato l&#39;estensione [[!DNL Analytics] e aggiunto [Analytics all&#39;app](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#add-analytics-to-your-app), questi eventi diventano disponibili nella configurazione [!UICONTROL In-App] in ACS.](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#configure-analytics-extension-in-launch)

## Risorse aggiuntive

* [Abilita metriche del ciclo di vita (documentazione)](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
