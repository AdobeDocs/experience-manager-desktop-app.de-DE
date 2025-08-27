---
title: Hochladen von Assets mit dem  [!DNL Experience Manager] -Desktop-Programm
description: Hochladen von Assets mit dem  [!DNL Adobe Experience Manager] -Desktop-Programm
feature: Desktop App,Asset Management
exl-id: f082c712-dc04-4bed-bac8-fa78f93de1c7
source-git-commit: db592420ded4d2f7288982a1ea17618484c82537
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 74%

---

# Hochladen von Assets {#upload-assets}

Benutzende des AEM-Desktop-Programms, die berechtigt sind, Assets hinzuzufügen, können Assets (z. B. Bilder, Dokumente, Videos oder andere Medien) hinzufügen.

## Bearbeiten von Assets und Hochladen aktualisierter Assets in [!DNL Experience Manager] {#edit-assets-upload-updated-assets}

Öffnen Sie Assets zur Bearbeitung, wenn Sie Änderungen vornehmen möchten, und laden Sie die aktualisierten Assets auf den [!DNL Experience Manager] hoch. Um Konflikte mit Bearbeitungen anderer Benutzer zu vermeiden, verwenden Sie das Programm, um eine Bearbeitungssitzung zu starten. Bevor Sie mit der Bearbeitung beginnen, stellen Sie sicher, dass das Asset kein Sperrsymbol enthält, das angibt, dass ein anderer Benutzer das Asset bearbeitet.

Um ein Asset zu bearbeiten, suchen Sie nach dem Asset oder navigieren Sie zum Speicherort des Assets. Klicken Sie auf ![Mehr](assets/do-not-localize/more2_da2.png) und dann auf **[!UICONTROL Edit]**.

Verwenden Sie **[!UICONTROL Toggle Check-out]** zum Sperren des Assets, um Konflikte mit Bearbeitungen anderer Benutzer in den beiden folgenden Situationen zu vermeiden:

* Sie haben begonnen, ein Asset zu bearbeiten, ohne es vorher auszuchecken (indem Sie es einfach öffnen).
* Sie möchten demnächst mit der Bearbeitung eines Assets beginnen und möchten nicht, dass andere Benutzer es bearbeiten.

Nachdem Sie die Bearbeitungen vorgenommen haben, zeigt die App den Status **[!UICONTROL Edited Locally]** für geänderte Assets an. Alle in den Assets gespeicherten Änderungen sind nur lokal verfügbar, bis Sie die Änderungen in [!DNL Experience Manager] hochladen. Um einzelne Assets oder einige Assets einzeln hochzuladen, klicken Sie in den Optionen für ein Asset auf **[!UICONTROL Upload Changes]**. Dadurch wird eine Version des Assets in [!DNL Experience Manager] erstellt. Über die Web-Oberfläche von [!DNL Assets] können Sie den Asset-Verlauf in der [Zeitleisten-Ansicht“ ](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/using/activity-stream).

![Option zum Hochladen von Änderungen im Programm](assets/upload_changes_single1_da2.png "Option zum Hochladen von Änderungen im Programm")

![Option zum Hochladen von Änderungen beim Anzeigen einer großen Vorschau eines Assets](assets/upload_changes_single2_da2.png "Option zum Hochladen von Änderungen beim Anzeigen einer großen Vorschau eines Asset")

