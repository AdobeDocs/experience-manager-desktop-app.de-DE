---
title: Erste Schritte [!DNL Experience Manager] Desktop-Programm
description: Erfahren Sie, wie  [!DNL Experience Manager]  Desktop-Programm die Inhaltserstellung und -veröffentlichung mit optimierten Workflows und Produktivitätsfunktionen verbessert.
feature: Desktop App,Asset Management
exl-id: 6cf29b6a-74e6-4860-a25b-d3e91abbaa9d
source-git-commit: a579ab861aa0af8c8415a0f38126de7f33c7a7b3
workflow-type: tm+mt
source-wordcount: '1213'
ht-degree: 42%

---

# Erste Schritte mit [!DNL Adobe Experience Manager] Desktop-Programm {#getting-started-desktop-app}

Verwenden Sie das [!DNL Adobe Experience Manager]-Desktop-Programm, um auf digitale Assets zuzugreifen, die in einem [!DNL Adobe Experience Manager] DAM-Repository auf Ihrem lokalen Desktop gespeichert sind. Sie können diese Assets dann in beliebigen Desktop-Programmen verwenden. Sie können die Assets lokal in Desktop-Programmen öffnen und bearbeiten. Nachdem Sie Änderungen vorgenommen haben, laden Sie sie mit der Versionskontrolle wieder in [!DNL Experience Manager] hoch, um Aktualisierungen für andere Benutzer freizugeben. Sie können auch neue Dateien und Ordnerhierarchien in [!DNL Experience Manager] hochladen, Ordner erstellen und Assets oder Dateien aus dem [!DNL Experience Manager]-DAM löschen.

Die Integration ermöglicht es verschiedenen Rollen im Unternehmen, die Assets zentral in [!DNL Experience Manager Assets] zu verwalten und auf die Assets auf dem lokalen Desktop in den nativen Programmen unter Windows oder macOS zuzugreifen.

Wenn Sie das Programm nach dem Abmelden oder zum ersten Mal öffnen, müssen Sie die URL des [!DNL Experience Manager]-Servers im Format `https://[aem-server-url]:[port]/` angeben. Wählen Sie dann die Option [!UICONTROL Connect] aus. Geben Sie Ihre Anmeldeinformationen ein, um das Programm mit dem Server zu verbinden.

