---
title: Fehlerbehebung für das Desktop-Programm, Version 1.10.
description: Führen Sie eine Fehlerbehebung für das [!DNL Adobe Experience Manager] -Desktop-Programm, Version 1.10. durch, um Probleme zu lösen, die eventuell bei der Installation, bei Upgrades, bei der Konfiguration usw. auftreten können.
exl-id: 1e1409c2-bf5e-4e2d-a5aa-3dd74166862c
source-git-commit: 5676e7ece8bb43f051dae72d17e15ab1c34caefc
workflow-type: tm+mt
source-wordcount: '3331'
ht-degree: 68%

---

# Fehlerbehebung für das [!DNL Adobe Experience Manager]-Desktop-Programm, v1.x {#troubleshoot-aem-desktop-app}

Führen Sie eine Fehlerbehebung für das AEM-Desktop-Programm durch, um gelegentliche Probleme im Zusammenhang mit Installation, Aktualisierung, Konfiguration usw. zu beheben.

Die [!DNL Adobe Experience Manager] Das -Desktop-Programm enthält Dienstprogramme, die Sie beim Zuordnen des AEM Assets-Repositorys als Netzwerkfreigabe auf dem Desktop unterstützen (SMB-Freigabe auf macOS). Bei der Netzwerkfreigabe handelt es sich um eine Betriebssystemtechnologie, mit deren Hilfe Remote-Quellen so behandelt werden können, als würden sie zum lokalen Dateisystem eines Computers gehören. Beim Desktop-Programm ist die Remote-Dateiquelle die DAM-Repository-Struktur (Digital Asset Management) einer Remote-AEM-Instanz. In der folgenden Abbildung wird die Topologie des Desktop-Programms beschrieben:

![Abbildung des Desktop-Programms](assets/aem-desktopapp-architecture.png)

Mit dieser Architektur fängt das Desktop-Programm Dateisystemaufrufe (Öffnen, Schließen, Lesen, Schreiben usw.) an die bereitgestellte Netzwerkfreigabe ab und übersetzt sie in native AEM HTTP-Aufrufe an den AEM-Server. Dateien werden lokal zwischengespeichert. Weitere Informationen finden Sie unter [Verwenden des AEM Desktop-Programms, Version 1.x](use-app-v1.md).

## Übersicht über die Komponenten des AEM-Desktop-Programms {#desktop-app-component-overview}

Das -Desktop-Programm umfasst die folgenden Komponenten:

* **Die Desktop-Applikation**: Die Anwendung stellt DAM als Remote-Dateisystem bereit oder hebt die Bereitstellung auf. Es übersetzt Dateisystemaufrufe zwischen der lokal bereitgestellten Netzwerkfreigabe und der Remote-AEM, mit der die Verbindung hergestellt wird.
* **WebDAV/SMB-Client des Betriebssystems**: Verarbeitet die Kommunikation zwischen Windows Explorer/Finder und dem Desktop-Programm. Wenn eine Datei abgerufen, erstellt, geändert, gelöscht, verschoben oder kopiert wird, kommuniziert der WebDAV/SMB-Client des Betriebssystems diesen Vorgang an das Desktop-Programm. Nach Erhalt der Kommunikation übersetzt das Desktop-Programm sie in native AEM Remote-API-Aufrufe. Wenn ein Benutzer beispielsweise in dem bereitgestellten Verzeichnis eine Datei erstellt, initiiert der WebDAV/SMB-Client eine Anfrage. Diese Anfrage wird vom Desktop-Programm in eine HTTP-Anfrage zur Erstellung der Datei in DAM übersetzt. Beim WebDAV/SMB-Client handelt es sich um eine integrierte Komponente des Betriebssystems. Er steht in keiner Weise mit dem Desktop-Programm, mit AEM oder Adobe in Verbindung.
* **Adobe Experience Manager-Instanz**: Bietet Zugriff auf die Assets, die im DAM-Repository von AEM Assets gespeichert sind. Darüber hinaus führt es die vom Desktop-Programm angeforderten Aktionen im Namen der lokalen Desktop-Programme aus, die mit der bereitgestellten Netzwerkfreigabe interagieren. Auf der AEM-Zielinstanz sollte AEM-Version 6.1 oder höher ausgeführt werden. Für AEM-Instanzen mit vorherigen AEM-Versionen müssen möglicherweise zusätzliche Feature Packs und Hotfixes installiert werden, um die vollständige Funktionalität zu erreichen.

