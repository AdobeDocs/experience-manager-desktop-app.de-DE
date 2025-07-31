---
title: Verwenden  [!DNL Experience Manager]  Desktop-Programms
description: Verwenden  [!DNL Adobe Experience Manager]  -Desktop-Programms.
feature: Desktop App,Asset Management
source-git-commit: 2947fbd3bfeb15b37a8f1b0118e969b5d70499d0
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 58%

---


# Öffnen von Assets auf Ihrem Desktop {#openondesktop-v2}

Sie können die Remote-Assets zur Ansicht im nativen Programm öffnen. Die Assets werden in einen lokalen Ordner heruntergeladen. Anschließend werden sie in der nativen Anwendung gestartet, die mit dem Dateiformat verknüpft ist. Sie können das native Programm ändern, um bestimmte Dateitypen (Erweiterungen) auf Ihrem Mac- oder Windows-Computer zu öffnen.

Klicken Sie im Asset-Menü auf **[!UICONTROL Open]**. Das Asset wird lokal heruntergeladen und im nativen Programm geöffnet. Überprüfen Sie den Download-Status und die Übertragungsgeschwindigkeit großer Assets in der Statusleiste.

<!-- ![Download progress bar for large-sized assets](assets/download_status_bar_da2.png "Download progress bar for large-sized assets")
-->

>[!NOTE]
>
>Wenn die erwarteten Änderungen nicht im Programm übernommen werden, klicken Sie auf das Symbol „Aktualisieren“ ![Aktualisieren](assets/do-not-localize/refresh.png) oder klicken Sie mit der rechten Maustaste auf **[!UICONTROL Refresh]**. Die Aktionen sind nicht verfügbar, während größere Downloads oder Uploads ausgeführt werden.

Um den lokalen Download-Ordner eines Assets zu öffnen, klicken Sie auf das Symbol ![Mehr Aktionen](assets/do-not-localize/more2_da2.png) und dann auf ![Anzeigen](assets/do-not-localize/reveal_action2_da2.png) **[!UICONTROL Reveal File]**.

## Verwenden oder Platzieren von Assets in nativen Dokumenten {#place-assets-in-native-documents}

In einigen Fällen, z. B. beim Platzieren eines Assets in einem nativen Dokument, greifen Sie in Windows Explorer oder Mac Finder auf eine Datei zu. Um zum Speicherort der lokal heruntergeladenen Datei im Dateisystem zu gelangen, verwenden Sie die Option ![Anzeigen](assets/do-not-localize/reveal_action2_da2.png) **[!UICONTROL Reveal File]**.

![Aktion „Datei anzeigen“ für ein Asset](assets/revealfile_action_da2.png "Aktion „Datei anzeigen“ für ein Asset")

Klicken Sie auf **[!UICONTROL Reveal File]** oder **[!UICONTROL Reveal Folder]** auf einen Ordner, um Windows Explorer oder Mac Finder zu öffnen, wobei die Datei oder der Ordner auf dem lokalen Computer vorausgewählt ist. Beispielsweise ist die Option nützlich, um die [!DNL Experience Manager] Dateien in den nativen Programmen zu platzieren, die das Platzieren oder Verknüpfen lokaler Dateien unterstützen. Informationen zum Platzieren von Dateien in Adobe InDesign finden Sie unter [Platzieren von Grafiken](https://helpx.adobe.com/de/indesign/using/placing-graphics.html).

Die **[!UICONTROL Reveal File]** Aktion öffnet eine lokale Netzwerkfreigabe. Es werden nur die lokal verfügbaren Assets angezeigt. Das heißt, es zeigt Assets an, die mithilfe der -App angezeigt, heruntergeladen oder geöffnet/bearbeitet wurden. Die lokale Netzwerkfreigabe lädt keine Änderungen in [!DNL Experience Manager] hoch. Um die Änderungen hochzuladen, verwenden Sie explizit die **[!UICONTROL Upload Changes]**- oder **[!UICONTROL Upload]**-Aktionen in der App.

>[!NOTE]
>
>Zur Abwärtskompatibilität mit dem [!DNL Experience Manager]-Desktop-Programm v1.x werden die angezeigten Dateien von einer lokalen Netzwerkfreigabe bereitgestellt, wobei nur lokal verfügbare Dateien angezeigt werden. Die Desktop-Pfade der angezeigten Dateien sind mit den Pfaden identisch, die von der Programm-Version v1.x erstellt wurden.

>[!CAUTION]
>
>Verwenden Sie die Option **[!UICONTROL Reveal File]** nicht, um Assets in nativen Programmen zu bearbeiten. Verwenden Sie stattdessen die Aktionen **[!UICONTROL Edit]**. Weitere Informationen finden Sie unter [Erweiterter Workflow: Zusammenarbeit an denselben Dateien und Vermeidung von Bearbeitungskonflikten](#adv-workflow-collaborate-avoid-conflicts).

## Nächste Schritte {#next-steps}

* [Video zu den ersten Schritten mit dem Adobe Experience Manager Desktop-Programm ansehen](https://experienceleague.adobe.com/en/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app)

* Geben Sie Feedback zur Dokumentation über [!UICONTROL Edit this page] ![Bearbeiten der ](assets/do-not-localize/edit-page.png)) oder [!UICONTROL Log an issue] ![Erstellen eines GitHub-](assets/do-not-localize/github-issue.png) in der rechten Seitenleiste

* Kontaktieren Sie die [Kundenunterstützung](https://experienceleague.adobe.com/de?support-solution=General#support)

>[!MORELIKETHIS]
>
>* [Grundlegendes zur Benutzeroberfläche](/help/using/user-interface.md)
>* [Verwalten von Assets im Desktop-Programm](/help/using/assets-management-tasks.md)
>* [Suchen](/help/using/search.md)