>[!VIDEO](https://video.tv.adobe.com/v/28868?quality=12&learn=on)

Die wichtigsten Aufgaben, die Sie mit dem [!DNL Adobe Experience Manager]-Desktop-Programm durchführen, sind:

![Workflows und Aufgaben, die Sie mit [!DNL Experience Manager] Desktop-Programm erledigen können](assets/aem_desktop_app_usecases_v2.png)

## Funktionsweise des Desktop-Programms {#how-app-works2}

Bevor Sie mit der Verwendung der Anwendung beginnen, verstehen [, wie die App funktioniert](release-notes.md#how-app-works). Machen Sie sich auch mit den folgenden Begriffen vertraut:

* **[!UICONTROL Desktop Actions]**: Über die Assets-Web-Benutzeroberfläche können Sie von innerhalb eines Browsers aus die Asset-Speicherorte erkunden oder das Asset auschecken und öffnen, um es in Ihrem nativen Desktop-Programm zu bearbeiten. Diese Aktionen sind über die Web-Benutzeroberfläche verfügbar und verwenden die Funktionen des -Desktop-Programms.

* Dateistatus **[!UICONTROL Cloud Only]**: Solche Assets werden nicht auf den lokalen Computer heruntergeladen und stehen nur auf dem [!DNL Experience Manager]-Server zur Verfügung.

* Dateistatus **[!UICONTROL Available locally]**: Die Assets werden wie bisher heruntergeladen und stehen auf dem lokalen Computer zur Verfügung. Die Assets werden nicht geändert.

* Dateistatus **[!UICONTROL Edited locally]**: Diese Assets werden lokal geändert und die Änderungen bleiben beim Hochladen auf den [!DNL Experience Manager]-Server erhalten. Nach dem Hochladen ändert sich der Status in [!UICONTROL Available locally]. Siehe [Bearbeiten von Assets](upload-assets.md#edit-assets-upload-updated-assets).

* Dateistatus ist **[!UICONTROL Editing conflict]**: Wenn Sie und andere Benutzer ein Asset gleichzeitig bearbeiten, zeigt das Programm an, dass ein Bearbeitungskonflikt aufgetreten ist. Das Programm bietet außerdem Optionen zum Beibehalten oder Verwerfen Ihrer Änderungen. Erfahren Sie, [wie Sie Bearbeitungskonflikte vermeiden](assets-management-tasks.md#adv-workflow-collaborate-avoid-conflicts).

* Dateistatus **[!UICONTROL Modified remotely]**: das Programm zeigt an, ob ein Asset, das Sie heruntergeladen haben, auf dem [!DNL Experience Manager]-Server geändert wurde. Das Programm bietet auch die Möglichkeit, die neueste Version herunterzuladen und Ihre lokale Kopie zu aktualisieren. Erfahren Sie, [wie Sie Bearbeitungskonflikte vermeiden](assets-management-tasks.md#adv-workflow-collaborate-avoid-conflicts).

* **[!UICONTROL Check-out]**: Wenn Sie eine Datei bearbeiten oder eine Datei bearbeiten möchten, können Sie den Status „Auschecken“ aktivieren. Dadurch wird dem Asset in der App und [!DNL Experience Manager] Web-Oberfläche ein Sperrsymbol hinzugefügt. Das Sperrsymbol zeigt anderen Benutzern an, dass sie dasselbe Asset nicht gleichzeitig bearbeiten sollen, da dies zu einem Bearbeitungskonflikt führt.

* **[!UICONTROL Check-in]**: Markieren Sie das Asset als sicher, damit andere Benutzer es bearbeiten können, ohne dass ein Bearbeitungskonflikt entsteht. Wenn Sie Ihre Änderungen hochladen, wird das Sperrsymbol automatisch entfernt. Durch Umschalten des Eincheckstatus wird auch das Sperrsymbol entfernt. Adobe empfiehlt jedoch, das manuelle Einchecken zu vermeiden, ohne die Änderungen hochzuladen. Wenn Sie Ihre Änderungen verwerfen, können Sie den Status „Einchecken“ manuell deaktivieren.

* Aktion **[!UICONTROL Open]**: Öffnen Sie einfach das Asset zur Vorschau im nativen Programm. Adobe empfiehlt, das Bearbeiten des Assets mithilfe dieser Aktion zu vermeiden. Der Grund dafür ist, dass das Asset nicht ausgecheckt wird. In der Zwischenzeit können andere Benutzer Änderungen vornehmen, die zu Bearbeitungskonflikten führen.

* Aktion **[!UICONTROL Edit]**: Verwenden Sie die Aktion, um das Bild zu ändern. Durch Klicken auf [!UICONTROL Edit] wird das Asset ausgecheckt und dem Asset wird ein Sperrsymbol hinzugefügt. Wenn Sie nach dem Klicken auf „Edit“ (Bearbeiten) das Asset nicht bearbeiten möchten, klicken Sie auf [!UICONTROL Toggle check-in]. Verwenden Sie zum Löschen, Umbenennen oder Verschieben von Assets in der [!DNL Experience Manager] DAM-Ordnerhierarchie die Aktionen der [!DNL Experience Manager]-Web-Oberfläche und nicht die Aktion „Bearbeiten“.

* Aktion **[!UICONTROL Download]**: Laden Sie das Asset auf Ihren lokalen Computer herunter. Sie können die Assets jetzt herunterladen und später bearbeiten. Arbeiten Sie offline und laden Sie die Änderungen später hoch. Assets werden in einen Cache-Ordner auf Ihrem Dateisystem heruntergeladen.

* **[!UICONTROL Reveal File]** oder **[!UICONTROL Reveal Folder]** Aktion: Während die Assets in einen lokalen Cache-Ordner heruntergeladen werden, ahmt die App ein lokales Netzlaufwerk nach. Es wird ein lokaler Pfad für jedes Asset bereitgestellt. Um diesen Pfad zu ermitteln, verwenden Sie die entsprechende Einblendeoption im Programm. Zum Platzieren von Assets im Creative Cloud-Programm ist die Aktion „Reveal“ (Anzeigen) erforderlich. Siehe [Platzieren von Assets](search.md#place-assets-in-native-documents).

* **[!UICONTROL Open In Web]**: Um das Asset in der [!DNL Experience Manager] Web-Oberfläche anzuzeigen, öffnen Sie es im Web. Sie können über die [!DNL Experience Manager] weitere Workflows initiieren, z. B. die Aktualisierung von Metadaten oder die Asset-Erkennung.

* Aktion **[!UICONTROL Delete]**: Löschen Sie das Asset aus dem [!DNL Experience Manager]-DAM-Repository. Durch die Aktion wird die Originalkopie des Assets auf dem Experience Manager-Server gelöscht. Wenn Sie nur Änderungen am lokalen Asset verwerfen möchten, finden Sie weitere Informationen unter [Änderungen verwerfen](upload-assets.md#edit-assets-upload-updated-assets).

* **[!UICONTROL Upload Changes]**: Das Desktop-Programm lädt das aktualisierte Asset nur hoch, wenn Sie es explizit auf den [!DNL Experience Manager]-Server hochladen. Wenn Sie Ihre Änderungen speichern, werden diese nur auf Ihrem lokalen Computer gespeichert. Beim Hochladen wird das Asset automatisch eingecheckt und das Sperrsymbol entfernt. Siehe [Bearbeiten von Assets](upload-assets.md#edit-assets-upload-updated-assets).

## Aktivieren von Desktop-Aktionen in [!DNL Experience Manager] Web-Oberfläche {#desktopactions-v2}

Über die [!DNL Assets]-Benutzeroberfläche in einem Browser können Sie zu den Asset-Speicherorten navigieren oder das Asset auschecken und öffnen, um es im Desktop-Programm zu bearbeiten. Diese Optionen werden als [!UICONTROL Desktop Actions] bezeichnet und sind standardmäßig nicht aktiviert. Gehen Sie zur Aktivierung wie folgt vor.

1. Klicken Sie in der [!DNL Assets]-Konsole in der Symbolleiste auf das Symbol **[!UICONTROL User]**.
1. Klicken Sie auf **[!UICONTROL My Preferences]**, um das Dialogfeld **[!UICONTROL Preferences]** anzuzeigen.

1. Wählen Sie im Dialogfeld [!UICONTROL User Preferences] die Option **[!UICONTROL Show Desktop Actions For Assets]** und klicken Sie dann auf **[!UICONTROL Accept]**.

   ![Aktivieren der Option „Desktop-Aktionen für Assets anzeigen“, um Desktop-Aktionen zu ermöglichen](assets/enable_desktop_actions1.png)

## Von der [!DNL Assets] Web-Benutzeroberfläche starten {#adv-workflow-start-from-aem-ui}

Starten Sie bei Bedarf Ihren Workflow über die Assets-Web-Oberfläche. Das Desktop-Programm ist in [!DNL Experience Manager] integriert, damit es bei Bedarf für Desktop-Aktionen genutzt werden kann.

Ein Sonderfall beim Starten eines Workflows über die Web-Benutzeroberfläche ist die Asset-Erkennung. Die Omnisearch-Leiste in der Assets-Benutzeroberfläche bietet eine umfassende und erweiterte Suchfunktion. Möglicherweise möchten Sie zuerst das gewünschte Asset im Web suchen und dann den Workflow in der App mithilfe von [!UICONTROL Desktop Actions] starten. Einige Beispielfälle umfassen das Filtern von Suchergebnissen mithilfe von Facetten, das Auffinden eines bestimmten, von Adobe Stock lizenzierten Assets oder eine von Ihrem Unternehmen implementierte Anpassung, die eine bessere Erkennung über die Web-Oberfläche ermöglicht.

Die Desktop-App-Funktionalität wird verwendet, wenn Sie die folgenden Aktionen in der Assets-Web-Benutzeroberfläche ausführen:

* Die [!UICONTROL Desktop Actions], die [!UICONTROL Open], [!UICONTROL Edit] und [!UICONTROL Reveal] ermöglichen
* [!UICONTROL Upload folder]
* [!UICONTROL Check-out] oder [!UICONTROL check-in]

Beispielsweise sind die Aktionen auf der Web-Benutzeroberfläche, die für ein in der App ausgechecktes Asset verfügbar sind, [!UICONTROL Open], [!UICONTROL Reveal] und [!UICONTROL Check in].

![Desktop-Aktionen in der [!DNL Experience Manager]-](assets/assets_web_actions_da2.png "-Desktop-Aktionen in der Experience Manager-Web-Oberfläche")

>[!NOTE]
>
>Der Browser fordert Sie möglicherweise auf, den Start des [!DNL Adobe Experience Manager]-Desktop-Programms zuzulassen. Um jedes Mal eine unterbrechungsfreie Übertragung vom Browser zur Mobile App zu erhalten, aktivieren Sie das entsprechende Kontrollkästchen, damit die Mobile App die Aufgabe übernehmen kann.

Die folgenden Informationen oder Workflows werden nicht über die Web-Oberfläche gefunden. Verwenden Sie das -Desktop-Programm, da die Web-Oberfläche lokale Änderungen nicht verfolgt und die folgenden Informationen nicht kennt:

* Dateien werden lokal bearbeitet.
* Dateien, die einen Bearbeitungskonflikt aufweisen und eine Möglichkeit haben, ihn zu beheben.
* Laden Sie die lokalen Änderungen in [!DNL Experience Manager] hoch.
* Verschiedene Status der lokal verfügbaren Dateien.

Im Gegenteil, Sie können das Asset über die Web-Oberfläche öffnen, indem Sie in der Desktop-App mit der Aktion **[!UICONTROL Open In Web]** beginnen.

## Nächste Schritte {#next-steps}

* [Video zu den ersten Schritten mit dem Adobe Experience Manager Desktop-Programm ansehen](https://experienceleague.adobe.com/en/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app)

* Geben Sie Feedback zur Dokumentation über [!UICONTROL Edit this page] ![Bearbeiten der &#x200B;](assets/do-not-localize/edit-page.png)) oder [!UICONTROL Log an issue] ![Erstellen eines GitHub-](assets/do-not-localize/github-issue.png) in der rechten Seitenleiste

* Kontaktieren Sie die [Kundenunterstützung](https://experienceleague.adobe.com/de?support-solution=General#support)

>[!MORELIKETHIS]
>
>* [Grundlegendes zur Benutzeroberfläche](/help/using/user-interface.md)
>* [Versionshinweise und bekannte Probleme](/help/using/release-notes.md)
>* [Installieren oder Aktualisieren des Desktop-Programms](/help/using/install-upgrade.md)
