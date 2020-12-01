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

Durante la configurazione di un [!UICONTROL In-App] messaggio, devi definire quale azione avviata dall’utente attiva la visualizzazione del messaggio. Tali azioni vengono denominate [!UICONTROL events]. Sono [!UICONTROL events] disponibili tre categorie: [!UICONTROL Mobile Application events], [!UICONTROL Life Cycle events]e [!UICONTROL Analytics events].

## [!UICONTROL Mobile Application Events] {#mobile-application-events}

[!UICONTROL Mobile Application events] sono implementate [!UICONTROL custom events] nell’applicazione mobile.

Esempi:

* Un cliente ha visualizzato un elemento
* Un cliente aggiunge un articolo al carrello
* Abbandono del carrello
* Un cliente ha acquistato qualcosa

È necessario configurarli [!UICONTROL events] in  Adobe Campaign. Il seguente video descrive come eseguire questa operazione.

>[!VIDEO](https://video.tv.adobe.com/v/26245?quality=12)

## [!UICONTROL Life Cycle events]  {#life-cycle-events}

[!UICONTROL Lifecycle events] sono pronte [!UICONTROL events]. The following [!UICONTROL events] are available:

* [!UICONTROL launched]
* [!UICONTROL upgraded]
* [!UICONTROL crashed]

Un esempio può essere un messaggio che introduce nuove funzioni dopo un aggiornamento o una promozione dell’evento.

>[!NOTE]
>
>È [!UICONTROL Lifecycle module] necessario configurare l&#39;applicazione per dispositivi mobili. Per ulteriori informazioni su [Come aggiungere il ciclo di vita all&#39;app, consulta qui](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle)

## [!UICONTROL Analytics Events] {#analytics-events}

Le tre categorie seguenti sono supportate a seconda degli strumenti utilizzati nell’app mobile:

* Adobe Analytics
* [!UICONTROL Context data]
* [!UICONTROL View state]

>[!NOTE]
>
>[!UICONTROL Analytics events] richiede una licenza Adobe Analytics . Dopo aver configurato [[!DNL Analytics] l&#39;](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#configure-analytics-extension-in-launch) estensione e aver aggiunto [Analytics all&#39;app](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#add-analytics-to-your-app), questi eventi diventano disponibili nella [!UICONTROL In-App] configurazione in ACS.

## Risorse aggiuntive

* [Abilita metriche del ciclo di vita (documentazione)](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
