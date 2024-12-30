---
title: Versionshinweise für das Desktop-Programm, v1.10
description: Versionshinweise, Verbesserungen, neue Funktionen, Kompatibilität und Downloadlinks für das AEM-Desktop-Programm, Version 1.10.
exl-id: 886864e0-016a-4a17-b3ba-4b18a514214a
source-git-commit: 23719d2f5d92f6031687df18036acdbc04722402
workflow-type: tm+mt
source-wordcount: '3989'
ht-degree: 44%

---

# Versionshinweise für das [!DNL Adobe Experience Manager]-Desktop-Programm, Version 1.10. {#aem-desktop-app-release-notes}

Für das AEM-Desktop-Programm v1.x sind die folgenden Download-Links und AEM-Kompatibilitätsinformationen verfügbar:

| Produkte | [!DNL Adobe Experience Manager]-Desktop-Programm |
|--- |--- |
| Version | 1.10 (1.10.0.6 unter Mac und 1.10.0.3 unter Windows) |
| Typ | Nebenversion |
| Datum | 1.10.0.6 (Mac): 15. April 2020; 1.10.0.3 (Win): 31. August 2018 |
| Download-URLs | [macOS X 64 Bit](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-1.10.0.6.dmg); [Windows 32 Bit](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-1.10.0.3.exe); [Windows 64 Bit](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-1.10.0.3.exe) |
| Kompatibilität | AEM 6.5.x; AEM 6.4.x; AEM 6.3 SP2; AEM 6.2 SP1 CFP2+; AEM 6.1 SP2 CFP7+ |

>[!NOTE]
>
>Die Cachegrößenbeschränkung wird nicht erzwungen. Beim Starten des Desktop-Programms wird die Cachegröße einmal berechnet und es wird eine Benachrichtigung angezeigt, wenn sich die Größe der vordefinierten Beschränkung nähert.

## Systemanforderungen und Voraussetzungen {#system-requirements-and-prerequisites}

Das [!DNL Adobe Experience Manager]-Desktop-Programm ist mit den folgenden Betriebssystemen kompatibel:

* macOS X 10.10 oder höher mit den neuesten Fehlerbehebungen.

* Windows 10 mit den aktuellen Service Packs und Fehlerbehebungen.

Adobe empfiehlt die Verwendung der neuesten Version des AEM-Desktop-Programms, um sicherzustellen, dass Sie die neuesten Funktionen, die neuesten Fehlerbehebungen und die bestmögliche Leistung verwenden.

Die AEM-Desktop-App-Version, die Sie auf Ihrem lokalen Computer installieren möchten, erfordert einen bestimmten AEM-Server
Version/Zusätzliche Server-seitige Komponenten (Service Packs, Hotfixes oder Feature Packs). Stellen Sie sicher, dass der AEM-Server ordnungsgemäß konfiguriert ist, bevor Sie zum ersten Mal eine Verbindung herstellen. Wenn Sie Hilfe benötigen, wenden Sie sich an Ihren AEM-Administrator.