## Vorgesehene Anwendungsfälle für das AEM-Desktop-Programm {#intended-use-cases-for-aem-desktop-app}

Das AEM-Desktop-Programm verwendet die Netzwerkfreigabetechnologie, um ein Remote-AEM-Repository einem lokalen Desktop zuzuordnen. Sie ist jedoch nicht als Ersatz für eine Netzwerkfreigabe mit Assets vorgesehen, bei der die Benutzer direkt auf ihrem lokalen Desktop Digital Asset Management-Vorgänge ausführen. Dazu zählen das Verschieben oder Kopieren mehrerer Dateien oder das Ziehen umfangreicher Ordnerstrukturen zu der AEM Assets-Netzwerkfreigabe direkt im Finder/Explorer.

Das AEM-Desktop-Programm bietet eine praktische Möglichkeit, auf DAM-Assets zwischen der Touch-Benutzeroberfläche von AEM Assets und dem lokalen Desktop zuzugreifen (sie zu öffnen) und sie zu bearbeiten (zu speichern). Sie verknüpft Assets auf dem AEM Assets-Server mit Ihren Desktop-basierten Workflows.

Der folgende Beispielanwendungsfall veranschaulicht, wie AEM Desktop verwendet werden sollte:

* Ein Benutzer meldet sich bei AEM an und verwendet die Web-Benutzeroberfläche, um ein Asset zu suchen.
* Er nutzt bei Bedarf die Funktionen für Desktop-Aktionen der AEM-Web-Benutzeroberfläche zum Öffnen, Anzeigen oder Bearbeiten des Assets auf dem Desktop.
* AEM Desktop öffnet das Asset im Standard-Editor für den Dateityp des Assets.
* Der Benutzer nimmt die gewünschten Änderungen am Asset vor.
* Nachdem eine Datei geändert wurde, kann der Benutzer den Synchronisierungsstatus der Datei im Statusfenster für die Hintergrundsynchronisierung von AEM Desktop anzeigen.
* Mithilfe des Kontextmenüs von AEM Desktop checkt der Benutzer das Asset ein/aus oder gibt es an die DAM-Benutzeroberfläche zurück.
* Nach Abschluss der Änderungen an der Datei kehrt der Benutzer zur AEM-Web-Benutzeroberfläche zurück.

Dieses Szenario ist nicht der einzige Anwendungsfall. Er veranschaulicht jedoch die bequeme Methode zum lokalen Zugreifen auf/Bearbeiten von Assets über AEM Desktop. Sie sollten die DAM-Web-Benutzeroberfläche so oft wie möglich verwenden, da sie ein besseres Erlebnis bietet. Sie ermöglicht Adobe mehr Flexibilität beim Erfüllen der Kundenanforderungen.

## Beschränkungen {#limitations}

Die WebDAV/SMB1-Netzwerkfreigabe bietet den Komfort, in einem Explorer/Finder-Fenster mit Dateien arbeiten zu können. Explorer/Finder und AEM kommunizieren jedoch über eine Netzwerkverbindung, die gewissen Einschränkungen unterliegt. Die zum Kopieren einer 1 GB großen Datei in das bereitgestellte WebDAV/SMB-Verzeichnis benötigte Zeit ist beispielsweise identisch mit dem Zeitaufwand zum Hochladen einer 1 GB großen Datei auf eine Website mit einem Webbrowser. Tatsächlich kann die Dauer im ersten Fall aufgrund der Ineffizienzen des WebDAV/SMB-Protokolls und der WebDAV/SMB-Clients des Betriebssystems (insbesondere macOS X) länger sein.

Die mit einem bereitgestellten Verzeichnis ausführbaren Aufgaben sind beschränkt. Grundsätzlich gestaltet sich die Arbeit mit größeren Dateien in Netzwerken mit unzureichender Verbindungsqualität, hoher Latenz oder geringer Bandbreite schwierig, was insbesondere für die Dateibearbeitung gilt.

Adobe empfiehlt, einige Anwendungsfälle zu testen, bevor Sie einem Kunden bestätigen, dass bestimmte Dateitypen über das bereitgestellte Verzeichnis effizient bearbeitet werden können.

Das AEM-Desktop-Programm ist für intensive Manipulationen des Dateisystems nicht geeignet. Dazu zählen unter anderem die folgenden Vorgänge:

* Verschieben oder Kopieren von Dateien und Verzeichnissen
* Hinzufügen vieler Assets zu AEM
* Suchen nach und Öffnen von Dateien über das Dateisystem, außer Durchsuchen von Ordnern
* Komprimieren oder Dekomprimieren von Dateiarchiven

Aufgrund der Beschränkungen des Betriebssystems gilt für Windows eine Dateigrößenbeschränkung von 4.294.967.295 Byte (ca. 4,29 GB). Der Grund dafür ist eine Registrierungseinstellung, die definiert, wie groß eine Datei auf einer Netzwerkfreigabe sein darf. Der Wert der Registrierungseinstellung ist ein DWORD-Ausdruck mit einer maximalen Größe, die der referenzierten Zahl entspricht.

Die [!DNL Experience Manager] Das -Desktop-Programm weist keinen konfigurierbaren Timeout-Wert auf, der die Verbindung zwischen [!DNL Experience Manager] Server und das Desktop-Programm nach einem festen Zeitintervall. Wenn beim Hochladen großer Assets nach einiger Zeit ein Verbindungs-Timeout eintritt, versucht das Programm, das Asset einige Male hochzuladen, indem es den Timeout-Wert für den Upload erhöht. Es gibt keine empfohlene Vorgehensweise, um die Standardeinstellungen für den Timeout zu ändern.

## Caching und Kommunikation mit AEM {#caching-and-communication-with-aem}

Das AEM-Desktop-Programm bietet interne Caching- und Hintergrundupload-Funktionen, um das Endbenutzererlebnis zu verbessern. Wenn Sie eine große Datei speichern, wird sie zuerst lokal gespeichert, sodass Sie Ihre Arbeit fortsetzen können. Nach einer gewissen Zeit (momentan 30 Sekunden) wird die Datei dann im Hintergrund an den AEM-Server gesendet.

Im Gegensatz zu Creative Cloud Desktop oder anderen Dateisynchronisierungslösungen wie Microsoft One Drive ist das AEM Desktop-Programm kein vollständiger Desktop Sync-Client. Der Grund dafür liegt darin, dass sie Zugriff auf das gesamte AEM Assets-Repository bietet, das für eine vollständige Synchronisierung extrem umfangreich sein kann (mehrere hunderte Gigabyte oder Terabyte).

Das Caching bietet die Möglichkeit, den Mehraufwand bezüglich des Netzwerks/Speichers auf eine Teilmenge von Assets zu beschränken, die für den Benutzer relevant sind.

>[!CAUTION]
>
>Adobe empfiehlt, die Erstellung von Miniaturbildern zu deaktivieren, um die Suche zu beschleunigen. Wenn Sie Symbolvorschauen aktivieren, speichert das Programm die digitalen Assets beim Navigieren durch den gemounteten Ordner zwischen. Das Programm lädt auch Assets herunter, die dem Benutzer möglicherweise unwichtig sind. Dadurch wird der Server geladen, die Bandbreite des Benutzers verbraucht und mehr Speicherplatz belegt.

So führt das AEM-Desktop-Programm das Caching durch:

* Wenn Sie einen Ordner im Finder öffnen und dort Miniaturansichten oder eine Vorschau von Dateien angezeigt wird, speichert das Desktop-Programm die Datei binär zwischen. Wenn Sie eine Datei in einer Anwendung öffnen, speichert das Programm die Datei auch binär zwischen.
* Wenn Sie Dateien über Finder oder andere Desktop-Programme speichern, wird die Datei zunächst lokal gespeichert (zwischengespeichert) und das Betriebssystem wird benachrichtigt. Die Datei wird dann im Hintergrund in die Warteschlange zum Hochladen auf den Server gestellt und schließlich über das Netzwerk hochgeladen. Wenn ein Netzwerkfehler auftritt, versucht das Desktop-Programm erneut, die gesamte Datei hochzuladen, und zwar maximal dreimal. Wenn der Upload nach drei Wiederholungen fehlschlägt, wird die Datei als in Konflikt stehende Datei markiert und der Status wird im Fenster mit dem Upload-Status der Warteschlange im Hintergrund angezeigt. Das Desktop-Programm versucht nicht mehr, die Datei zu aktualisieren. Der Benutzer sollte die Datei aktualisieren und nach dem Wiederherstellen der Verbindung erneut hochladen.

Es wird nicht jeder Vorgang lokal zwischengespeichert. Folgendes wird sofort ohne lokales Caching an den AEM-Server gesendet:

* Jegliche Vorgänge für Ordner, z. B. Erstellen, Löschen usw.
* Mithilfe der in Version 1.4 eingeführten Funktion „Folder Upload“ (Ordner hochladen) wird eine lokale Ordnerhierarchie ohne lokales Caching der Dateien hochgeladen.

## Individuelle Vorgänge {#individual-operations}

Lesen Sie bei der Fehlerbehebung der suboptimierten Leistung für einzelne Benutzer zunächst den Abschnitt [App-Einschränkungen](#limitations). Die folgenden Abschnitte umfassen Vorschläge zur Verbesserung der Performance für einzelne Benutzer.

## Bandbreitenempfehlungen {#bandwidth-recommendations}

Die für einen einzelnen Benutzer verfügbare Bandbreite spielt eine entscheidende Rolle bei der Performance des WebDAV/SMB-Clients.

Adobe empfiehlt, dass die Upload-Geschwindigkeit eines einzelnen Benutzers nahe 10 MBit/s liegt. Bei drahtlosen Verbindungen wird die Bandbreite oftmals zwischen mehreren Benutzern aufgeteilt. Wenn mehrere Benutzer gleichzeitig Aufgaben durchführen, die Netzwerkbandbreite verbrauchen, kann sich die Performance weiter verschlechtern. Verwenden Sie eine kabelgebundene Verbindung, um derartige Probleme zu vermeiden.

<!-- AG, 8/18: The Windows KB article is removed by MS now. Giving 404. Also, Win 7 support is gone and the desktop app is also not supported on Win 7. Hiding this content for now.

## Windows-specific configurations {#windows-specific-configurations}

If you use Experience Manager on Windows, you can configure Windows to enhance the performance of the WebDAV client. For more information, go to [https://support.microsoft.com/en-us/kb/2445570](https://support.microsoft.com/en-us/kb/2445570).

On Windows 7, modifying IE settings can improve the performance of WebDAV. For details, see how to [fix slow WebDAV performance in Windows 7](https://oddballupdate.com/2009/12/fix-slow-webdav-performance-in-windows-7/).
-->

## Gleichzeitig ausgeführte Vorgänge {#concurrent-operations}

Wenn Sie lokal mit einer Datei interagieren, überprüft AEM Desktop, ob in AEM eine neuere Version der Datei verfügbar ist. Wenn eine neue Version verfügbar ist, lädt das Programm eine neue Kopie der Datei in den lokalen Cache herunter. AEM Desktop überschreibt jedoch eine lokal zwischengespeicherte Datei nicht, wenn sie geändert wurde. Diese Funktion verhindert, dass Ihre Arbeit unbeabsichtigt überschrieben wird.

Wenn dieselbe Datei sowohl lokal als auch in AEM geändert wird, überschreibt die lokal geänderte Version die Version in AEM. In diesem Fall ist die vorherige Version in der Zeitleiste des Assets verfügbar. Sie können beide Versionen überprüfen und Konflikte lösen.

Wenn eine lokale Datei mit der auf dem Server verfügbaren Version inkompatibel ist, werden Sie über das Dialogfeld mit dem Status für den Upload im Hintergrund über den Konflikt benachrichtigt. Öffnen Sie zum Beheben des Problems die in Konflikt stehende Datei und speichern Sie sie. Das Speichern der Datei zwingt AEM Desktop zur Synchronisierung Ihrer letzten Änderungen in AEM. Sie können die vorherigen Versionen des Assets in der Zeitachse anzeigen und jegliche Konflikte auflösen.

Berücksichtigen Sie zusätzliche Faktoren, wenn mehrere Benutzer versuchen, in separaten bereitgestellten Verzeichnissen zu arbeiten, die auf dieselbe AEM abzielen. Insbesondere sind die folgenden Faktoren wichtig:

* Die verfügbare Bandbreite im ursprünglichen Netzwerk des Benutzers
* Netzwerkkonfiguration wie Firewalls oder Proxys des ursprünglichen Netzwerks
* Verfügbare Bandbreite im Netzwerk der AEM-Zielinstanz
* Gibt an, ob eine Dispatcher vor der Ziel-AEM-Instanz vorhanden ist
* Aktuelle Auslastung der AEM-Zielinstanz

## Zusätzliche AEM-Konfigurationen {#additional-aem-configurations}

Wenn sich die WebDAV/SMB-Leistung drastisch vermindert, wenn mehrere Benutzer gleichzeitig arbeiten, können Sie in AEM einige Einstellungen konfigurieren, um die Leistung zu verbessern.

## Aktualisieren des Übergangs-Workflows für Assets {#update-asset-transient-workflows}

Sie können AEM Leistung verbessern, indem Sie Übergangs-Workflows für den Workflow DAM-Update-Asset aktivieren. Durch die Aktivierung von Übergangs-Workflows wird die zum Aktualisieren von Assets erforderliche Leistung reduziert, wenn sie in AEM erstellt oder aktualisiert werden.

1. Navigieren Sie in der Experience Manager-Instanz (`https://[aem_server]:[port]/miscadmin`) zu `/miscadmin`.
1. Erweitern Sie in der Navigationsstruktur **Instrumente** > **Workflow** > **Modelle** > **Dam**.
1. Doppelklicken Sie auf **DAM-Update-Asset**.
1. Wechseln Sie im unverankerten Tool-Fenster auf die Registerkarte **Seite** und klicken Sie dann auf **Seiteneigenschaften**.
1. Aktivieren Sie das Kontrollkästchen **Verlaufs-Workflow** und klicken Sie auf **OK**.

### Anpassen der Warteschlange für die Granite-Übergangs-Workflows {#adjust-granite-transient-workflow-queue}

Eine weitere Methode zum Verbessern der AEM-Leistung besteht darin, den Wert der maximal zulässigen parallelen Aufträge für die Warteschlange für Granite-Übergangs-Workflows zu konfigurieren. Der empfohlene Wert beträgt ungefähr die Hälfte der Anzahl der verfügbaren CPUs mit dem Server. Führen Sie die folgenden Schritte aus, um den Wert anzupassen:

1. Navigieren Sie in der zu konfigurierenden AEM-Instanz zu `/system/console/configMgr` (z. B. `https://[aem_server]:[port]/system/console/configMgr`).
1. Suchen Sie nach `QueueConfiguration` und klicken Sie, um die einzelnen Aufträge zu öffnen, bis Sie den Auftrag **Warteschlange für Granite-Übergangs-Workflow** gefunden haben. Klicken Sie dann auf **Bearbeiten**.
1. Ändern Sie den Wert `Maximum Parallel Jobs` und klicken Sie auf **Speichern**.

## AWS-Konfiguration {#aws-configuration}

Aufgrund der Netzwerk-Bandbreitenbeschränkungen kann sich die Leistung von WebDAV/SMB verschlechtern, wenn mehrere Benutzer gleichzeitig arbeiten. Adobe empfiehlt, die Größe der AWS-Instanz für eine AEM-Zielinstanz zu erhöhen, die in AWS ausgeführt wird, um die WebDAV/SMB-Leistung zu verbessern.

Durch diese Maßnahme wird insbesondere die für den Server verfügbare Netzwerkbandbreite erhöht. Im Folgenden finden Sie einige Details dazu:

* Die für eine AWS-Instanz dedizierte Netzwerkbandbreite nimmt mit steigender Größe der Instanz zu. Informationen dazu, wie viel Bandbreite für die einzelnen Instanzgrößen verfügbar ist, finden Sie unter [AWS-Dokumentation](https://aws.amazon.com/ec2/instance-types/).
* Im Rahmen der Fehlerbehebung für einen großen Kunden hat Adobe die Größe seiner AEM-Instanz auf c4.8xlarge konfiguriert, hauptsächlich für die dedizierte Bandbreite von 4000 MBit/s, die bereitgestellt wird.
* Wenn der AEM Instanz eine Dispatcher voraus ist, stellen Sie sicher, dass sie die entsprechende Größe aufweist. Wenn die AEM-Instanz 4000 MBit/s bereitstellt, die Dispatcher jedoch nur 500 MBit/s bereitstellt, beträgt die effektive Bandbreite nur 500 MBit/s. Dies liegt daran, dass die Dispatcher einen Engpass im Netzwerk verursacht.

## Beschränkungen für ausgecheckte Dateien {#checked-out-file-limitations}

Es gibt einige bekannte Einschränkungen hinsichtlich der Interaktion mit ausgecheckten Dateien über Explorer/Finder. Wenn eine Datei ausgecheckt ist, sollte sie mit Ausnahme des Benutzers, der sie auscheckt, für alle Personen schreibgeschützt sein. Diese Regel wird durch die Implementierung des WebDAV/SMB1-Protokolls in AEM erzwungen. Die WebDAV/SMB-Clients des Betriebssystems interagieren jedoch häufig nicht perfekt mit ausgecheckten Dateien. Einige Eigenheiten werden im Folgenden beschrieben.

### Allgemein {#general}

Beim Schreiben in eine ausgecheckte Datei wird die Sperre nur in der AEM WebDAV-Implementierung erzwungen. Daher erzwingen Clients, die WebDAV verwenden, z. B. das Desktop-Programm, nur die Sperre. Die Sperre wird über die AEM Web-Oberfläche nicht erzwungen. In der AEM-Oberfläche wird lediglich für ausgecheckte Assets ein Schloss-Symbol in der Kartenansicht angezeigt. Das Symbol hat nur kosmetischen Charakter und keine Auswirkung auf das AEM-Verhalten.

Die WebDAV-Clients verhalten sich nicht immer erwartungsgemäß. Es können weitere Probleme auftreten. Eine Aktualisierung oder Überprüfung des Assets in AEM ist jedoch eine geeignete Methode, um sicherzustellen, dass ein Asset nicht im Moment bearbeitet wird. Dieses Verhalten ist typisch für WebDAV-Clients des Betriebssystems. Adobe hat keinen Einfluss darauf.

### Windows {#windows}

Das Löschen einer Datei scheint erfolgreich zu sein, da die Datei nicht mehr im Datei-Explorer von Windows angezeigt wird. Das Aktualisieren des Ordners und die Überprüfung in AEM Assets zeigen jedoch, dass die Datei noch vorhanden ist. Darüber hinaus scheint das Bearbeiten von Dateien erfolgreich zu verlaufen (es werden keine Warnungsdialogfelder oder Fehlermeldungen angezeigt). Beim erneuten Öffnen der Datei oder der Überprüfung in AEM Assets wird jedoch deutlich, dass die Datei unverändert ist.

#### MACOS X {#mac-os-x}

Beim Ersetzen einer Datei wird keine Warnung und kein Fehler angezeigt, aber bei der Überprüfung des Assets in AEM wird deutlich, dass es unverändert ist. Aktualisieren oder überprüfen Sie das Asset in AEM, um sicherzustellen, dass es nicht geändert wird.

## Fehlerbehebung bei Problemen mit dem Symbol des Desktop-Programms (macOS X) {#troubleshooting-desktop-app-icon-issues-mac-os-x}

Nach der Installation des Desktop-Programms wird in der Menüleiste das Menüsymbol des Desktop-Programms angezeigt. Wenn das Symbol nicht angezeigt wird, führen Sie die folgenden Schritte aus, um das Problem zu beheben:

1. Öffnen Sie das Terminalfenster des Betriebssystems.
1. Geben Sie den folgenden Befehl in das Befehlszeilenfenster ein und drücken Sie dann die Eingabetaste:

   ```shell
    cd ../Library/Caches.
   ```

1. Geben Sie den folgenden Befehl ein und drücken Sie die Eingabetaste:

   ```shell
   rm -r com.adobe.aem.assetscompanion
   ```

1. Geben Sie den folgenden Befehl ein und drücken Sie die Eingabetaste:

   ```shell
   cd ~/Library/Preferences
   ```

1. Geben Sie den folgenden Befehl ein und drücken Sie die Eingabetaste:

   ```shell
   rm com.adobe.aem.assetscompanion.plist
   ```

1. Geben Sie den folgenden Befehl ein und drücken Sie die Eingabetaste:

   ```shell
   rm ~/Library/Group\ Containers/group.com.adobe.aem.desktop/*
   ```

1. Starten Sie das System neu.

AEM-Desktop unternimmt für beliebige Dateien drei Synchronisierungsversuche. Wenn die Synchronisierung der Datei nach dem dritten Mal fehlschlägt, geht das AEM-Desktop-Programm davon aus, dass für die Datei ein Konflikt vorliegt, und Sie werden über das Statusfenster für den Upload im Hintergrund darüber benachrichtigt. Ein Konfliktzustand gibt an, dass Ihre letzten Änderungen weiterhin lokal verfügbar sind, sie jedoch nicht wieder mit AEM synchronisiert werden. Das AEM-Desktop-Programm versucht nicht mehr zu synchronisieren.

Die einfachste Methode zum Beheben dieser Situation besteht darin, die in Konflikt stehende Datei zu öffnen und erneut zu speichern. Dadurch wird AEM gezwungen, drei weitere Synchronisierungsversuche zu unternehmen. Wenn das Synchronisieren der Datei weiterhin fehlschlägt, lesen Sie für weitere Hilfe die Abschnitte unten.

## Löschen des AEM-Desktop-Caches {#clearing-aem-desktop-cache}

Beim Löschen des Caches von AEM Desktop handelt es sich um eine vorläufige Aufgabe zur Fehlerbehebung, durch die verschiedene Probleme mit AEM Desktop gelöst werden können.

Sie können den Cache löschen, indem Sie das Cache-Verzeichnis des Programms an den folgenden Speicherorten löschen.
Unter Windows: `%LocalAppData%\Adobe\AssetsCompanion\Cache\`

Unter Mac OS: `~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/`

Das Verzeichnis kann sich jedoch in Abhängigkeit vom konfigurierten AEM-Endpunkt des AEM-Desktop-Programms ändern. Der Wert ist eine codierte Version der Ziel-URL. Wenn das Ziel des Programms beispielsweise `http://localhost:4502` ist, lautet der Verzeichnisname `http%3A%2F%2Flocalhost%3A4502%2F`.

Wenn Sie den Cache löschen möchten, löschen Sie das Verzeichnis &lt;Encoded AEM Endpoint>.

>[!NOTE]
>
>Wenn Sie AEM Desktop-Cache löschen, gehen lokale Dateiänderungen verloren, wenn sie nicht mit AEM synchronisiert werden.

>[!NOTE]
>
>Ab der AEM-Desktop-Programm-Version 1.5 gibt es in der Benutzeroberfläche eine Option zum Löschen des Caches.

## Ermitteln der AEM-Desktop-Version {#finding-the-aem-desktop-version}

Das Verfahren zum Ermitteln der AEM Desktop-Version ist für Windows und macOS identisch.

Klicken Sie auf das AEM Desktop-Symbol und wählen Sie dann **About** (Info) aus. Daraufhin wird die Versionsnummer auf dem Bildschirm angezeigt.

## Aktualisieren des AEM-Desktop-Programms auf macOS {#upgrading-aem-desktop-app-on-macos}

Gelegentlich können beim Aktualisieren des AEM-Desktop-Programms auf macOS Probleme auftreten. Diese Probleme werden durch ältere Systemordner für das AEM Desktop-Programm verursacht. Dadurch wird verhindert, dass neue Versionen von AEM Desktop korrekt geladen werden. Zur Behebung dieses Problems können die folgenden Ordner und Dateien manuell entfernt werden.

Bevor Sie die unten aufgeführten Schritte durchführen, ziehen Sie das Programm „Adobe Experience Manager Desktop“ vom Ordner „macOS-Applikationen“ in den Papierkorb. Öffnen Sie dann das Terminal und führen Sie den folgenden Befehl aus, indem Sie Ihr Kennwort angeben, wenn Sie dazu aufgefordert werden.

```shell
sudo rm -rf ~/Library/Application\ Support/com.adobe.aem.desktop
sudo rm -rf ~/Library/Preferences/com.adobe.aem.desktop.plist
sudo rm -rf ~/Library/Logs/Adobe\ Experience\ Manager\ Desktop

sudo find /var/folders -type d -name "com.adobe.aem.desktop" | xargs rm -rf
sudo find /var/folders -type d -name "com.adobe.aem.desktop.finderintegration-plugin" | xargs rm -rf
```

## Speichern einer von anderen Benutzern ausgecheckten Datei {#saving-a-file-checked-out-by-others}

Technische Einschränkungen des Betriebssystems verhindern, dass Benutzer beim Versuch, eine von anderen ausgecheckte Datei zu überschreiben, ein konsistentes Erlebnis haben. Das Erlebnis variiert je nach Programm, das zum Bearbeiten der ausgecheckten Datei verwendet wird. Mitunter zeigt das Programm eine Fehlermeldung mit dem Hinweis an, dass ein Fehler beim Schreiben auf das Laufwerk aufgetreten ist, oder es wird ein scheinbar nicht relevanter oder allgemeiner Fehler angezeigt. Es kann auch sein, dass gar keine Fehlermeldung angezeigt und der Vorgang scheinbar erfolgreich ausgeführt wird.

In diesem Fall können Sie durch Schließen und erneutes Öffnen der Datei feststellen, dass die Inhalte unverändert sind. Bei einigen Programmen wird jedoch möglicherweise eine Sicherung der Datei gespeichert, sodass Ihre Änderungen übernommen werden können.

Unabhängig vom Verhalten bleibt die Datei unverändert, wenn Sie sie einchecken. Selbst wenn eine andere Version der Datei angezeigt wird, erfolgt keine Synchronisierung der Änderungen mit AEM.

## Beheben von Problemen beim Verschieben von Dateien {#troubleshooting-problems-around-moving-files}

Für die Server-API müssen zusätzliche Header und Werte für X-Ziel, X-Tiefe und X-Überschreiben übergeben werden, damit die Verschiebungs- und Kopiervorgänge funktionieren. Die Dispatcher übergibt diese Header nicht standardmäßig, wodurch diese Vorgänge fehlschlagen. Weitere Informationen finden Sie unter [Herstellen einer Verbindung zu AEM hinter einem Dispatcher](install-configure-app-v1.md#connect-to-an-aem-instance-behind-a-dispatcher).

## Beheben von AEM Desktop-Verbindungsproblemen {#troubleshooting-aem-desktop-connection-issues}

### Problem bei SAML-Umleitung {#saml-redirect-issue}

Die häufigste Ursache für Probleme beim Herstellen einer Verbindung zwischen AEM Desktop und Ihrer SSO-fähigen (SAML) AEM-Instanz ist die Tatsache, dass der SAML-Prozess keine Zurückleitung zum ursprünglich angeforderten Pfad durchführt. Alternativ kann die Verbindung zu einem Host umgeleitet werden, der nicht im AEM-Desktop-Programm konfiguriert ist. Führen Sie die folgenden Schritte durch, um den Anmeldungsprozess zu überprüfen:

1. Öffnen Sie einen Webbrowser.
1. Geben Sie in der Adresszeile die URL `/content/dam.json` an.
1. Ersetzen Sie die URL durch die AEM-Zielinstanz, z. B. `https://localhost:4502/content/dam.json`.
1. Melden Sie sich bei AEM an.
1. Überprüfen Sie nach der Anmeldung die aktuelle Adresse des Browsers in der Adresszeile. Sie sollte mit der ursprünglich von Ihnen eingegeben URL übereinstimmen.
1. Stellen Sie sicher, dass alle Angaben vor `/content/dam.json` mit dem im AEM-Desktop-Programm konfigurierten AEM-Zielwert übereinstimmen.

### Problem bei der SSL-Konfiguration {#ssl-configuration-issue}

Die Bibliotheken, die das AEM-Desktop-Programm für die HTTP-Kommunikation verwendet, verwenden eine strikte SSL-Durchsetzung. Manchmal kann eine Verbindung über einen Browser erfolgreich hergestellt werden, aber die Verwendung des AEM-Desktop-Programms ist nicht möglich. Installieren Sie für eine ordnungsgemäße SSL-Konfiguration das fehlende Zwischenzertifikat in Apache. Siehe [How to install an Intermediate CA cert in Apache](https://access.redhat.com/solutions/43575) (nur auf Englisch verfügbar).

## Verwenden AEM Desktop mit Dispatcher {#using-aem-desktop-with-dispatcher}

AEM Desktop arbeitet mit AEM -Implementierungen hinter einer Dispatcher, einer standardmäßigen und empfohlenen Konfiguration für AEM Server. AEM-Dispatcher vor AEM-Autorenumgebungen werden normalerweise so konfiguriert, dass das Caching von DAM-Assets übersprungen wird. Deshalb stellen Dispatcher aus Sicht von AEM Desktop kein zusätzliches Caching bereit. Stellen Sie sicher, dass die Dispatcher-Konfiguration für AEM Desktop angepasst ist. Weitere Informationen finden Sie unter [Herstellen einer Verbindung zu AEM mit einer Dispatcher](install-configure-app-v1.md#connect-to-an-aem-instance-behind-a-dispatcher).

## Überprüfen auf Protokolldateien {#checking-for-log-files}

Je nach Betriebssystem befinden sich die Protokolldateien für das AEM-Desktop-Programm in den folgenden Verzeichnissen:

* Windows: `%LocalAppData%\Adobe\AssetsCompanion\Logs`
* Mac: `~/Library/Logs/Adobe\ Experience\ Manager\ Desktop`
