---
title: Installieren und Konfigurieren des Desktop-Programms, v1.10
description: Installieren und konfigurieren Sie das  [!DNL Experience Manager] -Desktop-Programm Version 1.10 für die Arbeit mit  [!DNL Assets] -Servern und ordnen Sie die Assets als Laufwerk auf Ihrem Desktop zu.
exl-id: 7f3bdfb1-d345-4e48-b020-6e06531f46f2
source-git-commit: 1c7437786a50eeafa884ce92b745f3438b2d2b88
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 74%

---

# Installieren und Konfigurieren des [!DNL Experience Manager]-Desktop-Programms, v1.10 {#install-and-configure-aem-desktop-app}

Mithilfe des [!DNL Experience Manager]-Desktop-Programms können Sie über Ihren lokalen Desktop problemlos auf die Assets in [!DNL Experience Manager] zugreifen und sie in beliebigen Desktop-Programmen verwenden. Assets kann in Mac Finder oder Windows Explorer angezeigt, in Desktop-Programmen bearbeitet und Änderungen werden wieder in [!DNL Experience Manager] gespeichert, sodass beim Hochladen eine neue Version erstellt wird.

Durch diese Integration können verschiedene Rollen Assets zentral innerhalb des Unternehmens in Assets verwalten, in Creative Cloud und anderen Anwendungen darauf zugreifen und verschiedene Standards, einschließlich Branding, problemlos einhalten.

So verwenden Sie das [!DNL Experience Manager]-Desktop-Programm:

