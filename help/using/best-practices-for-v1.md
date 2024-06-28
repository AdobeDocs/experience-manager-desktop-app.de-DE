---
title: Best Practices für das Desktop-Programm, v1.10.
description: Wichtige Funktionen und empfohlene Verwendung der [!DNL Adobe Experience Manager] -Desktop-Programm Version 1.10.
exl-id: 5de06b33-c05c-47eb-b884-408b6f9afc94
source-git-commit: 1c7437786a50eeafa884ce92b745f3438b2d2b88
workflow-type: tm+mt
source-wordcount: '1651'
ht-degree: 49%

---

# Best Practices für das AEM-Desktop-Programm v1.10 {#aem-desktop-app-best-practices}

## Übersicht {#overview}

[!DNL Adobe Experience Manager] Das -Desktop-Programm verknüpft Ihre DAM-Lösung (Digital Asset Management) mit Ihrem Desktop, damit Sie die in der AEM Web-Benutzeroberfläche verfügbaren Dateien direkt auf dem Desktop öffnen können. Wenn Sie ein Asset vom Desktop aus gespeichert haben, wird es an den entsprechenden Speicherort in AEM hochgeladen.

AEM Desktop-Programm eliminiert die Wahrscheinlichkeit, dass Sie falsche lokale Kopien aktualisieren oder ein falsches Asset in AEM aktualisieren. Der benutzerfreundliche Workflow des Desktop-Programms wird mithilfe der Netzwerkfreigabetechnologie aktiviert, die von Desktop-Betriebssystemen bereitgestellt wird.

Das Desktop-Programm stellt das AEM Assets-Repository als Netzwerkfreigabe auf dem Desktop bereit. Daher sieht es so aus, als handle es sich um lokale Ordner und Dateien. Es wird jedoch nicht empfohlen, Digital Asset Management-Vorgänge direkt über den Desktop in der bereitgestellten Netzwerkfreigabe in Finder oder Explorer durchzuführen. Stattdessen empfiehlt Adobe, die AEM Assets-Web-Benutzeroberfläche zu verwenden, um Vorgänge wie das Kopieren oder Verschieben einer großen Anzahl von Assets durchzuführen.

>[!NOTE]
>
>Vor der Lektüre dieses Dokuments können Sie sich die allgemeinen [Best Practices zur AEM- und Creative Cloud-Integration](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/assets/administer/aem-cc-integration-best-practices) durchlesen, wenn Sie sich zunächst einen Überblick über dieses Thema verschaffen möchten.

## Architektur des AEM-Desktop-Programms {#aem-desktop-app-architecture}

Das AEM-Desktop-Programm stellt Netzwerkfreigaben über WebDAV (Windows) oder SMB (Mac) bereit. Die bereitgestellte Netzwerkfreigabe liegt ausschließlich lokal vor. Das AEM-Desktop-Programm fängt die Aufrufe (Öffnen, Lesen, Schreiben) ab und bietet zusätzliches lokales Caching. Das Programm übersetzt Remote-Aufrufe an den AEM Assets-Server in optimierte AEM-HTTP-Anforderungen. Die folgende Abbildung zeigt die Architektur des AEM-Desktop-Programms.

![Architektur des AEM-Desktop-Programms](assets/arch_v1.png)

*Abbildung: Architektur des Desktop-Programms*

Wenn eine Datei gespeichert wird, stellt das zusätzliche Caching beim Schreiben sicher, dass sie zunächst lokal gespeichert wird, sodass der Benutzer nicht auf die Netzwerkübertragung warten kann. Nach einer vordefinierten Verzögerung (30 Sekunden) wird die Datei zunächst im Hintergrund in AEM hochgeladen, woraufhin das Asset in AEM hochgeladen wird. Das AEM-Desktop-Programm verfügt über eine Benutzeroberfläche zum Überwachen des Status von Datei-Uploads im Hintergrund.

## Verwendungsempfehlung für das AEM-Desktop-Programm {#recommended-use-of-aem-desktop-app}

Zu den wichtigsten Funktionen des AEM-Desktop-Programms gehören:

* **Öffnen von Dateien über die AEM Assets-Web-Benutzeroberfläche auf dem Desktop**. Über die Web-Benutzeroberfläche können Sie Assets auf dem Desktop (in Finder, Explorer) anzeigen oder ein Asset mithilfe eines Desktop-Programms öffnen.

