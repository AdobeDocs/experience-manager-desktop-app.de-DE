---
title: Installieren und Konfigurieren des -Desktop-Programms
description: Installieren und konfigurieren Sie das  [!DNL Adobe Experience Manager] -Desktop-Programm für die Arbeit mit  [!DNL Adobe Experience Manager Assets] -Servern und laden Sie die Assets auf Ihr lokales Dateisystem herunter.
feature: Desktop App,Release Information
exl-id: 422e51c1-c456-4151-bb43-4b3d29a58187
source-git-commit: b1fad118e1ffbd0809afe9a33bcb848648cd8bdd
workflow-type: tm+mt
source-wordcount: '1447'
ht-degree: 64%

---

# Installieren des [!DNL Adobe Experience Manager]-Desktop-Programms {#install-app-v2}

Mithilfe des [!DNL Adobe Experience Manager]-Desktop-Programms können Sie über Ihren lokalen Desktop problemlos auf die Assets in [!DNL Experience Manager] zugreifen und sie in beliebigen nativen Desktop-Programmen verwenden. Assets kann in -Desktop-Programmen als Vorschau angezeigt und geöffnet werden. Sie können im Finder oder Explorer für die Verwendung in Dokumenten angezeigt und lokal bearbeitet werden. Änderungen werden wieder in [!DNL Experience Manager] gespeichert, sodass beim Hochladen eine neue Version erstellt wird.

Eine solche Integration bietet verschiedenen Rollen in der Organisation folgende Möglichkeiten:

* Assets zentral in [!DNL Experience Manager Assets] verwalten.

* Auf die Assets in allen nativen Desktop-Programmen zugreifen, einschließlich Programmen von Drittanbietern und in Adobe Creative Cloud. Dabei können die Benutzerverschiedene Standards – auch für Branding – problemlos einhalten.

So verwenden Sie das [!DNL Experience Manager]-Desktop-Programm:

* Stellen Sie sicher, dass Ihre [!DNL Experience Manager] Version mit dem [!DNL Experience Manager] Desktop-Programm kompatibel ist.