Best Practices für die gemeinsame Bearbeitung finden Sie unter [Erweiterter Workflow: Zusammenarbeit an denselben Dateien und Vermeidung von Bearbeitungskonflikten](#adv-workflow-collaborate-avoid-conflicts).

In den folgenden Fällen möchten Sie Ihre Änderungen und Bearbeitungen am lokalen Asset vielleicht verwerfen. Klicken Sie auf **[!UICONTROL Discard Changes]**.

* Wenn Sie Ihre Änderungen nicht lokal in [!DNL Experience Manager] speichern möchten.
* Sie nehmen Änderungen am ursprünglichen Asset vor, nachdem Sie einige Änderungen gespeichert haben.
* Sie stoppen die Bearbeitung des Assets, da es nicht mehr benötigt wird.

Deaktivieren Sie ggf. das Auschecken. Das aktualisierte Asset wird aus dem lokalen Cache-Ordner entfernt und erneut heruntergeladen, wenn Sie es bearbeiten oder öffnen.

## Hochladen und Hinzufügen neuer Assets zu [!DNL Experience Manager] {#upload-and-add-new-assets-to-aem}

Benutzer können dem DAM-Repository neue Assets hinzufügen. Vielleicht sind Sie z. B. ein Agenturfotograf oder -auftragnehmer, der eine große Anzahl von Fotos aus einem Foto-Shooting zum [!DNL Experience Manager]-Repository hinzufügen möchte. Um [!DNL Experience Manager] neue Inhalte hinzuzufügen, wählen Sie ![die Option „In Cloud hochladen“](assets/do-not-localize/upload_to_cloud_da2.png) in der oberen Leiste des Programms aus. Navigieren Sie zu den Asset-Dateien im lokalen Dateisystem und klicken Sie auf **[!UICONTROL Select]**. Alternativ können Sie Assets hochladen, indem Sie die Dateien oder Ordner in die Benutzeroberfläche des Programms ziehen. Wenn Sie unter Windows Assets auf einen Ordner innerhalb des Programms ziehen, werden die Assets in den Ordner hochgeladen. Wenn das Hochladen länger dauert, zeigt das Programm eine Fortschrittsleiste an.

<!-- ![Download progress bar for large-sized assets](assets/upload_status_da2.png "Download progress bar for large-sized assets")
-->

Sie können Ordner oder einzelne Dateien aus Ihrem lokalen Dateisystem hochladen. Die Hierarchie eines Ordners wird beim Hochladen beibehalten. Bevor Sie Assets stapelweise hochladen, lesen Sie [Massen-Uploads](#bulk-upload-assets).

Um die Liste der in einer bestimmten Sitzung übertragenen Assets anzuzeigen, klicken Sie auf **[!UICONTROL View]** > **[!UICONTROL Assets transfers]**. Mit der Liste können Sie die Dateiübertragungen der aktuellen Sitzung anzeigen und schnell überprüfen.

![Liste der übertragenen Assets in einer bestimmten Sitzung](assets/assets_transfered_da2.png "Liste der übertragenen Assets in einer bestimmten Sitzung")

Sie können die gleichzeitigen Uploads (Beschleunigung) mit der Einstellung **[!UICONTROL Preferences]** > **[!UICONTROL Upload acceleration]** steuern. Mehr gleichzeitige Uploads führen zu einer Beschleunigung des Upload-Vorgangs, können jedoch ressourcenintensiv sein und den Prozessor des lokalen Computers stärker auslasten. Wenn Ihr System nur langsam reagiert, starten Sie den Upload-Vorgang mit einer geringeren Anzahl gleichzeitiger Uploads neu.

>[!NOTE]
>
>Die Übertragungsliste ist nicht dauerhaft und steht nicht mehr zur Verfügung, wenn Sie das Programm verlassen und erneut öffnen.

## Massen-Upload von Assets {#bulk-upload-assets}

Benutzer oder Organisationen, wie Fotografen oder Kreativagenturen, können während Aktivitäten wie Fotoshootings, Retuschieren oder der Auswahl aus einem größeren Set zahlreiche lokale Assets erstellen. Diese Aufgaben werden oft außerhalb von [!DNL Experience Manager] ausgeführt. Sie können diese großen lokalen Ordner direkt vom Desktop-Programm in [!DNL Assets] hochladen. Die Ordnerhierarchien bleiben erhalten und alle verschachtelten Unterordner und eingeschlossenen Assets werden hochgeladen. Die hochgeladenen Assets stehen auch anderen Benutzern auf demselben Server sofort zur Verfügung. Assets werden im Hintergrund hochgeladen, sodass der Vorgang nicht an eine Webbrowsersitzung gebunden ist.

![Massen-Upload mehrerer lokaler Ordner von Ihrem Desktop in [!DNL Experience Manager]](assets/upload_local_folders_da2.png "Massen-Upload mehrerer lokaler Ordner von Ihrem Desktop in Experience Manager")

Wenn die erwarteten Änderungen nach dem Upload nicht im Programm übernommen werden, klicken Sie auf das Symbol ![Aktualisieren](assets/do-not-localize/refresh.png).

>[!NOTE]
>
>Verwenden Sie nicht die Upload-Funktion, um Assets über zwei [!DNL Experience Manager]-Bereitstellungen zu migrieren. Siehe stattdessen auch [Migrationshandbuch](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/administer/assets-migration-guide).

## Nächste Schritte {#next-steps}

* [Video zu den ersten Schritten mit dem Adobe Experience Manager Desktop-Programm ansehen](https://experienceleague.adobe.com/en/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app)

* Geben Sie Feedback zur Dokumentation über [!UICONTROL Edit this page] ![Bearbeiten der ](assets/do-not-localize/edit-page.png)) oder [!UICONTROL Log an issue] ![Erstellen eines GitHub-](assets/do-not-localize/github-issue.png) in der rechten Seitenleiste

* Kontaktieren Sie die [Kundenunterstützung](https://experienceleague.adobe.com/de?support-solution=General#support)

>[!MORELIKETHIS]
>
>* [Herunterladen von Assets](/help/using/download-assets.md)
>* [Grundlegendes zur Benutzeroberfläche](/help/using/user-interface.md)
>* [Suchen](/help/using/search.md)