* **Auschecken und Einchecken**. Assets kann zur Bearbeitung ausgecheckt werden und wird in AEM Assets als gesperrt markiert. Nach dem Bearbeiten können die Assets dann wieder eingecheckt und damit entsperrt werden.

* **Speichern von Änderungen in Dateien**. Sämtliche Änderungen, die Sie in einer Datei in einer Netzwerkfreigabe speichern, werden automatisch in AEM hochgeladen. Außerdem wird eine neue Version erstellt.

* **Platzieren von verknüpften Assets in anderen Dokumenten**. In Programmen wie Creative Cloud ([!DNL Adobe Photoshop], [!DNL Adobe InDesign] und [!DNL Adobe Illustrator]) können Sie eine externe Datei als Verknüpfung platzieren. Sie können beispielsweise ein Bild in einem InDesign-Dokument platzieren. In diesem Fall können Sie mit der Bereitstellung der Netzwerkfreigabe Assets aus der AEM zur Platzierung durchsuchen und auswählen. Das Platzieren verknüpfter Dateien funktioniert auch in einigen Nicht-Adobe-Apps wie MS® Office.

* **Auflösen von Verweisen in AEM**. Wenn sowohl die platzierten Dateien als auch die Hauptdateien mit dem Link in AEM gespeichert sind, können Server-seitige Informationen zu den Asset-Verweisen automatisch bereitgestellt werden.

* **Zugreifen auf das Asset über den Desktop**. In der bereitgestellten Netzwerkfreigabe bietet ein Kontextmenü eine [!UICONTROL More Info] Dialogfeld (größere Vorschau, wichtige Metadaten) und die Möglichkeit, ein Asset in der AEM-Benutzeroberfläche zu öffnen.

* **Massen-Upload von großen, hierarchischen Ordnern**. Wenn Sie die **Erstellen** > **Ordner-Upload** -Option in AEM Benutzeroberfläche zum Hochladen von Assets lädt das AEM Desktop-Programm die ausgewählte Ordnerhierarchie in den Hintergrund hoch, um sie zu AEM. Der Upload-Fortschritt wird über eine dedizierte Benutzeroberfläche im Desktop-Programm überwacht.

## Unsachgemäße Verwendung des AEM-Desktop-Programms {#inappropriate-use-of-aem-desktop-app}

* Verwenden Sie nicht das AEM-Desktop-Programm, um Assets vom Desktop aus zu verwalten. Das AEM-Desktop-Programm wurde nicht als Ersatz für Netzlaufwerke entwickelt. Verwenden Sie stattdessen die folgenden Funktionen:

   * AEM Assets-Web-Benutzeroberfläche für Digital Asset Management (Suchen oder Freigeben von Assets, Metadaten sowie Kopieren oder Verschieben).

   * [!UICONTROL Folder Upload]-Funktion des AEM-Desktop-Programms für den Uploads von großen, hierarchischen Ordnern.

* Behandeln Sie AEM Desktop-Programm nicht als Client zur Desktop-Synchronisierung für AEM Assets. Der Hauptvorteil des AEM-Desktop-Programms besteht hier darin, dass sie einen „virtuellen“ Zugriff auf das gesamte Repository ermöglicht, während Programme zur Desktop-Synchronisierung normalerweise nur die Assets synchronisieren, die dem jeweiligen Benutzer gehören. AEM Desktop-Programm bietet eine gewisse Zwischenspeicherung und Hintergrund-Upload. Die Funktionsweise unterscheidet sich jedoch stark von typischen Synchronisierungsanwendungen wie dem Adobe Creative Cloud-Desktop-Programm oder Microsoft OneDrive.

* Setzen Sie AEM-Desktop-Programm-Netzlaufwerke nicht zum regelmäßigen Speichern von Assets ein. Alle Speichervorgänge werden an AEM Assets übertragen. Daher ist es unpraktisch, intensive Bearbeitungsvorgänge direkt in dem bereitgestellten AEM Assets-Repository durchzuführen. Wird ein Asset direkt im bereitgestellten Repository bearbeitet, wird die Zeitleiste des Assets mit irrelevanten Versionen „vollgestopft“ und der Server wird durch Mehraufwand belastet.

