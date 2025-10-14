---
title: Verwenden des  [!DNL Experience Manager] -Desktop-Programms
description: Verwenden Sie das  [!DNL Adobe Experience Manager] -Desktop-Programm, um mit [!DNL Adobe Experience Manager] DAM-Assets direkt von Ihrem Win- oder Mac-Desktop aus zu arbeiten und sie in anderen Programmen zu verwenden.
feature: Desktop App,Asset Management
source-git-commit: c5aeee9ab636ba7bedff4225172140d59cfe627d
workflow-type: tm+mt
source-wordcount: '1416'
ht-degree: 40%

---


# Assets-Verwaltungsaufgaben in [!DNL AEM Desktop App] {#assets-management-tasks}

Asset-Management umfasst das Organisieren, Verwalten und Optimieren digitaler Assets, um Workflows zu optimieren. Dazu gehören Aufgaben wie das Duplizieren und Umbenennen von Dateien, das Anheften oder Aufheben der Anheftung von Ordnern für den schnellen Zugriff und das Anzeigen von Assets in verschiedenen Layouts. Dies verbessert die Effizienz, vereinfacht die Asset-Verfolgung und stellt sicher, dass digitale Assets plattformübergreifend einfach abgerufen und organisiert werden können.

## Anzeigen von Assets {#view-assets}

Mit dem AEM-Desktop-Programm können Sie Assets in vier verschiedenen Ansichten anzeigen:

* **[!UICONTROL Show Assets]:** Ermöglicht die Anzeige aller Assets.
* **[!UICONTROL Show Collections]:** Ermöglicht die Anzeige aller in der nativen AEM-Anwendung erstellten Sammlungen. Weitere Informationen [Sammlungen](#collections-desktop-app).
* **[!UICONTROL Edited Locally]:** Zeigt alle lokal geänderten Assets an. In dieser Ansicht können Sie mehrere Assets hinzufügen und hochladen.
* **[!UICONTROL Asset transfers]:** Ermöglicht die Anzeige aller Assets, die von der nativen Mobile App an die lokale App übertragen werden oder umgekehrt.
* **[!UICONTROL Pinned items]:** Ermöglicht die Anzeige aller angehefteten Elemente.

Führen Sie die folgenden Schritte aus, um zwischen verschiedenen Ansichten von Assets in der AEM Desktop-Anwendung zu wählen:

1. Öffnen Sie das AEM-Desktop-Programm.

1. Gehen Sie zur Ansicht Dropdown-Liste oben rechts. Eine der verfügbaren Ansichten auswählen.

   ![Ordner anheften oder entfernen](assets/view-pinned-assets.png)

## Anzeigen neu hinzugefügter Ordner und Dateien {#view-newly-added-files-folders}

Sie können neu erstellte Assets von Ihrem lokalen Computer in AEM hochladen, wo das zentrale Repository gespeichert wird. Um diese neu erstellten Assets lokal anzuzeigen, gehen Sie zum Dropdown-Menü **[!UICONTROL View]** und wählen Sie **[!UICONTROL Show Assets]** aus, um alle Aktualisierungen mit ihrer Zeitleiste und ihrem Titel anzuzeigen, oder wählen Sie **[!UICONTROL Edited Locally]** aus. Beide Optionen zeigen die lokal bearbeiteten Assets explizit an.

## Dateien duplizieren {#duplicate-files}

Wenn Sie eine Originaldatei beibehalten und Änderungen an der ähnlichen Datei vornehmen möchten, können Sie Dateien an verschiedenen Speicherorten (lokal und Cloud) gleichzeitig duplizieren. Dies kann durch den Vorgang „Dateien duplizieren“ über Assets hinweg erreicht werden.

Gehen Sie wie folgt vor, um Dateien im AEM-Desktop-Programm zu duplizieren:

1. Navigieren Sie zu einem Ordner und wählen Sie das Asset aus, das Sie duplizieren möchten.

   ![Weitere Optionen](assets/more-options1.png)

1. Klicken Sie auf **[!UICONTROL More actions]** ![Symbol Mehr Aktionen](assets/do-not-localize/more2_da2.png) und wählen Sie ![Symbol duplizieren](assets/do-not-localize/duplicate.svg) **[!UICONTROL Duplicate File]** Aktion aus.

1. Die doppelte Datei wird mit einem identischen Dateinamen und Inhalt erstellt.

## Titel eines Assets oder Ordners umbenennen {#rename-asset-title}

Gehen Sie wie folgt vor, um den Titel eines Assets oder Ordners umzubenennen:

1. Durchsuchen Sie das Asset, das Sie umbenennen möchten. Beim Benennen eines Ordners sind Sonderzeichen wie `\ / : * ?  | < > [ ] %`; nicht zulässig. Wenn enthalten, werden sie automatisch durch einen Bindestrich `-`.

1. Klicken Sie auf **[!UICONTROL More actions]** ![Symbol Mehr Aktionen](assets/do-not-localize/more2_da2.png) und wählen Sie **[!UICONTROL Rename]** aus, um den gewünschten Titel eines Assets hinzuzufügen.


## Ordner anheften oder entfernen {#pin-unpin-folder}

Angeheftete Ordner werden automatisch synchronisiert, um alle Änderungen widerzuspiegeln, die nativ in der App vorgenommen wurden. Für den Schnellzugriff können Sie einen Ordner anheften oder entfernen, indem Sie die folgenden Schritte ausführen:

1. Durchsuchen Sie das Asset, das Sie anheften oder entfernen möchten.

1. Klicken Sie auf **[!UICONTROL More actions]** ![Symbol Mehr Aktionen](assets/do-not-localize/more2_da2.png) und wählen Sie [!UICONTROL pin] aus, um das Asset oder den Ordner anzuheften. Klicken Sie alternativ auf [!UICONTROL unpin] , um die Anheftung aufzuheben.

   ![Ordner anheften oder entfernen](assets/pin-unpin.png)

## Auto refresh {#auto-refresh}

Die Funktion zur automatischen Aktualisierung aktualisiert Inhalte automatisch in Echtzeit, sodass Sie immer die neuesten Informationen sehen, ohne die Seite manuell neu laden zu müssen. Führen Sie die folgenden Schritte aus, um Assets automatisch zu aktualisieren und die Liste der aktualisierten Assets zu erhalten:

1. Öffnen Sie das AEM-Desktop-Programm.

1. Klicken Sie ![Aktualisierungssymbol](assets/do-not-localize/refresh.png) in der Menüleiste, um die Aktualisierungen abzurufen.

## Sammlungen {#collections-desktop-app}

Mit dem AEM-Desktop[Programm können Sie Sammlungen anzeigen](#view-collections-desktop-app) [&#x200B; herunterladen &#x200B;](#download-collections-desktop-app) durchsuchen, die in [!DNL Adobe Experience Manager Assets] Programm erstellt wurden.

### Anzeigen von Sammlungen {#view-collections-desktop-app}

Führen Sie die folgenden Schritte aus, um Sammlungen in der Desktop-Anwendung anzuzeigen:

1. Öffnen Sie das AEM-Desktop-Programm und navigieren Sie zu [Assets anzeigen](#view-assets).

1. Wählen Sie **[!UICONTROL Show Collections]** aus. Die im nativen Programm verfügbaren Sammlungen werden angezeigt.

   ![Sammlungen - Desktop-Programm](assets/collections-desktop-app.png)

### Herunterladen von Sammlungen {#download-collections-desktop-app}

Führen Sie die folgenden Schritte aus, um Sammlungen in der Desktop-Anwendung herunterzuladen:

1. Führen Sie die Schritte 1 und 2 aus, wie in [Sammlungen anzeigen](#view-collections-desktop-app).

1. Navigieren Sie zu Mehr Aktionen ![Symbol Mehr Aktionen](assets/do-not-localize/more2_da2.png) in der Sammlung, die Sie herunterladen möchten.

1. Klicken Sie auf **[!UICONTROL Download]** , um die jeweilige Sammlung herunterzuladen.

## Erstellen eines Ordners mit einem Metadatenschema {#create-folder-with-metadata-schema}

Mit dem AEM-Desktop-Programm können Sie beim Erstellen eines neuen Ordners Metadaten zuweisen. Führen Sie dazu die folgenden Schritte aus:

1. Wechseln Sie zum Symbol Verzeichnis erstellen ![Symbol Ordner hinzufügen](assets/do-not-localize/add-folder.svg). **[!UICONTROL Create Directory]** Bildschirm wird angezeigt.

1. Fügen Sie die folgenden Details hinzu:
   * **[!UICONTROL Name]** des Ordners.
   * Wählen Sie **[!UICONTROL Folder Metadata Schema]** die Metadatenhierarchie des Ordners aus oder wählen Sie **[!UICONTROL none]** aus, wenn Sie keine Metadaten mit dem Ordner verknüpfen möchten.

1. Klicken Sie auf **[!UICONTROL OK]** , um fortzufahren.

## Liste der übertragenen Assets {#list-of-transferred-assets}

Informationen zum Anzeigen der Liste der in einer bestimmten Sitzung übertragenen Assets finden Sie unter [Hochladen von Assets in [!DNL Experience Manager]](#upload-and-add-new-assets-to-aem).

## Erweiterter Workflow: Zusammenarbeit an denselben Dateien und Vermeidung von Bearbeitungskonflikten {#adv-workflow-collaborate-avoid-conflicts}

In kollaborativen Umgebungen können mehrere Benutzer an denselben Assets arbeiten, was zu Versionierungskonflikten führen kann. Um Konflikte zu vermeiden, befolgen Sie die folgenden Best Practices:

* Bearbeiten Sie keine Assets, indem Sie auf [!UICONTROL Open] klicken. Bearbeiten Sie die lokal heruntergeladenen Assets nicht, indem Sie sie aus Ihrem Dateisystemordner öffnen. Andere Benutzer wissen nicht, dass das Asset gerade bearbeitet wird.
* Um ein Asset zu bearbeiten, klicken Sie immer auf [!UICONTROL Edit]. Dadurch wird das Asset im nativen Programm geöffnet und dem Asset ein Sperrsymbol hinzugefügt, sodass die anderen Benutzer wissen, dass das Asset bearbeitet wird.
* Klicken Sie auf [!UICONTROL Toggle Check-in], wenn Sie versehentlich mit der Bearbeitung beginnen, ohne auf [!UICONTROL Edit] geklickt zu haben. Diese Funktion fügt dem Asset ein Sperrsymbol hinzu. Wenn Sie ein Asset später bearbeiten möchten, andere es bis dahin aber nicht bearbeiten sollen, klicken Sie auf [!UICONTROL Toggle Check-in], um es zu sperren.
* Bevor Sie ein Asset bearbeiten, stellen Sie sicher, dass es nicht von anderen Benutzern bearbeitet wird. Suchen Sie nach dem Sperrsymbol für das Asset.
* Laden Sie nach Abschluss der Änderungen alle Änderungen hoch und checken Sie das Asset ein.

![Status von Bearbeitungskonflikten](assets/edits_conflicts_status_da2.png "Status von Bearbeitungskonflikten")

Wenn ein lokal heruntergeladenes Asset auf dem [!DNL Experience Manager]-Server aktualisiert wird, zeigt das Programm den Status **[!UICONTROL Modified remotely]** an. Sie können entweder Ihre lokale Kopie entfernen oder Ihre lokale Kopie aktualisieren, indem Sie auf [!UICONTROL Remove] bzw. [!UICONTROL Update] klicken. Über Links im Dialogfeld können Sie beide Versionen des Assets anzeigen.

![Optionen zum Beheben des Konflikts, wenn das Asset remote bearbeitet wird](assets/modified_remotely_dialog_da2.png "Optionen zum Beheben des Konflikts, wenn das Asset remote bearbeitet wird")

Wenn ein lokal bearbeitetes Asset auch ohne Ihr Wissen auf dem Server aktualisiert wurde, zeigt das Programm den Status **[!UICONTROL Editing Conflict]** an. Sie können eine Version der Änderungen beibehalten – entweder Sie behalten Ihre Aktualisierungen bei (klicken Sie auf **[!UICONTROL Keep Mine]**) und löschen die Bearbeitung der anderen Person oder Sie übernehmen die Aktualisierungen der anderen Person und löschen Ihre (**[!UICONTROL Overwrite Mine]**).

![Optionen zum Beheben eines Bearbeitungskonflikts](assets/editing_conflict_dialog_da2.png "Optionen zum Beheben eines Bearbeitungskonflikts")

## Erweiterter Workflow: Platzieren und Verknüpfen von Assets in einer InDesign-Datei {#adv-workflow-place-assets-indesign}

Wenn Sie das [!DNL Experience Manager]-Desktop-Programm verwenden, um Dateien mit verknüpften Assets zu öffnen, werden die Assets vorab heruntergeladen und in den nativen Programmen angezeigt. Damit dieser Workflow funktioniert, muss Ihr natives Programm das Platzieren von Links zu lokalen Assets unterstützen und [!DNL Experience Manager] muss die Auflösung dieser Links in den Binärdateien zu Server-seitigen Verweisen unterstützen.

Das [!DNL Experience Manager]-Desktop-Programm unterstützt diesen Workflow mit einigen ausgewählten Adobe Creative Cloud-Desktop-Programmen und -Dateiformaten - Adobe InDesign, Adobe Illustrator und Adobe Photoshop. Mit dem Workflow können Sie effizient mit den unterstützten Creative Cloud-Dateien arbeiten. Wenn Benutzer A Assets zu einer InDesign-Datei hinzufügt und in [!DNL Experience Manager] eincheckt, kann Benutzer B die Assets in der Datei sehen, obwohl sie nicht Teil der Datei sind. Die Assets werden lokal auf den Computer von Benutzer B heruntergeladen.

>[!NOTE]
>
>Das Desktop-Programm kann jedem Laufwerk unter Windows zugeordnet werden. Für reibungslose Nutzung sollten Sie eine Änderung des Standard-Laufwerksbuchstabens jedoch vermeiden. Wenn Benutzer derselben Organisation unterschiedliche Laufwerksbuchstaben verwenden, können sie die von anderen platzierten Assets nicht sehen. Die platzierten Assets werden nicht abgerufen, wenn sich der Pfad ändert. Die platzierten Assets bleiben weiterhin in der Binärdatei (z. B. INDD) und werden nicht entfernt.

Informationen zu den Einschränkungen dieses Workflows finden Sie in den [Systemanforderungen und unterstützten Versionen](release-notes.md).

Gehen Sie wie folgt vor, um diesen Workflow mit einem Bild-Asset und InDesign auszuprobieren:

1. Halten Sie eine INDD-Datei mit platzierten Assets in [!DNL Experience Manager] bereit. Informationen zum Erstellen einer solchen INDD-Datei finden Sie unter [Platzieren von Grafiken](https://helpx.adobe.com/de/indesign/using/placing-graphics.html).
1. **[!UICONTROL Edit]** Sie im -Desktop-Programm die INDD-Datei mit platzierten Assets in [!DNL Experience Manager].
1. Die App lädt die InDesign-Datei und die verknüpften Assets herunter. Wenn InDesign das Dokument öffnet, werden die Verknüpfungen aufgelöst, Assets werden heruntergeladen und die Assets werden im InDesign-Dokument angezeigt.
1. Um eine neue Grafik in der InDesign-Datei zu platzieren, verwenden Sie die **[!UICONTROL Reveal File]**-Aktion für das Asset. Die Aktion lädt das Asset lokal herunter und öffnet den Speicherort für die lokale Netzwerkfreigabe in Windows Explorer oder Mac Finder.
1. Platzieren Sie das angezeigte Asset im InDesign-Dokument. Dadurch wird ein Link im Dokument erstellt.
1. Nachdem Sie die Änderungen im InDesign-Dokument abgeschlossen haben, speichern Sie es und laden Sie es mit dem Desktop-Programm in [!DNL Experience Manager] hoch.

## Nächste Schritte {#next-steps}

* [Video zu den ersten Schritten mit dem Adobe Experience Manager Desktop-Programm ansehen](https://experienceleague.adobe.com/de/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app)

* Geben Sie Feedback zur Dokumentation über [!UICONTROL Edit this page] ![Bearbeiten der &#x200B;](assets/do-not-localize/edit-page.png)) oder [!UICONTROL Log an issue] ![Erstellen eines GitHub-](assets/do-not-localize/github-issue.png) in der rechten Seitenleiste

* Kontaktieren Sie die [Kundenunterstützung](https://experienceleague.adobe.com/de?support-solution=General#support)

<!--* Provide product feedback using the [!UICONTROL Feedback] option available on the AEM Desktop App user interface>-->

>[!MORELIKETHIS]
>
>* [Grundlegendes zur Benutzeroberfläche](/help/using/user-interface.md).
>* [Erste Schritte](/help/using/get-started.md).
