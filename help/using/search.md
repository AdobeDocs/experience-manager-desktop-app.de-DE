---
title: Durchsuchen, Suchen und Anzeigen einer Vorschau von Assets im [!DNL Experience Manager]-Desktop-Programm
description: Durchsuchen, Suchen und Anzeigen einer Vorschau von Assets im  [!DNL Adobe Experience Manager] -Desktop-Programm.
feature: Desktop App
source-git-commit: 2947fbd3bfeb15b37a8f1b0118e969b5d70499d0
workflow-type: tm+mt
source-wordcount: '910'
ht-degree: 75%

---


# Durchsuchen, Suchen und Anzeigen einer Vorschau von Assets {#browse-search-preview-assets}

Sie können die im [!DNL Experience Manager]-Repository verfügbaren Assets vom Desktop-Programm aus durchsuchen, suchen und in der Vorschau anzeigen. Versuchen Sie Folgendes im Programm:

1. Navigieren Sie zu einem Ordner und sehen Sie einige grundlegende Informationen zu den im Ordner verfügbaren Assets sowie kleine Miniaturen aller Assets.

   ![DAM-Dateien und -Ordner durchsuchen](assets/browse_folder_da2.png "DAM-Dateien und -Ordner durchsuchen")

1. Um weitere Informationen und eine größere Miniaturansicht eines einzelnen Assets anzuzeigen, klicken Sie auf den Dateinamen.

   ![Anzeigen einer größeren Vorschau eines Assets und weiterer Aktionen](assets/large_preview_actions_da2.png "Anzeigen einer größeren Vorschau eines Assets und weiterer Aktionen")

1. Klicken Sie auf **[!UICONTROL Open]** oder **[!UICONTROL Edit]**, um die Datei lokal herunterzuladen und sie im nativen Programm anzuzeigen oder zu bearbeiten.
1. Suchen Sie mithilfe von Keywords nach einem zugehörigen Asset im [!DNL Experience Manager]-Repository. Verwenden Sie `?` und `*` als Platzhalter. Diese Platzhalter ersetzen ein einzelnes oder mehrere Zeichen. Filtern und sortieren Sie die Ergebnisse nach Bedarf.

   ![Beispielsuche mit einem Sternchen-Platzhalter](assets/search_wildcard_da2.png "Beispielsuche mit einem Sternchen-Platzhalter")

   ![Eine weitere Beispielsuche mit unterschiedlicher Platzierung des Sternchen-Platzhalters](assets/search_wildcard2_da2.png "Eine weitere Beispielsuche mit unterschiedlicher Platzierung des Sternchen-Platzhalters")

>[!NOTE]
>
>Die App zeigt die Assets an, indem sie die Suchkriterien über mehrere Metadatenfelder hinweg und nicht nur den Titel oder Dateinamen des Assets abgleicht.

## Öffnen von Assets auf Ihrem Desktop {#openondesktop-v2}

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

### Verwalten von Sonderzeichen in Asset-Namen {#special-characters-in-filename}

Im alten Programm behielten die im Repository erstellten Knotennamen die Leerzeichen und die Groß- und Kleinschreibung der vom Benutzer angegebenen Ordnernamen bei. Damit das aktuelle Programm die Knotennamensregeln der Programmversion 1.10 emulieren kann, aktivieren Sie [!UICONTROL Use legacy conventions when creating nodes for assets and folders] unter [!UICONTROL Preferences]. Weitere Informationen finden Sie in den [Programmvoreinstellungen](/help/using/install-upgrade.md#set-preferences). Diese veraltete Voreinstellung ist standardmäßig deaktiviert.

>[!NOTE]
>
>Das Programm ändert nur die Knotennamen im Repository anhand der folgenden Namenskonventionen. Das Programm behält den `Title` des Assets unverändert bei.

| Zeichen ‡ | Alte Voreinstellung im Programm | Bei Auftreten in Dateinamen | Bei Auftreten in Ordnernamen | Beispiel |
|---|---|---|---|---|
| `. / : [ ] \| *` | Aktiviert oder deaktiviert | Ersetzt durch `-` (Bindestrich). Ein `.` (Punkt) in der Dateinamenerweiterung wird unverändert beibehalten. | Ersetzt durch `-` (Bindestrich). | `myimage.jpg` bleibt unverändert und `my.image.jpg` ändert sich in `my-image.jpg`. |
| `% ; # , + ? ^ { } "` und Leerzeichen | ![deselect icon](assets/do-not-localize/deselect-icon.png) Deaktiviert | Leerzeichen werden beibehalten | Ersetzt durch `-` (Bindestrich). | `My Folder.` ändert sich in `my-folder-`. |
| `# % { } ? & .` | ![deselect icon](assets/do-not-localize/deselect-icon.png) Deaktiviert | Ersetzt durch `-` (Bindestrich). | Nicht vorhanden. | `#My New File.` ändert sich in `-My New File-`. |
| Großbuchstaben | ![deselect icon](assets/do-not-localize/deselect-icon.png) Deaktiviert | Groß- und Kleinschreibung wird unverändert beibehalten. | In Kleinbuchstaben geändert. | `My New Folder` ändert sich in `my-new-folder`. |
| Großbuchstaben | ![selection checked icon](assets/do-not-localize/selection-checked-icon.png) Aktiviert | Groß- und Kleinschreibung wird unverändert beibehalten. | Groß- und Kleinschreibung wird unverändert beibehalten. | Nicht vorhanden. |

‡ Die Liste der Zeichen ist eine durch Leerzeichen getrennte Liste.

## Suchen aller bearbeiteten Bilder {#find-all-edited-images}

Das Programm bietet eine Ansicht mit der Bezeichnung **[!UICONTROL Edited locally]**, mit der Sie schnell auf alle Dateien zugreifen können, die Sie lokal heruntergeladen haben (über die Aktionen [!UICONTROL Open] oder [!UICONTROL Edit]) und die dann geändert wurden. Mit dem Programm können Sie alle lokal bearbeiteten Assets auswählen und die Änderungen mit wenigen Klicks hochladen. In dieser Ansicht werden auch die lokal bearbeiteten Assets angezeigt, die einen Bearbeitungskonflikt haben.

![Filtern Sie, um alle lokal bearbeiteten Assets anzuzeigen](assets/edited_locally_filter_da2.png " Filtern Sie beispielsweise, um alle lokal bearbeiteten Assets für einen Massen-Upload von Bearbeitungen anzuzeigen")

## Nächste Schritte {#next-steps}

* [Video zu den ersten Schritten mit dem Adobe Experience Manager Desktop-Programm ansehen](https://experienceleague.adobe.com/de/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app)

* Geben Sie Feedback zur Dokumentation über [!UICONTROL Edit this page] ![Bearbeiten der &#x200B;](assets/do-not-localize/edit-page.png)) oder [!UICONTROL Log an issue] ![Erstellen eines GitHub-](assets/do-not-localize/github-issue.png) in der rechten Seitenleiste

* Kontaktieren Sie die [Kundenunterstützung](https://experienceleague.adobe.com/de?support-solution=General#support)

>[!MORELIKETHIS]
>
>* [Grundlegendes zur Benutzeroberfläche](/help/using/user-interface.md)
>* [Verwenden des -Desktop-Programms](/help/using/using-desktop-app.md)
>* [Verwalten von Assets im Desktop-Programm](/help/using/assets-management-tasks.md)