* Laden Sie das Programm herunter und installieren Sie es. Siehe [Installieren des Desktop-Programms](#install-v2) unten.

* Testen Sie die Verbindung mithilfe einiger Assets. Erfahren Sie, [wie Sie Assets durchsuchen und suchen](search.md#browse-search-preview-assets).

## Systemanforderungen, Voraussetzungen und Download-Links {#tech-specs-v2}

Detaillierte Informationen finden Sie in den Versionshinweisen zum [[!DNL Experience Manager] -Desktop-Programm](release-notes.md).

## Upgrade von einer früheren Version {#upgrade-from-previous-version}

Wenn Sie Version 1.x des Desktop-Programms verwenden, sollten Sie sich mit den Unterschieden und Ähnlichkeiten zwischen der vorherigen und der neuesten Version des Programms vertraut machen. Siehe [Neue Funktionen im Desktop-](introduction.md#whats-new-v2) und [Funktionsweise des Programms](release-notes.md#how-app-works).

>[!NOTE]
>
>Zwei Versionen eines Desktop-Programms können nicht gleichzeitig auf einem Computer vorhanden sein. Deinstallieren Sie vor der Installation einer Version die andere Version.

Gehen Sie wie folgt vor, um von einer früheren Version des Programms zu aktualisieren:

1. Synchronisieren Sie vor dem Upgrade alle Assets und laden Sie Ihre Änderungen in [!DNL Experience Manager] hoch. Dadurch wird verhindert, dass beim Deinstallieren der App Bearbeitungen verloren gehen.

1. Deinstallieren Sie die vorherige Version des Programms. Wählen Sie bei der Deinstallation die Option zum Löschen des Cache.

1. Starten Sie den Computer neu.

1. [Laden Sie die neueste Version des Programms herunter](release-notes.md) und [installieren Sie sie](#install-v2). Befolgen Sie die unten stehenden Anweisungen.

## Installieren {#install-v2}

Gehen Sie wie folgt vor, um das Desktop-Programm zu installieren. Deinstallieren Sie ein eventuell vorhandenes Adobe [!DNL Experience Manager]-Desktop-Programm v1.x, bevor Sie die neueste Version des Programms installieren. Weitere Informationen finden Sie oben.

1. Laden Sie das neueste Installationsprogramm von der Seite mit den [Versionshinweisen](release-notes.md) herunter.

1. Halten Sie die URL und die Anmeldeinformationen Ihrer [!DNL Experience Manager]-Bereitstellung bereit.

1. Wenn Sie ein Upgrade von einer anderen Version des Programms durchführen, finden Sie weitere Informationen unter [Aktualisieren des Desktop-Programms](#upgrade-from-previous-version).

1. Überspringen Sie diesen Schritt, wenn Sie [!DNL Experience Manager] as a [!DNL Cloud Service], [!DNL Experience Manager] 6.4.4 oder neuer, oder [!DNL Experience Manager] 6.5.0 oder neuer verwenden. Stellen Sie sicher, dass Ihr [!DNL Experience Manager]-Setup die in den [Versionshinweisen](release-notes.md) erwähnten Kompatibilitätsanforderungen erfüllt. Falls notwendig, laden Sie das passende [Kompatibilitätspaket](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/featurepack/adobe-asset-link-support) herunter und installieren Sie es unter Verwendung von [!DNL Experience Manager] Package Manager als [!DNL Experience Manager]-Administrator. Weitere Informationen zur Installation eines Pakets finden Sie unter [Arbeiten mit Paketen](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/sites/administering/contentmanagement/package-manager).

1. Führen Sie die Installationsprogrammbinärdatei aus und befolgen Sie die Anweisungen auf dem Bildschirm zur Installation.

1. Unter Windows werden Sie vom Installationsprogramm möglicherweise zur Installation von `Visual Studio C++ Redistributable 2015` aufgefordert. Befolgen Sie die Anweisungen auf dem Bildschirm, um es zu installieren. Wenn die Installation fehlschlägt, installieren Sie sie manuell. [Laden Sie das Installationsprogramm herunter](https://www.microsoft.com/de-de/download/details.aspx?id=52685) und installieren Sie sowohl `vc_redist.x64.exe`- als auch `vc_redist.x86.exe`. Führen Sie das Installationsprogramm für das [!DNL Experience Manager]-Desktop-Programm erneut aus.

1. Starten Sie den Computer nach Aufforderung neu. Starten und konfigurieren Sie das Desktop-Programm.

1. Um das Programm mit einem [!DNL Experience Manager]-Repository zu verbinden, klicken Sie auf das Programmsymbol in der Ablage und starten Sie das Programm. Geben Sie die Adresse des [!DNL Experience Manager]-Servers in folgendem Format ein: `https://[aem_server]:[port]/`.

   Klicken Sie auf **[!UICONTROL Connect]** und geben Sie die Anmeldeinformationen ein.

   ![Verbindungsbildschirm des Desktop-Programms zur Eingabe der Server-Adresse](assets/connect_da2.png)

   *Abbildung: Verbindungsbildschirm zur Eingabe der Server-Adresse.*

   Wählen Sie **[!UICONTROL Remember Connection]** aus, damit Sie nicht bei jeder Anmeldung bei der Desktop-Anwendung die Verbindungsdetails eingeben müssen.

   >[!CAUTION]
   >
   >Stellen Sie sicher, dass vor oder nach der Adresse des [!DNL Experience Manager]-Servers keine Leerzeichen am Anfang oder Ende stehen. Andernfalls kann die App keine Verbindung zum [!DNL Experience Manager]-Server herstellen.

1. [Optional] Klicken Sie auf **[!UICONTROL I want to connect a different way]** und klicken Sie auf **[!UICONTROL Adobe login]** , um sich mithilfe von Adobe Identity Management Service (IMS) beim Experience Manager Assets-Server anzumelden. Mit der IMS-Anmeldung kann die Desktop-App die Aktualisierung des Zugriffstokens automatisch durchführen, sodass Benutzende bis zu 14 Tage angemeldet bleiben können. Klicken Sie auf **[!UICONTROL Direct login]** , um die Standardanmeldung mit den Anmeldeinformationen des Benutzers auf dem [!DNL Experience Manager]-Server durchzuführen.

   ![Adobe-Anmeldung](assets/adobe-login.png)

1. Nach erfolgreicher Verbindung können Sie die Liste der Ordner und Assets anzeigen, die im Stammordner des [!DNL Experience Manager]-DAM verfügbar sind. Sie können die Ordner im Programm durchsuchen.

   ![Nach der Anmeldung zeigt das Programm den DAM-Inhalt an](assets/firstview_da2.png)

   *Abbildung: Das Programm zeigt nach der Anmeldung den DAM-Inhalt an*

1. ([!DNL Experience Manager] 6.5.1 oder höher) Wenn Sie das -Desktop-Programm mit [!DNL Experience Manager] 6.5.1 oder höher verwenden, aktualisieren Sie den S3- oder Azure-Connector auf Version 1.10.4 oder höher. Siehe [Azure-Connector](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/deploying/data-store-config#azure-data-store) oder [S3-Connector](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/deploying/data-store-config#amazon-s-data-store).

   Wenn Sie Adobe Managed Services (AMS)-Kunde sind, wenden Sie sich an den Adobe-Support.

## Festlegen von Voreinstellungen {#set-preferences}

Um die Voreinstellungen zu ändern, klicken Sie auf das Symbol ![Weitere Optionen](assets/do-not-localize/more_options_da2.png) und auf das Symbol **[!UICONTROL Preference]** ![Voreinstellungen](assets/do-not-localize/preferences_icon_da2.png). Passen Sie die Werte im Fenster **[!UICONTROL Preferences]** wie folgt an:

* [!UICONTROL Launch the application on logon].

* [!UICONTROL Show a window when the application starts].

* **[!UICONTROL Cache Directory]**: Speicherort des lokalen Caches der App (sie enthält die lokal heruntergeladenen Assets).

* **[!UICONTROL Network Drive Letter]**: Der Laufwerksbuchstabe, der für die Zuordnung zum [!DNL Experience Manager]-DAM verwendet wird. Ändern Sie diesen Netzlaufwerkbuchstaben nicht, wenn Sie sich nicht sicher sind. Das Programm kann jedem Laufwerksbuchstaben unter Windows zugeordnet werden. Wenn zwei Benutzer Assets aus unterschiedlichen Laufwerksbuchstaben platzieren, können sie die Assets des jeweils anderen nicht sehen. Der Pfad der Assets ändert sich. Die Assets bleiben in der Binärdatei (z. B. INDD) und werden nicht entfernt. Das Programm listet alle verfügbaren Laufwerksbuchstaben auf und verwendet standardmäßig den letzten verfügbaren Buchstaben, also meist `Z`.

* **[!UICONTROL Maximum Cache Size]**: Zulässiger Cache auf der Festplatte in GB, der zum Speichern lokal heruntergeladener Assets verwendet wird.

* **[!UICONTROL Current cache size]**: Speichergröße der lokal heruntergeladenen Assets. Die Informationen werden erst angezeigt, nachdem Assets mit dem Programm heruntergeladen wurden.

* **[!UICONTROL Automatically download linked assets]**: Beim Herunterladen der Originaldatei werden Assets, die in unterstützten nativen Creative Cloud-Programmen platziert werden, automatisch abgerufen.

* **[!UICONTROL Maximum number of downloads]**: ![Vorsichtssymbol](assets/do-not-localize/caution-icon.png) Mit Vorsicht ändern. Beim erstmaligen Herunterladen von Assets (über die Option „Anzeigen“, „Öffnen“, „Bearbeiten“, „Herunterladen“ usw.) werden die Assets nur heruntergeladen, wenn der Stapel weniger als diese Anzahl enthält. Der Standardwert ist 50. Ändern Sie sie nicht, wenn Sie sich nicht sicher sind. Eine Erhöhung des Werts kann zu längeren Wartezeiten führen, während eine Verringerung des Werts verhindern kann, dass alle erforderlichen Assets oder Ordner in einem Versuch heruntergeladen werden.

* **[!UICONTROL Use legacy conventions when creating nodes for assets and folders]**: ![Vorsichtssymbol](assets/do-not-localize/caution-icon.png) Mit Vorsicht ändern. Mit dieser Einstellung kann das Programm das Programmverhalten der Version 1.10 beim Hochladen von Ordnern emulieren. In Version 1.10 berücksichtigen die im Repository erstellten Knotennamen die Leerzeichen und Groß-/Kleinschreibung der vom Benutzer angegebenen Ordnernamen. In Version 2.1 des Programms werden die zusätzlichen Leerzeichen in den Ordnernamen jedoch in Bindestriche umgewandelt. Wenn Sie beispielsweise `New Folder` oder `new   folder` hochladen, wird derselbe Knoten im Repository erstellt, wenn die Option nicht ausgewählt ist und das Standardverhalten in Version 2.1 beibehalten wird. Wenn diese Option ausgewählt ist, werden für die beiden oben genannten Ordner im Repository verschiedene Knoten erstellt, die dem Verhalten der App v1.10 entsprechen.

  Das Standardverhalten von v2.1 bleibt unverändert: Es ersetzt mehrere Leerzeichen in Ordnernamen durch Bindestriche im Repository-Knotennamen und konvertiert Knotennamen in Kleinbuchstaben.

* **[!UICONTROL Upload Acceleration]**: ![Vorsichtssymbol](assets/do-not-localize/caution-icon.png) Mit Vorsicht ändern. Beim Hochladen von Assets kann das Programm gleichzeitige Uploads verwenden, um die Upload-Geschwindigkeit zu steigern. Sie können die Zahl der gleichzeitigen Uploads erhöhen, indem Sie den Schieberegler nach rechts verschieben. Der Schieberegler auf der linken Seite bedeutet keine gleichzeitige Verarbeitung (Singlethread-Upload), die mittlere Position entspricht zehn gleichzeitigen Threads und die maximale Begrenzung auf der rechten Seite entspricht 20 gleichzeitigen Threads. Eine höhere Parallelitätsgrenze ist ressourcenintensiver.

Um die nicht verfügbaren Voreinstellungen zu aktualisieren, melden Sie sich beim [!DNL Experience Manager]-Server ab und aktualisieren Sie anschließend. Klicken Sie nach dem Aktualisieren der Voreinstellungen auf ![Voreinstellungen speichern](assets/do-not-localize/save_preferences_da2.png).

![Voreinstellungen und Einstellungen für das Desktop-Programm](assets/preferences_da2.png)

*Abbildung: Voreinstellungen für das Desktop-Programm.*

### Proxy-Unterstützung {#proxy-support}

Die [!DNL Experience Manager]-Desktop-App verwendet den vordefinierten Proxy des Systems, um über HTTPS eine Verbindung zum Internet herzustellen. Das Programm kann die Verbindung nur mit einem Netzwerk-Proxy herstellen, für den keine gesonderte Authentifizierung erforderlich ist.

Wenn Sie Proxy-Server-Einstellungen für Windows konfigurieren oder ändern (Internetoptionen > LAN-Einstellungen), starten Sie das [!DNL Experience Manager]-Desktop-Programm neu, damit die Änderungen wirksam werden. Die Proxy-Konfiguration wird angewendet, wenn Sie das Desktop-Programm starten. Schließen Sie das Programm und starten Sie es erneut, damit Änderungen wirksam werden.

Wenn für den Proxy eine Authentifizierung erforderlich ist, kann die IT-Abteilung die URL von [!DNL Experience Manager Assets] in den Proxy-Server-Einstellungen zulassen, um den Programm-Traffic durchzulassen.

## Deinstallieren des Programms {#uninstall-the-app}

Gehen Sie wie folgt vor, um das Programm unter Windows zu deinstallieren:

1. Laden Sie alle Änderungen in [!DNL Experience Manager] hoch, um den Verlust von Änderungen zu vermeiden. Siehe [Bearbeiten von Assets und Hochladen aktualisierter Assets in [!DNL Experience Manager]](upload-assets.md#edit-assets-upload-updated-assets). Melden Sie sich ab und beenden ([!UICONTROL Exit]) Sie das Programm.

1. Entfernen Sie die Anwendung so, wie Sie auch jede andere Anwendung im Betriebssystem entfernen würden. Deinstallieren Sie sie unter Windows über „Programme hinzufügen und entfernen“.

1. Um den Cache und die Protokolle zu entfernen, aktivieren Sie das entsprechende Kontrollkästchen.

   ![Dialogfeld zum Deinstallieren mit Auswahl zum Entfernen von Protokollen und Cache](assets/uninstall_da2.png)

1. Folgen Sie den angezeigten Anweisungen. Starten Sie nach Abschluss des Vorgangs den Computer neu.

Gehen Sie wie folgt vor, um das Programm auf einem Mac zu deinstallieren:

1. Laden Sie alle Änderungen in [!DNL Experience Manager] hoch, um den Verlust von Änderungen zu vermeiden. Siehe [Bearbeiten von Assets und Hochladen aktualisierter Assets in [!DNL Experience Manager]](upload-assets.md#edit-assets-upload-updated-assets). Melden Sie sich ab und beenden ([!UICONTROL Exit]) Sie das Programm.

1. Entfernen Sie `Adobe Experience Manager Desktop.app` aus `/Applications`.

Alternativ können Sie den folgenden Befehl am Terminal ausführen, um die internen Anwendungscaches auf der Mac zu bereinigen und die App zu deinstallieren:

```shell
/Applications/Adobe Experience Manager Desktop/Contents/Resources/uninstall-osx/uninstall.sh
```