* Stellen Sie sicher, dass Ihre [!DNL Experience Manager] Server-Version mit der [!DNL Experience Manager] Desktop-App kompatibel ist. Weitere Informationen finden Sie in der [Kompatibilitätsmatrix](release-notes-of-v1.md#compatibilitymatrix).

* Laden Sie das Programm herunter und installieren Sie es.

* Testen Sie die Verbindung mithilfe einiger Assets. Siehe [Zugreifen auf und Öffnen von Assets über den Desktop](use-app-v1.md#openondesktop).

## Systemanforderungen, Voraussetzungen und Download-Links {#system-requirements-prerequisites-and-download-links}

Detaillierte Informationen finden Sie in den Versionshinweisen zum [[!DNL Experience Manager] -Desktop-Programm](release-notes-of-v1.md).

## Installieren und Verbinden des Programms mit dem [!DNL Experience Manager]-Server {#install-and-connect-aem-desktop-app-to-aem-server}

Weitere Informationen finden Sie unter [Installieren und Verbinden des  [!DNL Experience Manager] -Desktop-Programms mit dem  [!DNL Experience Manager] -Server](use-app-v1.md#installandconnect).

>[!NOTE]
>
>Es kann immer nur eine Instanz des [!DNL Experience Manager]-Desktop-Programms installiert und aktiv sein.

## Dateiverarbeitung {#file-handling}

Beim Ändern einer Datei unter einem vom Desktop-Programm bereitgestellten Netzwerkfreigabe-Speicherort werden die Dateien in zwei Phasen in diesem Verzeichnis gespeichert. In der ersten Phase wird eine Datei lokal gespeichert. Ein Benutzer kann die Datei speichern und deren Bearbeitung fortsetzen, ohne auf den Abschluss der Übertragung warten zu müssen.

In der zweiten Phase lädt das Desktop-Programm die aktualisierte Datei nach einer vordefinierten Verzögerung (z. B. 30 Sekunden) auf den [!DNL Experience Manager]-Server hoch. Dieser Vorgang erfolgt im Hintergrund. Verwenden Sie die Option „View Asset Status“ (Asset-Status anzeigen), um den Status des Upload-Vorgangs anzuzeigen.

1. Hochladen eines Assets in Assets.

1. Klicken Sie in der Symbolleiste auf das Symbol für das [!DNL Experience Manager]-Desktop-Programm.

1. Wählen Sie im Menü die Option „View Asset Status“ (Asset-Status anzeigen) aus.

1. Überprüfen Sie im Dialogfeld den Status des Upload-Vorgangs.

>[!NOTE]
>
>Das [!DNL Experience Manager]-Desktop-Programm kann Assets mit einer Größe von bis zu 40 GB verarbeiten.

## Herstellen einer Verbindung zu einer [!DNL Experience Manager]-Instanz hinter einer Dispatcher {#connect-to-an-aem-instance-behind-a-dispatcher}

Für die Methoden zum Kopieren und Verschieben in der Assets-API ist es erforderlich, dass die folgenden Header an [!DNL Experience Manager] weitergeleitet werden:

* X-Ziel
* X-Tiefe
* X-Überschreiben

[!DNL Experience Manager]-Desktop stellt Verbindungen mit [!DNL Experience Manager] über eine URL her, die einen standardmäßigen Port enthält. Daher sollte die `virtualhosts` in der Dispatcher-Konfiguration die standardmäßige Port-Nummer enthalten. Weitere Informationen zur Konfiguration von `virtualhosts` finden Sie unter [Identifizieren von virtuellen Hosts](https://experienceleague.adobe.com/de/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration#identifying-virtual-hosts-virtualhosts).

Weitere Informationen zum Konfigurieren der Dispatcher für die Übergabe dieser zusätzlichen Header finden Sie unter [&#x200B; der HTTP-Header](https://experienceleague.adobe.com/de/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration#specifying-the-http-headers-to-pass-through-clientheaders).

### Proxy-Unterstützung {#proxy-support}

Die [!DNL Experience Manager]-Desktop-App verwendet den vordefinierten Proxy des Systems, um über HTTPS eine Verbindung zum Internet herzustellen. Das Programm kann die Verbindung nur mit einem Netzwerk-Proxy herstellen, für den keine gesonderte Authentifizierung erforderlich ist.

Wenn Sie Proxyserver-Einstellungen für Windows konfigurieren oder ändern (Internetoptionen > LAN-Einstellungen), starten Sie das [!DNL Experience Manager]-Desktop-Programm neu, damit die Änderungen wirksam werden.

>[!NOTE]
>
>Proxy-Konfiguration wird nur angewendet, wenn Sie das Desktop-Programm starten. Schließen Sie das Programm und starten Sie es erneut, damit Änderungen wirksam werden.

Wenn für den Proxy eine Authentifizierung erforderlich ist, kann die IT-Abteilung die URL von Experience Manager Assets in den Proxyserver-Einstellungen zulassen, um den Programmdatenverkehr durchzulassen.

## Anpassen des Dialogfelds „Asset-Info“  {#customize-the-asset-info-dialog}

Sie können das Dialogfeld „Asset Info“ (Asset-Informationen) anpassen, indem Sie es mit mindestens einer dieser beiden Komponenten überlagern:

* Die Seite der Granite-Benutzeroberfläche unter `/libs/dam/gui/content/assets/moreinfo`.

* HTL-Komponente `/css/javascript` unter `/libs/dam/gui/components/admin/moreinfo`.

Welche Komponente überlagert wird, hängt von der Art der Anpassung ab. Wenn Sie die Komponenten ändern möchten, die als Teil des Dialogfelds „Asset Info“ angezeigt werden, überlagern Sie die Seite der Granite-Benutzeroberfläche. Um den HTML-, CSS- oder JavaScript-Inhalt des Dialogfelds zu ändern, überlagern Sie die HTL-Komponente.

## Verwalten des Caches {#manage-cache}

In Windows befindet sich der Cache unter `%LOCALAPPDATA%\Adobe\AssetsCompanion\Cache\`, wo eine kodierte Version des im Desktop-Programm konfigurierten [!DNL Experience Manager]-Hosts gespeichert ist. Beispiel: `http://localhost:4502` wird als `http%3A%2F%2Flocalhost%3A4502%2F` angezeigt.

Unter macOS X befindet sich ein ähnliches Verzeichnis unter `~/Library/Group Containers/group.com.adobe.aem.desktop/cache`.

### Programminterne Option zum Verwalten des Cache {#in-app-option-to-manage-cache}

Sie können festlegen, wie viel Festplattenspeicher für lokale Caching-Zwecke zur Verfügung gestellt wird. Die Artefakte vom Assets-Server werden für ein reibungsloseres Erlebnis lokal zwischengespeichert. Sie können die Standardeinstellungen Ihren Anforderungen entsprechend anpassen. Außerdem können Sie den Cache löschen, um alle Assets erneut abzurufen. Klicken Sie zum Festlegen der gewünschten Optionen auf das Symbol des Programms und klicken Sie auf **[!UICONTROL Advanced]** > **[!UICONTROL Manage Cache]**.

>[!NOTE]
>
>Wenn Sie den Cache löschen, werden nicht gespeicherte Änderungen beibehalten. Alle Assets, die nicht in den [!DNL Experience Manager]-Server eingecheckt wurden, werden beibehalten und nicht gelöscht.

### Ändern des Cache-Verzeichnisses unter Windows {#change-location-of-cache-on-windows}

Der Standardspeicherort des Caches für das [!DNL Experience Manager]-Desktop-Programm lautet:

* Unter Windows: `%LocalAppData%\Adobe\AssetsCompanion\Cache\EncodedAEMEndpoint`

* Unter Mac OS: `~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/EncodedAEMEndpoint`

Die `EncodedAEMEndpoint` ist die konfigurierte [!DNL Experience Manager]-Endpunkt-URL der App. Der Wert ist eine kodierte Version der Ziel-URL für den [!DNL Experience Manager]-Server. Wenn das Ziel des Programms beispielsweise `http://localhost:4502` ist, lautet der Verzeichnisname `http%3A%2F%2Flocalhost%3A4502`. Der Windows-Pfad zum Cache-Verzeichnis in diesem Beispiel lautet `%LocalAppData%\Adobe\AssetsCompanion\Cache\http%3A%2F%2Flocalhost%3A4502`.

Um das Programm auf einen anderen Ordner oder ein anderes Laufwerk zu verweisen, bearbeiten Sie die Konfigurationsdatei des Programms.

1. Navigieren Sie zum Installationsverzeichnis der App. Der Standardspeicherort unter Windows ist `C:\Program Files (x86)\Adobe\Adobe Experience Manager Desktop`.

1. Bearbeiten Sie die `Adobe Experience Manager Desktop.exe.config` mit einem Texteditor.

   Zum Speichern von an dieser Datei vorgenommenen Änderungen sind Administratorberechtigungen erforderlich.

1. Suchen Sie nach der Zeichenfolge „ProxyCacheRoot.“ Sie stellen fest, dass der zugehörige Wert auf das Cache-Verzeichnis `%LocalAppData%\Adobe\AssetsCompanion\Cache` festgelegt ist. Ändern Sie diesen Wert einfach in einen beliebigen gültigen Pfad.

   >[!NOTE]
   >
   >Das Programm erstellt automatisch ein Unterverzeichnis mit der Bezeichnung *&lt;Encoded AEM Endpoint>*. Dieses Verhalten kann nicht konfiguriert werden.

>[!MORELIKETHIS]
>
>* Sehen Sie sich eine [Einführung in die  [!DNL Experience Manager] -](https://experienceleague.adobe.com/de/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app)-App“ an (5 Minuten, 43 Sekunden).
>* [Verwenden des [!DNL Experience Manager] -Desktop-Programms](use-app-v1.md).
>* [Fehlerbehebung für das [!DNL Experience Manager] -Desktop-Programm](troubleshoot-app-v1.md).
