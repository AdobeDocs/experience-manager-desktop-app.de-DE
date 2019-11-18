---
title: Installieren und Konfigurieren von AEM Desktop App Version 1.x
seo-title: Installieren und Konfigurieren von AEM Desktop App Version 1.x
description: Installieren und konfigurieren Sie AEM Desktop-App Version 1.x für die Verwendung mit AEM Assets-Servern und ordnen Sie die Assets als Laufwerk auf Ihrem Desktop zu.
seo-description: Installieren und konfigurieren Sie AEM Desktop-App Version 1.x für die Verwendung mit AEM Assets-Servern und ordnen Sie die Assets als Laufwerk auf Ihrem Desktop zu.
uuid: 79bc9de9-5708-41f9-ac43-68c1fd2a2129
contentOwner: Agupta
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: f6365302-1690-4719-9b8c-035719422740
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 7ce29042aff6d4caea0e7b8a56673d4bfed03a45

---


# Installieren und Konfigurieren der AEM Desktop-App v1.x {#install-and-configure-aem-desktop-app}

Installieren und konfigurieren Sie die AEM-Desktop-App für die Verwendung mit AEM Assets-Servern und laden Sie die Assets in Ihr lokales Dateisystem herunter. So verwenden Sie die AEM-Desktop-App

* Stellen Sie sicher, dass Ihre AEM-Serverversion von der AEM-Desktop-App unterstützt wird. Weitere Informationen finden Sie in der [Kompatibilitätsmatrix](release-notes-of-v1.md#compatibilitymatrix).
* Laden Sie die Applikation herunter und installieren Sie sie.
* Testen Sie die Verbindung mithilfe einiger Assets. See [Access and open assets on your desktop](use-app-v1.md#openondesktop).

## Systemanforderungen, Voraussetzungen und Download-Links {#system-requirements-prerequisites-and-download-links}

For detailed information, see the [AEM desktop app release notes](release-notes-of-v1.md).

## Install and connect AEM desktop app to AEM server {#install-and-connect-aem-desktop-app-to-aem-server}

For details, see [Install and connect AEM desktop app to AEM server](use-app-v1.md#installandconnect).

>[!NOTE]
>
>Es kann jeweils nur eine Instanz der AEM-Desktop-App installiert und aktiv sein.

## Proxy-Unterstützung {#proxy-support}

Die AEM-Desktop-App verwendet den vordefinierten Proxy des Systems, um über HTTPS eine Verbindung zum Internet herzustellen. Die App kann die Verbindung nur mit einem Netzwerk-Proxy herstellen, für den keine gesonderte Authentifizierung erforderlich ist.

Wenn Sie die Proxy-Servereinstellungen für Windows konfigurieren oder ändern (Internetoptionen &gt; LAN-Einstellungen), starten Sie die AEM-Desktop-App neu, damit die Änderungen wirksam werden.

Wenn für den Proxy eine Authentifizierung erforderlich ist, kann die IT-Abteilung die URL von AEM Assets in den Proxyserver-Einstellungen der Whitelist hinzufügen, um den Applikationsdatenverkehr durchlaufen zu lassen.

## Dateiverarbeitung {#file-handling}

Wenn Sie eine Datei von einem Netzwerkfreigabeort ändern, der von der Desktop-App bereitgestellt wird, werden die Dateien in zwei Phasen an diesem Speicherort gespeichert. In der ersten Phase wird eine Datei lokal gespeichert. Ein Benutzer kann die Datei speichern und deren Bearbeitung fortsetzen, ohne auf den Abschluss der Übertragung warten zu müssen.

In der zweiten Phase lädt die Desktop-App die aktualisierte Datei nach einer vordefinierten Verzögerung (z. B. 30 s) auf den AEM-Server hoch. Dieser Vorgang erfolgt im Hintergrund. Verwenden Sie die Option „View Asset Status“ (Asset-Status anzeigen), um den Status des Upload-Vorgangs anzuzeigen.

1. Hochladen eines Assets in AEM Assets.
1. Klicken Sie in der Symbolleiste auf das Symbol für die AEM-Desktop-App bzw. tippen Sie auf das Symbol für die AEM-Desktop-App.
1. Wählen Sie im Menü die Option „View Asset Status“ (Asset-Status anzeigen) aus.
1. Überprüfen Sie im Dialogfeld den Status des Upload-Vorgangs.

>[!NOTE]
>
>Die AEM-Desktop-App kann bis zu 40 GB mit Assets verarbeiten.

## Herstellen einer Verbindung mit einer AEM-Instanz hinter einem Dispatcher {#connect-to-an-aem-instance-behind-a-dispatcher}

Für die Methoden zum Kopieren und Verschieben in der Assets-API ist es erforderlich, dass die folgenden Header an AEM weitergeleitet werden:

* X-Ziel
* X-Tiefe
* X-Überschreiben

AEM Desktop stellt Verbindungen mit AEM über eine URL her, die einen standardmäßigen Port enthält. Therefore, the *virtualhosts* setting in the dispatcher configuration should include the default port number. Weitere Informationen zur Konfiguration von „virtualhosts“ finden Sie unter [Identifizieren von virtuellen Hosts](https://docs.adobe.com/content/help/en/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html#identifying-virtual-hosts-virtualhosts).

For additional information on configuring the dispatcher to pass through these additional headers, see [Specifying the HTTP Headers](https://docs.adobe.com/content/help/en/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html#specifying-the-http-headers-to-pass-through-clientheaders).

## Anpassen des Dialogfelds „Asset Info“{#customize-the-asset-info-dialog}

Sie können das Dialogfeld „Asset Info“ (Asset-Informationen) anpassen, indem Sie es mit mindestens einer dieser beiden Komponenten überlagern:

* The Granite user interface page at `/libs/dam/gui/content/assets/moreinfo`
* Die HTL- `/css/javascript` Komponente am `/libs/dam/gui/components/admin/moreinfo`

Welche Komponente überlagert wird, hängt von der Art der Personalisierung ab. Wenn Sie die Komponenten ändern möchten, die als Teil des Dialogfelds „Asset Info“ angezeigt werden, überlagern Sie die Seite der Granite-Benutzeroberfläche. Um den HTML/CSS/Javascript-Inhalt des Dialogfelds zu ändern, überlagern Sie die HTL-Komponente.

## Verwalten des Cache {#manage-cache}

On Windows, the cache is at `%LOCALAPPDATA%\Adobe\AssetsCompanion\Cache\`, where is an encoded version of the AEM host configured in the desktop app. Beispiel: `http://localhost:4502` wird wie `http%3A%2F%2Flocalhost%3A4502%2F`.

On Mac OS X, a similar directory is at `~/Library/Group Containers/group.com.adobe.aem.desktop/cache`.

### Option zum Verwalten des Cache in der App {#in-app-option-to-manage-cache}

Sie können festlegen, wie viel Festplattenspeicher für lokale Caching-Zwecke zur Verfügung gestellt wird. Die Artefakte vom AEM Assets-Server werden für ein reibungsloseres Erlebnis lokal zwischengespeichert. Sie können die Standardeinstellungen Ihren Anforderungen entsprechend anpassen. Außerdem können Sie den Cache löschen, um alle Assets erneut abzurufen. To set the desired options, click the application's icon and click **[!UICONTROL Advanced]** &gt; **[!UICONTROL Manage Cache]**. ****

>[!NOTE]
>
>Wenn Sie den Cache löschen, werden nicht gespeicherte Änderungen beibehalten. Alle Elemente, die nicht auf dem AEM-Server eingecheckt wurden, werden beibehalten und nicht gelöscht.

### Ändern des Cache-Verzeichnisses unter Windows {#change-location-of-cache-on-windows}

Der Standardspeicherort des Cache für die AEM-Desktop-App ist:

* Windows: `%LocalAppData%\Adobe\AssetsCompanion\Cache\EncodedAEMEndpoint`
* Mac: `~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/EncodedAEMEndpoint`

`EncodedAEMEndpoint` ist die konfigurierte AEM-Endpunkt-URL der AEM-Desktop-App. Der Wert ist eine codierte Version der Ziel-URL für den AEM-Server. For example, if the application is targeting `http://localhost:4502`, the directory name is `http%3A%2F%2Flocalhost%3A4502`. Der Windows-Pfad zum Cacheverzeichnis in diesem Beispiel ist %LocalAppData%\Adobe\AssetsCompanion\Cache\http%3A%2F%2Flocalhost%3A4502.

Um die Applikation auf einen anderen Ordner oder ein anderes Laufwerk zu verweisen, bearbeiten Sie die Konfigurationsdatei der Applikation.

1. Navigieren Sie zum Installationsverzeichnis der App. Der Standardspeicherort unter Windows ist `C:\Program Files (x86)\Adobe\Adobe Experience Manager Desktop`.
1. Bearbeiten Sie die Datei „Adobe Experience Manager Desktop.exe.config“ mit einem Texteditor.

   Zum Speichern der Änderungen in dieser Datei sind Administratorrechte erforderlich.

1. Suchen Sie nach der Zeichenfolge „ProxyCacheRoot“. Sie stellen fest, dass der zugehörige Wert auf das Cache-Verzeichnis „%LocalAppData%\Adobe\AssetsCompanion\Cache“ festgelegt ist. Ändern Sie diesen Wert einfach in einen beliebigen gültigen Pfad.

   >[!NOTE]
   >
   >The app automatically creates an *&lt;Encoded AEM Endpoint&gt;* subdirectory; this behavior is not configurable.

## Zusätzliche Ressourcen {#additional-resources}

* [Einführung in die AEM-Desktop-App](https://helpx.adobe.com/experience-manager/kt/eseminars/ccoo-aem-desktop-app.html)
* [Verwenden der AEM-Desktop-App](use-app-v1.md)

* [Einchecken/Auschecken mit der AEM-Desktop-App](https://helpx.adobe.com/experience-manager/kt/assets/using/checkin-checkout-technical-video-understand.html)
* [Verwenden der Desktop-App mit AEM Assets](https://helpx.adobe.com/experience-manager/kt/assets/using/checkin-checkout-technical-video-understand.html)
* [Fehlerbehebung für AEM-Desktop-App](troubleshoot-app-v1.md)