* Setzen Sie das AEM-Desktop-Programm nicht ein, um große Datenmengen von einer AEM-Instanz zu einer anderen zu migrieren. Informationen zum Planen und Ausführen von Asset-Migrationen finden Sie im [Migrationshandbuch](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/administer/assets-migration-guide). Im Gegensatz dazu ist das Desktop-Programm [unterstützt Massen-Upload](use-app-v1.md#bulkupload) eine große Anzahl von Assets zum ersten Mal in [!DNL Adobe Experience Manager].

## Empfehlungen für ausgewählte Anwendungsfälle {#recommendations-for-selected-use-cases}

### Zugriff auf Assets für kreative Benutzende {#access-to-assets-for-creative-users}

Das AEM-Desktop-Programm ermöglicht einen virtuellen Zugriff auf das gesamte DAM-Repository. Dabei kann es sich für kreative Benutzer als schwierig herausstellen, die richtigen Assets zu finden und auf diese über ihren Desktop zuzugreifen. Wenden Sie diese Best Practices an, um diesen Vorgang für kreative Benutzer zu vereinfachen.

* Verwenden Sie die Funktionen zur Zusammenarbeit der Web-Benutzeroberfläche von AEM Assets, um kreativen Benutzern einen direkteren Zugang zu den richtigen Assets zu ermöglichen. Hierzu gehören etwa die Freigabe von Ordnern oder Sammlungen, die Bereitstellung von Smart-Sammlungen (gespeicherten Suchen) oder der Versand von Benachrichtigungen mit Verweisen zu den richtigen Assets. Kreative Benutzer können dann Desktop-Aktionen in der Web-Benutzeroberfläche verwenden, um schnell auf diese Assets auf ihrem Desktop zugreifen zu können.

* Legen Sie geeignete Berechtigungen für Assets (Zugriffssteuerung) fest, um die Anzeige des DAM-Repositorys für kreative Benutzer zu vereinfachen, indem Sie im Grunde den Zugriff dieser Benutzer auf die benötigten/interessanten Assets beschränken:

   * Bestimmte Bereiche, die für kreative Benutzer keine Relevanz haben, können den entsprechenden Benutzergruppen verweigert werden, damit sie diesen nicht angezeigt werden, auch nicht auf dem Desktop.

   * Die meisten Assets in DAM sind endgültig und nicht zum Ändern vorgesehen. Solche Assets sollten für kreative Benutzer schreibgeschützt sein.

   * Nur Assets, die geändert/überarbeitet werden müssen, sollten mit Schreibzugriff für kreative Benutzer versehen werden. Einige Organisationen verwenden AEM Projekte und die von ihnen erstellten Ordner zum Hosten von Assets, die noch geändert werden können.

### Suchen nach Assets {#searching-assets}

So suchen Sie nach einer Datei, die Sie auf dem Desktop öffnen möchten:

* Suchen Sie das Asset mithilfe der AEM Assets-Web-Benutzeroberfläche. Die Suche in AEM Assets ist nicht nur leistungsstark (Suchfacetten, gespeicherte Suchen), sondern bietet auch zusätzliche Funktionen, um das richtige Asset zu finden. Dazu gehören zusätzliche Filter wie die Möglichkeit, Assets basierend auf dem Status (Genehmigung, Ablauf), Sammlungen, Aufgaben, Benachrichtigungen und die Freigabe von Ordnern/Sammlungen für andere Benutzer/Gruppen zu suchen.

* Nachdem Sie das Asset gefunden haben, verwenden Sie Desktop-Aktionen in AEM Benutzeroberfläche, um auf das Asset auf dem Desktop zuzugreifen.

### Aktualisieren von mit dem AEM-Desktop-Programm geöffneten Assets {#updating-assets-opened-using-aem-desktop-app}

Wenn Sie ein Asset direkt in dem Verzeichnis bearbeiten, das AEM Assets einer lokalen Netzwerkfreigabe zugeordnet hat, wird das Asset bei jedem Speichervorgang auf dem Desktop in AEM hochgeladen. Außerdem erstellt AEM eine Version und generiert Wiedergaben.

Gehen Sie wie folgt vor, wenn ein in AEM gespeichertes Asset aktualisiert werden muss:

* Bei **geringfügigen Aktualisierungen**, etwa Anforderungen kleinerer Überarbeitungen im Genehmigungsprozess:

   * Checken Sie die Datei aus und öffnen Sie sie auf dem Desktop.

   * Aktualisieren Sie die Datei.

   * Speichern Sie die aktualisierte Version. Das Asset wird aktualisiert und in der Zeitleiste wird die ursprüngliche Version zum Vergleich angezeigt.

* Bei **umfassenden Aktualisierungen** wie einer Änderungsanforderung, für die ein kleiner kreativer WIP-Zyklus erforderlich ist:

   * Verwenden Sie die Option Anzeigen , um den entsprechenden Ordner auf dem Desktop zu öffnen.

   * Kopieren Sie die Datei in einen WIP-Ordner außerhalb der zugeordneten AEM Assets-Freigabe. (Kopieren Sie die Datei beispielsweise in einen mit dem Adobe Creative Cloud-Desktop-Programm synchronisierten Ordner.)

   * Arbeiten Sie an der Datei und speichern Sie sie zwischendurch. Die Änderungen werden nicht in AEM Assets gespeichert.

   * Wenn Sie die Bearbeitung abgeschlossen haben, verschieben, kopieren oder speichern Sie die von AEM zugeordnete Datei, um sie als neue Version hochzuladen.

## Netzwerkleistung {#network-performance}

Ein gutes Benutzererlebnis mit dem AEM-Desktop-Programm beruht auf einer stabilen Netzwerkverbindung und einem gut abgestimmten Server, insbesondere für das Hochladen und Aktualisieren von Assets. Diese Empfehlungen gelten für Netzwerk-/IT-Teams von Unternehmen.

### Überlegungen zum Netzwerk {#network-considerations}

Informationen zu Best Practices für die AEM Assets-Netzwerkkonfiguration finden Sie unter [Massen-Migration von Assets](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/administer/assets-migration-guide) Dokument. Zu den wichtigen Aspekten, die zur Optimierung des AEM Desktop-Programm-Erlebnisses für die Benutzer beitragen, zählen:

* **Verwenden eines ordnungsgemäß konfigurierten Dispatcher**. Verwenden Sie die AEM Dispatcher für zusätzliche Sicherheit und stellen Sie sicher, dass sie für [AEM Desktop-Programm-Verbindung hinter einer Dispatcher AEM](install-configure-app-v1.md#connect-to-an-aem-instance-behind-a-dispatcher)

* **Brandeinsparung**. Erwägen Sie, die Symbolvorschau in Finder in Mac zu deaktivieren, wenn Sie das bereitgestellte Repository mit Finder durchsuchen. Der Finder fordert jede Datei an, um eine Vorschau zu generieren, und bewirkt, dass das Desktop-Programm das Asset herunterlädt und lokal zwischenspeichert. Durch die Einsparung von Bandbreite wird auch das Benutzererlebnis für die Benutzer auf dem Desktop verringert. Dies sollte daher bei der Arbeit an Repositorys mit großen Assets oder begrenzter Bandbreite erfolgen.

>[!NOTE]
>
>Um die Symbolvorschau zu deaktivieren, navigieren Sie im Finder zu [!UICONTROL View]auswählen [!UICONTROL View Options]und deaktivieren Sie dann die [!UICONTROL Show icon preview] -Option. Diese Einstellung bezieht sich nur auf den aktuellen Ordner. Um sie standardmäßig festzulegen, klicken Sie im selben Fenster auf die Option [!UICONTROL Use as default].

### Optimieren der Serverleistung {#optimizing-server-performance}

Informationen zur Leistungsoptimierung des AEM Assets-Servers finden Sie unter [Handbuch zur Leistungsoptimierung von AEM Assets](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/administer/performance-tuning-guidelines). Einige wichtige Aspekte im Zusammenhang mit der Server-Leistung des AEM-Desktop-Programms beziehen sich auf das Optimieren der Workflow-Konfiguration für Asset-Uploads:

* **Leistungsstärkere Asset-Uploads**. Konfigurieren Sie die [AEM Workflow-Modell für Asset-Update als vorübergehend](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/administer/performance-tuning-guidelines).

* **Beschränkung der Server-CPU für Uploads**. Stellen Sie sicher, dass der Parameter für die maximalen parallelen Workflow-Aufträge korrekt festgelegt ist, damit bei Uploads nicht die gesamte CPU ausgefüllt wird.