Lesen Sie die Informationen in der [detaillierten Kompatibilitätsmatrix](#compatibilitymatrix) am Ende dieses Dokuments, um die Voraussetzungen für Ihr Setup zu prüfen.

## Neue Funktionen im Desktop-Programm, v1.10 {#what-s-new-in-aem-desktop-app}

Das AEM-Desktop-Programm 1.10 konzentriert sich auf die Verbesserung des Benutzererlebnisses rund um den Upload großer Dateien, Informationen über Hintergrundvorgänge sowie ein optimiertes Erlebnis beim Öffnen von Assets mit verlinkten Dateien (wie InDesign).

>[!NOTE]
>
>Wenn Sie macOS 10.15.4 oder höher verwenden, verwenden Sie mindestens Version 1.10.0.6 des Programms. Diese Patch-Version erfüllt die [Apple-Benachrichtigungsanforderungen](https://developer.apple.com/news/?id=04102019a).

**Lokales Bearbeiten/Auschecken**: Automatische Uploads gespeicherter Asset-Änderungen, die im Statusfenster deaktiviert werden können. So können Benutzer an Dateien arbeiten, die hierbei vorgenommenen Änderungen speichern und, wenn sie bereit sind, alle Änderungen hochladen.

**Fenster „Vereinfachter Asset-Status**. Das Statusfenster wurde vereinfacht. Auf der Registerkarte [!UICONTROL Uploads] werden jetzt sowohl einzelne Assets als auch Ordner- oder Massen-Uploads angezeigt. Die vorherige Registerkarte „Massen-Uploads“ wurde entfernt.

**Anwendungssymbol zum Anzeigen von Massen-Uploads**. Das Programmsymbol zeigt anhand der Überlagerung „Transfer“ (Übertragung) an, dass ein Massen-Upload durchgeführt wird, indem die Überlagerung angezeigt wird.

**Benachrichtigungen für Aktualisierungskonflikte**. Wenn vom Programm während einer Asset-Aktualisierung ein Konflikt erkannt wird, wird eine Benachrichtigung angezeigt, sodass der/die Benutzende sie überprüfen kann, ohne das Statusfenster zu überwachen. Beim Start sucht die Anwendung nach allen Konflikten und ermöglicht dem Benutzer, diese zu lösen.

**Besserer Umgang mit Verbindungsabbrüchen**. Massen-Uploads werden bei einem Verbindungsverlust angehalten und der Benutzer kann später fortgesetzt werden. Für fehlgeschlagene Uploads einzelner Dateien steht Benutzern die Schaltfläche [!UICONTROL Retry] zur Verfügung.

## Installationsanweisungen {#installation-instructions}

Detaillierte Anweisungen finden Sie unter [Installieren und Konfigurieren des AEM-Desktop-Programms](install-configure-app-v1.md).

## Verbesserungen in den vorherigen Versionen {#enhancements-in-the-previous-versions}

Diese Version erweitert und ersetzt die Vorgängerversionen des [!DNL Experience Manager]-Desktop-Programms, die die folgenden wesentlichen Verbesserungen boten:

* **Version 1.9 / 1.9.1**: Wiederverwendbare Uploads, verbessertes Statusfenster, Anwendungssymbole, die den Status der Anwendung/Verbindung anzeigen, Vorabrufen verknüpfter Assets zum InDesign von Dateien.

* **Version 1.8**: Bessere Kontrolle der Cachegröße für den Benutzer, verbessertes Anmeldeerlebnis für SAML/SSO unter Windows, Unterstützung `.pac` Netzwerk-Proxys auf Mac und kundengemeldete Probleme.

* **Version 1.7**: Verbesserungen der Stabilität und Caching-Logik, bessere Unterstützung für Netzwerk-Proxys und Möglichkeit, interne Dateien nach der Deinstallation zu bereinigen

* **Version 1.6**: Verbesserungen am Anmeldeprozess für verschiedene AEM-Sicherheitskonfigurationen sowie an der Stabilität und Leistung des Programms.

* **Version 1.5**: Programm-Stabilität und Ausfallsicherheit bei verschiedenen Netzwerkproblemen, bessere Unterstützungsmöglichkeiten.

* **Version 1.4**: Möglichkeit, hierarchische Ordner im Hintergrund mit der Fortschrittsüberwachung hochzuladen.

* **Version 1.3**: verbesserte Leistung und Stabilität beim Zugriff auf Dateien und Speichern von Änderungen in AEM, insbesondere aus Creative Cloud-Desktop-Progammen wie InDesign, Illustrator oder Photoshop. Diese Version sollte Benutzern ein Desktop-artiges Erlebnis bei der Arbeit mit Dateien bieten und gleichzeitig Übertragungsvorgänge für Netzwerkdaten im Hintergrund durchführen.

### Seit Einführung des AEM-Desktop-Programms 1.9 verfügbare Verbesserungen {#Enhancements-Available-Since-AEM-Desktop-App-19x}

[!DNL Adobe Experience Manager] Desktop-Programm Version 1.9.1 war eine Patch-Version. Sie wurde entwickelt, um wichtige Kundenprobleme beim Auschecken von Assets zu beheben. Adresse, die Dateien von einer Netzwerkfreigabe in ein lokales Verzeichnis kopiert.

* Assets, die von einem Benutzer ausgecheckt werden, sollten nicht für Bearbeitungen durch andere Benutzer verfügbar sein (CQ-4246009).

* Unterstützung für das Kopieren aus einem zugeordneten Ordner in einen lokalen Ordner, wenn sich der Benutzerordner auf einer separaten Festplattenpartition befindet (CQ-4243978)

Das AEM-Desktop-Programm 1.9 konzentrierte sich auf die Verbesserung des Benutzererlebnisses rund um den Upload großer Dateien, Informationen über Hintergrundvorgänge sowie ein optimiertes Erlebnis beim Öffnen von Assets mit verlinkten Dateien (wie InDesign).

**Fortsetzbare Uploads**
Für Uploads, insbesondere bei großen Dateien, gibt es eine Option, sie im neuen Fenster Asset-Status anzuhalten / fortzusetzen.

**Verbessertes Fenster für den Asset-Status**
Ein verbessertes Fenster Asset-Status enthält die folgenden Informationen zu Assets.

[!UICONTROL Changes]

* Zeigt Änderungen an, die sich momentan in der Warteschlange befinden.

* Zeigt laufende Uploads mit einer Fortschrittsleiste, Übertragungsrate, Gesamtdateigröße und den bisher übertragenen Betrag an.

* Abgeschlossene Uploads werden mit der übertragenen Datenmenge und der Übertragungsrate angezeigt.

* Fehlgeschlagene Uploads werden zusammen mit einer Fehlermeldung und Übertragungsinformationen angezeigt, sofern verfügbar.

* Bei dreimal fehlgeschlagenen Uploads wird eine Fehlermeldung angezeigt.

* Widersprüchliche Dateien werden mit einem Symbol angezeigt, auf das der Benutzer klicken kann. Durch das Klicken auf das Symbol wird ein Dialogfeld mit einer Erklärung und zwei Optionen angezeigt:

   * [!UICONTROL Keep Mine] lädt die Datei sofort auf den Server hoch

   * [!UICONTROL Overwrite Mine] löscht die lokale Datei sofort und lädt eine neue Kopie vom Server herunter

[!UICONTROL Downloads]

* Zeigt aktive Downloads an, einschließlich einer Übertragungsrate und der bislang übertragenen Größe.

* Abgeschlossene Downloads werden mit der insgesamt übertragenen Rate, der endgültigen Rate und einem Symbol angezeigt, das die Datei öffnet, wenn Sie darauf klicken (nur für einzelne Dateien verfügbar).

* Fehlgeschlagene Downloads werden mit einer Fehlermeldung und Übertragungsinformationen angezeigt, sofern verfügbar.

* Die Fußzeile zeigt die Gesamtzahl der heruntergeladenen Dateien und die durchschnittliche Übertragungsrate an.

* Wenn ein(e) Benutzende(r) mehrere Dateien über die [!DNL Experience Manager Assets]-Web-Benutzeroberfläche öffnet oder bearbeitet, werden sie gruppiert. Beispiel: meinasset.jpeg und 4 weitere Dateien.

* Beim Herunterladen von InDesign-Dokumenten mit verknüpften Assets aus AEM Assets lädt das Desktop-Programm zunächst alle verknüpften Assets herunter, bevor es das Dokument öffnet und den Download-Status angibt. Beispiel: 5 von 24.

[!UICONTROL Bulk Uploads]

Hochladen großer Ordnerhierarchien über [!UICONTROL Create] > [!UICONTROL Upload Folder] in den Triggern der AEM-Web-Benutzeroberfläche in diesem Dialogfeld. Dasselbe tritt auf, wenn Sie im Finder oder Explorer im Kontextmenü des Desktop-Programms &quot;Assets einfügen“ kopieren und auswählen.

* Zeigt aktive Uploads an, einschließlich eines Fortschrittsbalkens und des Namens der momentan übertragenen Datei.

* Laufende Uploads enthalten ein Symbol, durch das der Upload abgebrochen wird, wenn auf das Symbol geklickt wird. Die Übertragung wird angehalten, nachdem die aktuelle Übertragung der Datei abgeschlossen ist.

* Fehlgeschlagene Übertragungsprozesse werden mit einer Fehlermeldung angezeigt (nur, wenn die gesamte Übertragung fehlschlägt).

* Wenn eine einzelne Datei nicht übertragen werden kann, wird sie auf der Registerkarte als Fehler angezeigt. Andernfalls werden einzelne Dateien nicht auf der Registerkarte * angezeigt, sondern nur ein einzelner Eintrag für den gesamten Upload.

**Symbole zur Anzeige des Status von Hintergrundvorgängen**

Das Anwendungssymbol gibt den Status von Hintergrundvorgängen an, um den Benutzern einen besseren visuellen Hinweis zu geben. Wenn die Anwendung beispielsweise nicht mit AEM verbunden ist, wird das Symbol ausgegraut. Wenn es einen aktiven Upload gibt, wird eine „Sync“-Überlagerung angezeigt usw.

**Vorab-Abruf verknüpfter Assets**

Um das Benutzererlebnis mit dem InDesign von Dokumenten mit verknüpften Assets in AEM zu verbessern, ruft das Desktop-Programm diese verknüpften Dateien vorab in den lokalen Cache ab. Dieser Fluss erfolgt vor dem Herunterladen und Öffnen des InDesign-Dokuments. Auf diese Weise sind die verknüpften Dateien lokal verfügbar und müssen beim Zugriff auf Assets auf InDesign (im Bedienfeld „Links„) nicht länger warten.
Der Vorabruf funktioniert nur, wenn AEM die Links auf der Serverseite erkennt. Ein Asset mit erkannten Links verfügt über eine Liste von „Verweisen“, die in der Eigenschaftenansicht des InDesign-Assets aufgeführt ist.

### Seit Einführung des AEM-Desktop-Programms 1.8 verfügbare Verbesserungen {#enhancements-available-since-aem-desktop-app-18x}

In der Folgeversion 1.8.1 des AEM-Desktop-Programms wurden Verbesserungen hinsichtlich des gleichzeitigen Öffnens mehrerer Dateien über die AEM-Benutzeroberfläche gegenüber der Version 1.8 hinzugefügt (CQ-4237747, CQ-4238780). Verbesserungen im AEM-Desktop-Programm 1.8:

* Caching: Neue Benutzeroberfläche zum Verwalten des Caches des AEM-Desktop-Programms (CQ-4208690), einschließlich folgender Funktionen:

   * Aktuelle Cachegröße anzeigen

   * Maximale Cache-Größe definieren, bevor eine Benachrichtigung gesendet wird

   * Die Cache-Größe wird nur beim Start des Desktop-Programms überprüft. Beim Erreichen der konfigurierten Beschränkung wird eine Meldung angezeigt.

   * Die neue Benutzeroberfläche bietet eine Schaltfläche zum Löschen des Caches.

* Anmeldung: (Win) Feste Anmeldung bei AEM-Instanz, die für die Verwendung von SAML und SSL konfiguriert ist (CQ-4216353)

* Netzwerk:

   * Wenn eine AEM-Sitzung abläuft, wird der Benutzer jetzt benachrichtigt und kann auf die Benachrichtigung klicken, um sich erneut anzumelden (CQ-4202028).

   * (Mac) Fügen Sie Unterstützung für das Verbinden mit AEM über die Verwendung der `.pac` Proxy-Konfiguration hinzu (CQ-4233430).

   * (Windows) Behebung von Problemen mit dem Dialogfeld „Advanced“ > „Login URL“ (Erweitert > Anmelde-URL) (CQ-4236061).

* Fehlerbehebungen:

   * Dialogfeld „Weitere Asset-Informationen“: Manchmal war die Aktionsleiste nicht sichtbar (CQ-4208540).

   * (Windows) Dateien können nun synchronisiert werden, nachdem sie in der AEM Assets-Benutzeroberfläche auf eine ältere Version zurückgesetzt wurden (CQ-4216411).

### Seit Einführung des AEM-Desktop-Programms 1.7 verfügbare Verbesserungen {#Enhancements-Available-Since-AEM-Desktop-App-17}

* Stabilität:

   * Die Stabilität wurde verbessert, wenn die AEM-Desktop-App eine Verbindung zu einem überlasteten AEM-Server herstellt (CQ-4224803).

   * Verbesserte Stabilität, wenn viele Dateien angefordert werden (CQ-4224212).

   * Verbesserte Asset-Aktualisierung mit zusätzlicher Prüfung (CQ-4228291).

* Caching:

   * Behobene Festplattenfehler und Probleme beim Öffnen von Dateien in Photoshop, InDesign, Finder (CQ-4223993, CQ-4217603, CQ-4223717).

   * Verbesserte Zwischenspeicherung zur Vermeidung von Binärdateien mit Größe null (CQ-4216599).

* Anmeldung: Ermöglicht die Verbindung mit striktem SSL, das für spezielle Konfigurationen deaktiviert ist (wie lokal ausgestellte Zertifikate) (CQ-4223949).

* Netzwerke: Verbesserte Unterstützung für die Verbindung über Netzwerk-Proxy (CQ-4223477, CQ-4221280, CQ-4206854).

* Installation und Deinstallation:

   * (Win) Cleaner-Deinstallation (CQ-4220906).

   * [Windows (32 Bit)] Installationsprogramm schlägt beim Versuch zur Installation von Microsoft.NET Framework Version 4.5 zu fehl (CQ-4218084).

   * (Mac) Skript zur manuellen Ausführung für das vollständige Entfernen von Desktop-Programm-Dateien (CQ-4216489).

>[!NOTE]
>
>Probleme, die beim Laden der Betaversion des AEM-Desktop-Programms 1.7 auftreten und in Version 1.6 nicht vorhanden waren, werden in den Versionshinweisen weggelassen.

### Seit Einführung des AEM-Desktop-Programms 1.6 verfügbare Verbesserungen {#Enhancements-Available-Since-AEM-Desktop-App-16}

* Dokumentation: Neue Dokumentation [Best Practices für das Programm, v1.x](/help/using/best-practices-for-v1.md).

* Verbesserter Anmeldeprozess für AEM:

   * Verbessertes SAML-Handling – Relax-Regeln (CQ-4202781).

   * Fügen Sie die Funktion hinzu, um eine separate Anmelde-URL in den Voreinstellungen zu konfigurieren (CQ-4214052, CQ-4214051).

* Benutzerfreundlichkeit: Benachrichtigen Sie Benutzende, wenn ein Asset für größere Assets noch heruntergeladen wird (CQ-4216284).

* Netzwerke:

   * DNS-Caching (CQ-4210176).

   * Unterstützung für Verbindung über Proxy unter Windows (CQ-4206854).

* Zwischenspeicherung und Zugriff auf Netzwerkfreigabe in Finder/Explorer:

   * Das Sperrsymbol ist jetzt für ausgecheckte Assets unter Windows 10 sichtbar (CQ-90957).

   * Ordnerinhalte können in der Netzwerkfreigabe verschwinden/erneut angezeigt werden (CQ-4209160, CQ-4210180).

   * Fehler beim Datei-Upload aufgrund eines Konflikts, der im Bericht zum Upload-Warteschlangen-Status gemeldet ist (CQ-4215727).

   * Beim Öffnen mehrerer Dateien über den Ordner für das Desktop-Programm in PS werden möglicherweise Fehlermeldungen zu abgeschnittenen oder unvollständigen Dateien angezeigt (CQ-4216276).

* Verbesserungen an Stabilität und Performance:

   * Verbesserte Leistung beim Durchsuchen von Ordnern mit vielen Assets (CQ-4214933).

   * Das Desktop-Programm 1.5 kann einen Desktop-Computer im Laufe der Zeit verlangsamen (CQ-4209159).

   * Die Funktion zum Anzeigen des Warteschlangenstatus funktioniert nur für den Benutzer, der das Programm installiert hat (CQ-4212199).

   * (Windows) Stellen Sie sicher, dass das 32-Bit-Installationsprogramm keinen 64-Bit-Code enthält (CQ-4217406).

* Ausgewählte Probleme, die in Beta 1.6 gefunden und behoben wurden:

   * Hohe CPU-Auslastung (CQ-4218070).

   * Ziehen von Dateien per Drag-and-Drop führt zu Fehler beim Hochladen in AEM (CQ-4217006).

### Seit Einführung des AEM-Desktop-Programms 1.5 verfügbare Verbesserungen {#Enhancements-Available-Since-AEM-Desktop-App-15}

**Version 1.5.1.5 für macOS X:** Die 1.5.1.5-Version bietet die folgenden Vorteile:

* Neue Funktionen und Verbesserungen: Hinzufügen der Funktion zum Kopieren/Einfügen zur Finder-Integration, um die direkte Übertragung vom Desktop zur AEM zu ermöglichen (CQ-4208158).

* Fehlerbehebungen:

   * Problem aufgrund von Fehler 43 behoben, das in einigen Fällen beim Umbenennen von Assets aufgetreten ist (CQ-4207900).

   * Beim Zurücksetzen auf eine ältere Version aus der Timeline aktualisiert AEM das Asset nicht in Finder (CQ-4205194).

   * Das Desktop-Programm stürzt beim Durchsuchen großer verschachtelter Verzeichnisse ab (CQ-4208539).

   * Der Bereitstellungspunkt für das -Desktop-Programm ist jetzt /Volumes/DAM, sodass er für alle Benutzer konsistent ist (CQ-4208159).

   * Durch das erstmalige Einfügen einer Datei in InDesign wird eine Aktualisierungswarnung ausgelöst (CQ-4207454).

Hinweis zu Link-Warnungen: Creative Cloud-Programme (z. B. InDesign) erstellen einen „Schnappschuss“ der letzten Änderung des Elements zum Zeitpunkt seiner Platzierung. Wenn sich dieses Datum zu einem späteren Zeitpunkt ändert, meldet die Adobe Creative Cloud-App, dass die Links veraltet sind. Diese Informationen werden auf verschiedene Weise berichtet:

* Beim Start der Adobe Creative Cloud-App wird ein Dialogfeld angezeigt, in dem der Benutzer darüber informiert wird, dass die verknüpften Assets veraltet sind, und der Benutzer aufgefordert wird, Maßnahmen zu ergreifen.

* Wenn die Adobe Creative Cloud-App bereits ausgeführt wird, wird für das verknüpfte Asset ein gelbes Warndreieck angezeigt.

Dieses Verhalten ist für Assets auf der lokalen Festplatte und Assets in einem auf dem AEM-Desktop gemounteten Verzeichnis identisch, mit den folgenden Ausnahmen:

* Wenn ein(e) andere(r) Benutzende(r) ein platziertes Asset bearbeitet, wird beim ersten Öffnen eines Dokuments mit dem platzierten Asset durch andere Benutzende das Warnsymbol angezeigt. Diese Warnung tritt nur auf, wenn das platzierte Asset bereits lokal zwischengespeichert wurde.

* Wenn ein(e) Benutzende(r) ein platziertes Asset über das gemountete Verzeichnis des AEM-Desktops ändert und dann seinen/ihren lokalen Cache löscht, wird das platzierte Asset als veraltet gemeldet.

Beide Fälle werden erwartet und sind Nebeneffekte der „verzögerten Synchronisierung“ der AEM-Desktops.

**Version 1.5.0.x für macOS X und Windows:** Diese Version des AEM-Desktop-Programms bietet die folgenden Vorteile:

* Bessere Stabilität und Ausfallsicherheit bei verschiedenen Netzwerkproblemen.

   * Zuverlässigere Zuordnung von AEM Assets-Ordnern (CQ-103276, CQ-4204669, CQ-4203957).

   * Verbesserte Handhabung zwischengespeicherter Dateien (CQ-4204336, CQ-4206263).

   * Verbesserte Handhabung von Downloads/Uploads großer Dateien mit einer Größe von mehr als 2 GB (CQ-4206438).

   * Behebung von Fehler 36 beim Verschieben oder Umbenennen einer großen Anzahl von Dateien in Finder (CQ-4204640).

* Optimierungen bei der Netzwerkkommunikation mit dem AEM-Server (CQ-4204974, CQ-100903).

* Verbesserte Zuverlässigkeit beim Öffnen, Platzieren und Speichern von Assets aus AEM in Creative Cloud-Programmen (CQ-4203968, CQ-4205511, CQ-103543, CQ-4207141, CQ-90980).

* Verbesserte Unterstützungsmöglichkeit: Option zum Leeren des Cache (CQ-4202541), einfacher Zugriff auf Protokolle (CQ-4202340, CQ-4204673).

* Weitere Fehlerbehebungen:
   * Bessere Unterstützung für Assets und Ordner mit japanischen Zeichen in name/nicht-englischen Spracheinstellungen (CQ-4195433, CQ-4205793, CQ-4199446).

   * Bessere Handhabung der Anmeldung mit SSL (CQ-4200217).

   * Zuverlässigere Freigabebereitstellung (CQ-4200793).

   * Diverse Verbesserungen hinsichtlich der Stabilität (CQ-4207539, CQ-4200378).

   * Verbesserte Handhabung der AEM Assets-URL in den Voreinstellungen (CQ-97388).

### Seit Einführung des AEM-Desktop-Programms 1.4 verfügbare Verbesserungen {#Enhancements-Available-Since-AEM-Desktop-App-14}

* Vereinfachter Upload hierarchischer Ordner über die neue Aktion „Erstellen“ > „Ordner hochladen“ in der Touch-optimierten Benutzeroberfläche.
   * Diese Aktion initiiert einen Vorgang zum Hochladen von Ordnern, der von der Desktop-Anwendung ausgeführt wird.
   * Das Desktop-Programm durchläuft die angegebene Ordnerhierarchie auf dem Desktop im Hintergrund und lädt die Dateien in AEM Assets hoch.
   * Der Benutzer kann den Fortschritt laufender Vorgänge im neuen Fenster Upload-Warteschlangenstatus überwachen.
   * Der Status der Upload-Warteschlange bietet außerdem bessere Informationen zur Fehlerbehebung (z. B. keine Verbindung zum Server).
* Neue Aktion „Bearbeiten“ in der Touch-optimierten Benutzeroberfläche, die Checkout- und Öffnen-Vorgänge in einer kombiniert.
* Optimierte Gruppierung von Desktop-bezogenen Aktionen in der Touch-Benutzeroberfläche (AEM 6.3).
* Die Kompatibilität mit den neuesten Betriebssystemversionen wurde verbessert.
* Vom Kunden gemeldete Fehlerbehebungen.

### Seit Einführung des AEM-Desktop-Programms 1.3 verfügbare Verbesserungen {#Enhancements-Available-Since-AEM-Desktop-App-13}

* Höhere Effizienz. Netzwerkvorgänge werden schneller abgeschlossen und die Wartezeiten für Benutzer werden verkürzt.
* Verbesserte Finder-Integration, die für mehr Stabilität sorgt und den Zugriff auf Funktionen wie Miniaturansichten ermöglicht.
* Verbesserungen hinsichtlich der Zwischenspeicherung und Leistung.
* Bessere Unterstützung für das direkte Speichern aus Desktop-Programmen (PS, ID, AI usw.).
* Verbesserte Integration mit macOS (Protokoll für lokales Netzlaufwerk von WebDAV in stabileres SMB1 geändert).
* Die Desktop-App stellt eine Verbindung zum AEM-Server her, indem sie das AEM-native HTTP-RESTful-Protokoll verwendet.
* Die Dateien werden zunächst lokal gespeichert und nach einer festgelegten Zeit (30 Sek.) im Hintergrund wieder in AEM hochgeladen. Dieser Workflow verkürzt die Zeit zum Speichern von Dateien.
* Besseres Handling von Desktop-Programmen, die Zwischenvorgänge zum Speichern von Dateien verwenden (partielles Speichern und temporäre Dateien). Dadurch können in der AEM Assets-Timeline korrekte Versions- und Asset-Upload-Informationen angezeigt werden.
* Es wird ein Dialogfeld zum Nachverfolgen des Status von Upload-Hintergrundaufgaben bereitgestellt.

## Liste der Änderungen {#list-of-changes}

### Bereitstellungspunkt für Mac {#mount-point-on-mac}

Seit macOS 10.12 (Sierra) hat Apple die Berechtigungen für den Ordner &quot;/Volumes“, die zum Bereitstellen von Netzlaufwerken und Geräten verwendet werden, restriktiver geändert. Für das Erstellen eines neuen Bereitstellungspunkts an diesem Speicherort waren Administratorrechte erforderlich. Dieses Problem wurde in macOS 10.12.5 behoben.

Der Bereitstellungspunkt des AEM-Desktop-Programms hat sich in den Versionen 1.4 und 1.5 geändert. Auf macOS wurde er zu einem DAM-Unterordner im lokalen Ordner des Benutzers geändert, wodurch Benutzende ohne Administratorrechte unterstützt werden (CQ-104183).

Da für den `/Volumes` keine Administratorrechte mehr erforderlich sind, wurde diese Änderung in Version 1.5.1 rückgängig gemacht. Diese Änderung ermöglicht es auch, InDesign-Dokumente, die Assets aus AEM platziert haben, zwischen macOS-Benutzern freizugeben.

### Protokolländerung (seit Version 1.3) {#protocol-change-since}

* macOS X:
   * Das Protokoll für lokale Netzwerklaufwerke für die OS X-Desktop-Integration wurde von WebDAV in SMB1 geändert.
   * Das mit der Desktop-Anwendung bereitgestellte AEM-Repository wird im Finder als `smb` Netzlaufwerk und nicht als WebDAV-Laufwerk angezeigt.
* Windows:
   * Das lokale Netzlaufwerksprotokoll für Windows-Desktop-Integrationen bleibt bestehen; AEM wird als WebDAV-Freigabe gemountet.
* Für beide Plattformen (Windows und Mac):
   * Das Protokoll zum Zugreifen auf/Herunterladen von Assets und zum Hochladen von Änderungen in AEM wurde in das native AEM-Protokoll geändert, ein HTTP-basiertes RESTful-Protokoll. Es bietet eine bessere Kontrolle über Netzwerkvorgänge und eine bessere Kompatibilität mit der Netzwerkinfrastruktur.

>[!NOTE]
>
>Auf macOS X führt die Änderung des Protokolls für das lokale Netzlaufwerk von WebDAV zu SMB1 zu einem anderen lokalen Pfad zum gleichen Asset im Repository. Diese Änderung kann sich auf Links zu Dateien auswirken, die in Adobe Creative Cloud-Anwendungen über den Befehl „Place“ platziert werden. Weitere Informationen finden [ unter „Verwenden ](use-app-v1.md) AEM-Desktop-Programms“.

### Dateiverarbeitung (seit 1.3) {#file-handling-since}

* Ordner werden nach einer festgelegten Verzögerung (derzeit 30 Sek.) automatisch aktualisiert.
* Dateien, die von anderen Benutzern ausgecheckt wurden, sind als schreibgeschützt markiert.
* Dateien werden in zwei Phasen auf einem Netzlaufwerk gespeichert, das über die Desktop-App bereitgestellt wird.
* In der ersten Phase wird eine Datei lokal gespeichert. Auf diese Weise muss der Benutzer, der die Datei speichert, nicht warten, bis die Datei vollständig in AEM übertragen wurde, und kann seine Arbeit fortsetzen, sobald die Datei gespeichert wurde.
* In der zweiten Phase lädt das Desktop-Programm nach einer vordefinierten Verzögerung (z. B. dreißig Sekunden) eine aktualisierte Datei auf den AEM-Server hoch. Dieser Vorgang erfolgt im Hintergrund. Verwenden Sie die Option **Status der Dateisynchronisierung im Hintergrund anzeigen**, um den Status des Upload-Vorgangs anzuzeigen.

## Wichtige Hinweise {#important-notices}

**Ordner-Upload:** Adobe empfiehlt die Verwendung der neuen Ordner-Upload-Funktion, um größere, hierarchische Ordner in AEM hochzuladen. Dieser Ansatz wird empfohlen, anstatt eine Kopie / Drag-and-Drop in ein bereitgestelltes AEM-Repository aus der Finder / Explorer-Ebene zu verwenden. Bei Verwendung der Funktion zum Hochladen von Ordnern kommuniziert das Desktop-Programm direkt mit AEM und hat somit eine viel bessere Kontrolle über den gesamten Prozess.

**AEM-Sitzung aktivieren:** Das AEM-Desktop-Programm hängt von einer Sitzung ab, die auf dem AEM Assets-Server geöffnet ist, um einen ordnungsgemäßen Betrieb sicherzustellen. Tägliche Benutzer sollten die Bereitstellung von AEM Assets am Ende des Tages beenden, um sich abzumelden, und morgens erneut mounten, um die Anmeldung und Netzwerkfreigabefunktion sicherzustellen.

**Deaktivieren Sie „Symbolvorschau“ im Finder.** Stellen Sie sicher, dass „Symbol“ und „Symbolvorschau“ deaktiviert sind, um große Ordner mit dem Finder nach Leistung zu durchsuchen, insbesondere bei schlechter Netzwerkverbindung. Andernfalls lädt Finder jedes Asset in einem Ordner herunter, um eine kleine Vorschau zu generieren, was zu schlechter Leistung und hoher Bandbreitenauslastung führen kann (CQ-4219779)

* Navigieren Sie im Finder zum freigegebenen AEM Assets-Netzwerkordner.
* Klicken Sie mit der rechten Maustaste auf den DAM-Bereitstellungspunkt.
* Wählen Sie die Option zum Anzeigen der Ansichtsoptionen aus.
* Deaktivieren Sie das Kontrollkästchen „Symbolvorschau anzeigen“.
* Klicken Sie auf „Als Standard verwenden“.

**Bereinigen Sie den Cache beim Herstellen einer Verbindung mit einem neuen AEM-Server.** Wenn die Desktop-Anwendung eine Verbindung zu einem anderen AEM-Server mit derselben URL herstellt, wird der Cache nicht automatisch gelöscht. Löschen Sie den Cache manuell, um einen ordnungsgemäßen Betrieb sicherzustellen. Beachten Sie, dass dieser Prozess normalerweise beim Testen auftritt, wenn AEM-Installationen bei der Ausführung über dieselbe URL ersetzt werden können (CQ-4216982)

**CA-signierte SSL-Zertifikate verwenden:** Die AEM-Desktop-App unterstützt keine selbstsignierten SSL-Zertifikate, wenn über eine sichere HTTPS-Verbindung eine Verbindung zu AEM hergestellt wird. Für derartige Verbindungen ist ein CA-signiertes Zertifikat auf dem Server erforderlich (CQ-87941).

## Bekannte Probleme {#known-issues}

* Allgemein:
   * Es werden Server-URLs benötigt, um ohne Pfad auf den Server zu verweisen (z. B. `http://server`, `https://server`, `http://server:port` oder `https://server:port`). Außer „/content/dam“ werden keine anderen Kontextpfade und Unterordner unterstützt (CQ-89343, CQ-87272).
* Dateinamen/Lokalisierung:
   * Datei- und Ordnernamen mit reservierten Zeichen werden nicht ordnungsgemäß verarbeitet. Stellen Sie sicher, dass Sie Datei- und Ordnernamen verwenden, die den AEM-Anforderungen entsprechen. (CQ-93361, CQ-93308, CQ-89276, CQ-4217183)
   * Einige Programme wie Adobe Illustrator erstellen möglicherweise Dateien mit Namen, die in AEM nicht unterstützt werden. Beispiel: Hinzufügen von `Converted` nach der Konvertierung einer Datei, wodurch das Hochladen verhindert wird. (CQ-4216985)
   * Assets mit internationalen Namen kann alle paar Sekunden erscheinen und verschwinden.
* Ein- und Auschecken:
   * Ein von einem Benutzer ausgechecktes Asset kann nicht von einem anderen Benutzer geöffnet werden, weder über die Aktion „Öffnen“ in der Touch-optimierten Benutzeroberfläche noch direkt auf dem Desktop. Einige Programme melden möglicherweise, dass das Asset gesperrt oder beschädigt ist bzw. nicht reagiert, wenn versucht wird, das Asset zu öffnen (CQ-4199234).
   * Das gleichzeitige Ändern von Dateien durch mehrere Benutzer kann dazu führen, dass einige Änderungen verloren gehen. Die Problemumgehung besteht darin, die Ein- und Auscheckfunktionen zu verwenden, um zu verhindern, dass mehrere Benutzer dieselbe Datei ändern. (CQ-97035)
   * Bestimmte Anwendungen unterstützen das Flag „Schreibgeschützt“ nicht ordnungsgemäß, sodass ein Benutzer eine Datei speichern kann, die von einem anderen Benutzer ausgecheckt wurde. Die geänderte Datei wird erst dann übertragen, wenn der andere Benutzer die Datei wieder eincheckt. Beide Änderungen sind in AEM als verschiedene Versionen des Assets verfügbar. (CQ-89551, CQ-87572, CQ-89615)
   * Der ausgecheckte und der schreibgeschützte Status werden unabhängig im Finder gemeldet. Dieser Ansatz führt zu zwei Sperrsymbolen, wenn ein Benutzer ein Asset auscheckt. (CQ-89507)
* Finder-Integration:
   * Beim Ziehen und Ablegen großer Dateien kann es vorkommen, dass der Finder eine Zeitüberschreitung aufweist, während die Dateien im Hintergrund übertragen werden. Diese Verzögerung führt zu einer `Error - 36`. Die Lösung besteht darin, das Asset per Drag-and-Drop zu verschieben oder erneut zu öffnen. (CQ-4219628)
   * Das manuelle erneute Laden von Ordnern funktioniert nicht immer. Problemumgehung: Warten Sie dreißig Sekunden, bis der Ordner automatisch aktualisiert wird. (CQ-97389).
   * „Weitere Asset-Informationen…“ ist auf die Auswahl einer einzelnen Datei beschränkt. (CQ-89542, CQ-87656)
   * In AEM Assets öffnen… ist auf die Auswahl einer einzelnen Datei und eines einzelnen Ordners beschränkt. (CQ-83382)
   * Fehler beim Umbenennen von Assets ohne Erweiterung. (CQ-4218971)
* Kopieren/Einfügen-Funktion: Einfügen ist verfügbar, wenn kein Asset in die Zwischenablage kopiert wurde.
* Windows:
   * Dateien mit alternativen Datenströmen (ADS) werden nur in NTFS-Dateisystemen vollständig unterstützt. Beim Kopieren von Dateien in die WebDAV-Freigabe über die Desktop-App wird in einem Warndialogfeld gewarnt, dass einige Dateieigenschaften nicht an den neuen Speicherort übertragen werden können. Diese Warnung ist in der Regel korrekt, da die Eigenschaften nur für ein bestimmtes Programm auf dem Desktop des Benutzers relevant sind und nichts mit dem tatsächlichen Dateiinhalt zu tun haben. (CQ-103770) (Win)
   * Der Benutzer, der das Desktop-Programm unter Windows verwendet, muss derjenige sein, der es installiert. (CQ-4216389) (Win)
   * Die App kann abstürzen, wenn die Option [!UICONTROL Retry] bei einem fehlgeschlagenen Upload ausgewählt wird. Dieser Absturz kann unter bestimmten Umständen auftreten, nachdem der Batch-Upload fortgesetzt wurde, wenn die Verbindung getrennt wurde. (CQ-4251884) (Win)

## Hilfreiche Ressourcen {#helpful-resources}

* [Dokumentation zu AEM](https://experienceleague.adobe.com/de/docs)
* [Verwenden des AEM-Desktop-Programms, v1.x](use-app-v1.md)
* [Best Practices für das AEM-Desktop-Programm, v1.x](best-practices-for-v1.md)

## Kompatibilitätsmatrix und Voraussetzungen {#compatibilitymatrix}

Das AEM-Desktop-Programm ist mit verschiedenen AEM-Versionen kompatibel. Informationen zu den unterstützten Versionen finden Sie in der Kompatibilitätsmatrix.

| Version | Revision | Veröffentlichungsdatum | Kompatibilität |
|--- |--- |--- |--- |
| 1.10 | 1.10.0.3 (Mac und Win) | 31. August 2018 | AEM 6.5; AEM 6.4 SP1; AEM 6.3 SP2; AEM 6.2 SP1 CFP2+; AEM 6.1 SP2 CFP7+ |
| 1.9 | 1.9.1.1 (Mac und Win) | 21. Juni 2018 | AEM 6.4; AEM 6.3 SP1; AEM 6.2 SP1 CFP2+; AEM 6.1 SP2 CFP7+ |
| 1.8 | 1.8.1.0 (Mac und Win) | Donnerstag, 28. März 2018 | AEM 6.4; AEM 6.3 SP1; AEM 6.2 SP1 CFP2+; AEM 6.1 SP2 CFP7+ |
| 1.7 | 1.7.0.3 (Mac und Win) | Donnerstag, 10. Januar 2018 | AEM 6.3 SP1; AEM 6.2 SP1 CFP2+; AEM 6.1 SP2 CFP7+ |
