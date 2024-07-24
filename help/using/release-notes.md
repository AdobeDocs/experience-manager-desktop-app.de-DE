---
title: „Versionshinweise zum [!DNL Adobe Experience Manager]-Desktop-Programm“
description: Versionshinweise, Verbesserungen, neue Funktionen, Kompatibilität und Download-Links für das  [!DNL Adobe Experience Manager] -Desktop-Programm.
mini-toc-levels: 1
feature: Desktop App,Release Information
exl-id: e058e7a2-fcc8-4ad1-899e-20695db6bc72
source-git-commit: 11a4397aa54cd58395b02273864f4edd843357a1
workflow-type: tm+mt
source-wordcount: '1953'
ht-degree: 66%

---

# [!DNL Adobe Experience Manager] Versionshinweise zum Desktop-Programm {#release-notes-v2}

Die Versionsinformationen zur neuesten Desktop-Anwendungsversion 2.3.1 finden Sie unten. Das Veröffentlichungssdatum ist der Freitag, 25. Juli 2024.

Die neueste Version der Desktop-Anwendung enthält die folgenden Fehlerbehebungen und Verbesserungen:

* Das neue Enterprise Windows-Installationsprogramm installiert die Anwendung unter Programmdateien.
* Unterstützung für **Grundlegende Authentifizierung** bei AEM- und SSO-Anmeldungen.
* Konfigurierbare Anzahl von Assets, die während des Upload-Vorgangs zulässig sind.

Die **unterstützten [!DNL Experience Manager]-Versionen** sind:

* [!DNL Experience Manager] as a [!DNL Cloud Service]. Siehe [Versionshinweise](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/home).
* [!DNL Experience Manager] 6.5.0 oder höher, für Adobe Managed Services (AMS) oder On-Premise. Weitere Informationen finden Sie in den [Versionshinweisen zum Service Pack](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/release-notes/release-notes).

Das [!DNL Adobe Experience Manager]-Desktop-Programm ist für die folgenden **Betriebssysteme** verfügbar:

* macOS X 10.14 oder höher mit aktuellen Fehlerbehebungen.
* Windows 10 mit den aktuellen Service Packs und Fehlerbehebungen.

Für AEM Desktop App-Version 2.3.1 und neuere Versionen sind zwei Versionen des Windows-Installationsprogramms verfügbar. Das Basisinstallationsprogramm installiert die AEM Desktop App im Verzeichnis der lokalen App-Daten des Benutzers. Adobe empfiehlt diesen Installationsprozess für die meisten Benutzer. Es ist auch ein Enterprise Windows-Installationsprogramm verfügbar, das die AEM Desktop App unter dem Verzeichnis der freigegebenen Programmdateien installiert. Diese beiden Installationsprogramme installieren dieselbe Version der AEM Desktop App, ohne dass sich die Funktionalität unterscheidet.

Die **Download-URLs** für die unterstützten Betriebssysteme sind:

| Betriebssystem | [!DNL Experience Manager] as a [!DNL Cloud Service] | [!DNL Experience Manager] 6.x |
|---|---|---|
| macOS (v2.3.1) | [Download-Link](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faemcloud.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faemcloud%2Fpublic%2Faem-desktop-app%2Faem-desktop-osx-x64-2.3.1.dmg&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081954149%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=mwSX5ilZL0he2raIx8t5ecQ%2FWuizky4MpcCXX3mEN38%3D&amp;reserved=0) | [Download-Link](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faem.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Fadobe%2Faem-desktop-app%2Faem-desktop-osx-x64-2.3.1.dmg&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081981239%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=LJH3OCFq7yRykN4wU8HN9%2FBXC%2BjfXLJH4QizeFZfRHE%3D&amp;reserved=0) |
| macOS Apple Silicon (M1) (v2.3.1) | [Download-Link](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faemcloud.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faemcloud%2Fpublic%2Faem-desktop-app%2Faem-desktop-osx-arm64-2.3.1.dmg&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081965822%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=2YENn0tDduiucogClt6aBZHDOE6dbzBdigq8VQawIO0%3D&amp;reserved=0) | [Download-Link](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faem.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Fadobe%2Faem-desktop-app%2Faem-desktop-osx-arm64-2.3.1.dmg&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081986151%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=jCepldg4dMej0%2BrK2mUonXwqsWL8ksE8%2BLMSgsH9qTA%3D&amp;reserved=0) |
| Windows 64-Bit (v2.3.1) | [Download-Link](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faemcloud.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faemcloud%2Fpublic%2Faem-desktop-app%2Faem-desktop-win-x64-2.3.1.exe&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081970892%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=sRn2UWW%2Bi7SMEvSO74ZGGvJ40vHh1KhLc7zAfKc37Es%3D&amp;reserved=0) | [Download-Link](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faem.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Fadobe%2Faem-desktop-app%2Faem-desktop-win-x64-2.3.1.exe&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081991004%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=aQWZtEK%2F3cWX8n8Au%2FwZ5Zd9xPVo5phvk%2FuF%2Be0HRrE%3D&amp;reserved=0) |
| Windows 64-Bit Enterprise (v2.3.1) | [Download-Link](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faemcloud.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faemcloud%2Fpublic%2Faem-desktop-app%2Faem-desktop-win-x64-2.3.1.msi&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081976350%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=v9C0sLDSkuL%2FMIyae2WkbitJPVgSlAw2BqcaH5Im0uw%3D&amp;reserved=0) | [Download-Link](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faem.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Fadobe%2Faem-desktop-app%2Faem-desktop-win-x64-2.3.1.msi&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081995827%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=2btCh0aIrUBiyeG37K9YorvzTeIJOggbq%2FRauUMn4LY%3D&amp;reserved=0) |
| macOS (v2.3.0) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.3.0.dmg) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.3.0.dmg) |
| macOS Apple-Chip (M1) (v2.3.0) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.3.0.dmg) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.3.0.dmg) |
| Windows 64-Bit (v2.3.0) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.3.0.exe) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.3.0.exe) |
| macOS (v2.2.2) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.2.2.dmg) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.2.2.dmg) |
| macOS Apple-Chip (M1) (v2.2.2) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.2.2.dmg) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.2.2.dmg) |
| Windows 64-Bit (v2.2.2) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.2.2.exe) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.2.2.exe) |
| macOS (v2.2.1) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.2.1.dmg) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.2.1.dmg) |
| macOS Apple-Chip (M1) (v2.2.1) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.2.1.dmg) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.2.1.dmg) |
| Windows 64-Bit (v2.2.1) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.2.1.exe) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.2.1.exe) |
| macOS (v2.2.0) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.2.0.dmg) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.2.0.dmg) |
| macOS Apple-Chip (M1) (v2.2.0) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.2.0.dmg) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.2.0.dmg) |
| Windows 64-Bit (v2.2.0) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.2.0.exe) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.2.0.exe) |
| macOS (v2.1.5.0) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-2.1.5.0.dmg) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-2.1.5.0.dmg) |
| Windows 64-Bit (v2.1.5.0) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win64-2.1.5.0.exe) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-2.1.5.0.exe) |
| Windows 32-Bit (v2.1.5.0) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win32-2.1.5.0.exe) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-2.1.5.0.exe) |
| macOS (v2.1.4.0) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-2.1.4.0.dmg) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-2.1.4.0.dmg) |
| Windows 64-Bit (v2.1.4.0) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win64-2.1.4.0.exe) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-2.1.4.0.exe) |
| Windows 32-Bit (v2.1.4.0) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win32-2.1.4.0.exe) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-2.1.4.0.exe) |
| macOS (v2.1.3.4) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-2.1.3.4.dmg) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-2.1.3.4.dmg) |
| Windows 64-Bit (v2.1.3.4) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win64-2.1.3.4.exe) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-2.1.3.4.exe) |
| Windows 32-Bit (v2.1.3.1) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win32-2.1.3.1.exe) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-2.1.3.1.exe) |

## Unterstützung verschiedener Asset- und Dateitypen {#support-for-file-types}

Das Programm unterstützt in [!DNL Experience Manager] gespeicherte Assets, die Binärdateien für die grundlegenden Vorgänge darstellen. Das Öffnen von Dateien im nativen Desktop-Programm hängt von der Betriebssystemverknüpfung bestimmter Dateitypen wie PNG oder JPG mit bestimmten Programmen wie Mac Preview oder Adobe Photoshop ab.

Einige Dateitypen unterstützen das Platzieren von verknüpften Assets in der Binärdatei. Das Programm lädt die verknüpften Assets vorab herunter, falls das Asset im [!DNL Experience Manager]-Repository vorhanden ist, wenn diese Binärdateien mit dem Desktop-Programm geöffnet werden. Derzeit werden folgende Dateitypen unterstützt:

* [!DNL Adobe InDesign]-Dateien (INDD-Format)
* [!DNL Adobe Illustrator]-Dateien (AI-Format)
* [!DNL Adobe Photoshop]-Dateien (PS-Format)

Diese Funktion wird in den Versionen [!DNL Adobe Creative Cloud] 2018 und [!DNL Adobe Creative Cloud] 2019 des oben genannten Programms unterstützt. Das Programm verwendet einen heuristischen Best-Match-Ansatz, um die lokalen Desktop-Pfade verknüpfter Assets URLs auf dem [!DNL Experience Manager]-Server zuzuordnen. Dieser Ansatz beruht auf den folgenden Annahmen:

* Pfade zu platzierten Dateien im nativen Programm verwenden einen globalen Desktop-Pfad (platziert von der lokalen Netzwerkfreigabe mit der Option [!UICONTROL Reveal] ).

* Pfade werden von der nativen Anwendung im XMP-Datensatz der Datei gespeichert.

* [!DNL Experience Manager] hat den XMP-Datensatz mit den Pfaden zum Metadaten-Datensatz des Assets extrahiert.

* Die Pfade können Assets in [!DNL Experience Manager] zugeordnet werden, das heißt, die platzierten Dateien befinden sich auch in [!DNL Experience Manager] unter einem zugeordneten Pfad.

## Neue Funktionen, Verbesserungen und Fehlerbehebungen {#what-is-new}

Weitere Informationen finden Sie unter [Neue Funktionen in Version 2.0](introduction.md#whats-new-v2).

**Aktualisierungen in der App v2.3.0**

* Unterstützung für IMS-Anmeldung wurde hinzugefügt. Durch die IMS-Integration kann das Desktop-Programm automatisch das Zugriffstoken aktualisieren, sodass der Benutzer bis zu 14 Tage lang angemeldet bleiben kann.

* Verbesserte Unterstützung für Unternehmens-Proxys und Web-Filterung.

**Aktualisierungen in der Programmversion 2.2.2**

* (Nur Windows) Das Desktop-Programm zeigt nach der Installation der Versionen 2.2.0 und 2.2.1 einen leeren Bildschirm an.

**Aktualisierungen in der Programmversion 2.2.1**

* Das -Desktop-Programm zeigt eine Fehlermeldung zur Zeitüberschreitung der Sitzung an, wenn Sie auf **[!UICONTROL Sign In]** klicken.

* Probleme beim Zugriff auf die Desktop-Anwendung v2.2.0 in macOS.

* Das Desktop-Programm zeigt eine Fehlermeldung an, wenn Sie Assets durch Klicken auf **[!UICONTROL Edited Locally]** sortieren.

**Aktualisierungen in der Programmversion 2.2.0**

* Unterstützung für Apple-Chip (M1).

* Möglichkeit, die Verbindungszeichenfolge beim Anmelden bei der Desktop-Anwendung zu speichern.

**Aktualisierungen in der Programmversion 2.1.5.0**

* Das Desktop-Programm reagiert nicht mehr, wenn Sie Dateien in einen Ordner hochladen, der chinesische Zeichen enthält (ASSETS-9237).

* Das Desktop-Programm ersetzt Punkte in Dateinamen durch Gedankenstriche (ASSETS-10955).

**Aktualisierungen in der Programmversion 2.1.4.0**

Die neue Version der Anwendung enthält Fehlerkorrekturen.

**Aktualisierungen in der Programmversion 2.1.3.4**

Die neue Version des Programms bietet eine Fehlerbehebung.

**Aktualisierungen in der Programmversion 2.1.3.3**

Die neue Version des Programms bietet eine Fehlerbehebung.

**Aktualisierungen in der Programmversion 2.1.3.2**

Diese Version des Programms bietet eine Fehlerbehebung.

**Aktualisierungen in der Programmversion 2.1.3.1**

Folgender Fehler wurde in der aktuellen Version behoben:

* Die Geschwindigkeit beim Upload und Download von Assets wurde verbessert, auch bei großen Assets. In dieser Version wurde ein Problem behoben, bei dem Asset-Uploads mit dem [!DNL desktop app] manchmal fehlschlugen, wenn sehr große Dateien hochgeladen wurden.

**Aktualisierung in der Programmversion 2.1.2.0**

* Dem Hauptmenü des Programms wurde eine neue Option [!UICONTROL Clear Cookies] hinzugefügt. Dies hilft bei potenziellen Anmeldungsproblemen, z. B. beim Wechsel einer Verbindung von einem Server zu einem anderen. Siehe [Löschen von Cookies vor dem Verbinden](/help/using/troubleshoot.md#cannot-login-cookies-issue).

* Es wurde eine neue Option hinzugefügt, mit der die App, falls ausgewählt, Ordner und Dateien mit Knotennamen in [!DNL Adobe Experience Manager] hochladen kann, die mit den lokalen Datei- und Ordnernamen übereinstimmen. Dieser Prozess stellt die Konsistenz zwischen lokalen und hochgeladenen Namen sicher.

  Dieses Verhalten ähnelt dem Standardverhalten in Version 1 des Desktop-Programms. Wenn die Option in der aktuellen Version nicht aktiviert ist, werden Leerzeichen und die Zeichen `% ; # , + ? ^ { } "` in Ordnernamen durch Gedankenstriche in Ordnerpfaden ersetzt. Außerdem werden die Großbuchstaben in Ordnerpfaden in Kleinbuchstaben umgewandelt. In Dateinamen werden die Zeichen `# % { } ? &` jedoch durch einen Bindestrich ersetzt, Leerzeichen und Groß-/Kleinschreibung werden jedoch beibehalten. Weitere Informationen finden Sie in den [Programmvoreinstellungen](/help/using/install-upgrade.md#set-preferences) und unter [Hochladen und Hinzufügen neuer Assets](/help/using/using.md#upload-and-add-new-assets-to-aem).

**Aktualisierung in der Programmversion 2.1.1.0**

* Mit einer erweiterten Einstellung kann das Programm das Programmverhalten der Version 1.10 beim Hochladen von Ordnern emulieren. In Version 1.10 berücksichtigen die im Repository erstellten Knotennamen die vom Benutzer angegebenen Leerzeichen und Groß- und Kleinschreibung der Ordnernamen. In Version 2.1 bleibt das Standardverhalten unverändert: Mehrere Leerzeichen in Ordnernamen werden im Repository-Knotennamen durch Bindestriche ersetzt und Knotennamen werden in Kleinbuchstaben umgewandelt. Weitere Informationen finden Sie in den [Programmvoreinstellungen](/help/using/install-upgrade.md#set-preferences).

**Aktualisierung in der Programmversion 2.1.0.0**

* Um Assets hochzuladen, können Benutzer die Dateien oder Ordner jetzt direkt aus dem Windows Explorer oder Mac Finder in die Benutzeroberfläche des Programms ziehen. Dieser Prozess funktioniert zusätzlich zur Upload-Option, die in der Anwendung verfügbar ist. Siehe [Upload von Assets](/help/using/using.md#upload-and-add-new-assets-to-aem) <!-- CQ-4309527 -->

**Aktualisierung in der Programmversion 2.0.3**

Folgender Fehler wurde in der aktuellen Version behoben:

* Das Anmeldeproblem für Programmbenutzer unter Windows, die versuchen, auf das DAM-Repository unter [!DNL Adobe Experience Manager] 6.5.5.0 zuzugreifen, wurde behoben.

**Aktualisierungen in der Programmversion 2.0.2**

Die folgenden Fehlerbehebungen und Aktualisierungen sind verfügbar:

* Die Upload-Beschleunigung ist jetzt verfügbar, um die Upload-Leistung zu steigern. Wenn diese Einstellung aktiviert ist, verwendet das Programm mehr lokale CPU-Threads und ist ressourcenintensiver, um schnellere Uploads durchzuführen.

* Das Hochladen von Assets funktioniert jetzt, wenn Dateinamen oder Pfade bestimmte GB18030-Zeichen enthalten. <!-- CQ-4283494 -->

* Die Option „Nach Relevanz sortieren“ ist verfügbar, nachdem in den Suchergebnissen zu einem anderen Sortiertyp gewechselt wurde. <!-- CQ-4286874 -->

* Das Desktop-Programm listet jetzt Unterordner auf, ohne dass eine explizite Aktualisierung erforderlich ist. <!-- CQ-4285711 -->

* (Windows) Ein seltener Fehler mit einer nicht verwendbaren Programm-Oberfläche auf einigen Windows-Computern wurde behoben. Benutzer können nicht auf die App-Oberfläche klicken, da sie verzerrt angezeigt wird und der Klickbereich der Oberflächenelemente seitlich &quot;verschoben&quot;ist. <!-- CQ-4280785 -->

**Aktualisierungen in der Programmversion 2.0.1**

Die folgenden Fehlerbehebungen und Aktualisierungen sind verfügbar:

* Option zum Konfigurieren des Verzeichnisses `%Temp%` entsprechend dem Pfad `%APPDATA%`. <!-- CQ-4282665 -->

* Benutzer können sich über die Okta-SAML-Authentifizierung bei der [!DNL Experience Manager]-Autoreninstanz anmelden. <!-- CQ-4278134 -->

## Installationsanweisungen {#installation-instructions-v2}

Informationen zum Installieren und Konfigurieren des Programms finden Sie unter [Installieren des [!DNL Experience Manager] -Desktop-Programms](install-upgrade.md).

Wenn Sie von einer vorherigen Version des [!DNL Experience Manager]-Desktop-Programms aktualisieren, müssen Sie die folgenden Best Practices für die Umstellung befolgen, die unter [Upgrade von der vorherigen Version](install-upgrade.md#upgrade-from-previous-version) aufgeführt sind.

## Wichtige Hinweise zur Funktionsweise des Programms {#how-app-works}

Es ist wichtig, die folgenden Informationen zum Programm und dessen Funktionsweise zu verstehen.

* Das Programm bietet vollständige Kontrolle über Vorgänge, bei denen Asset-Binärdateien vollständig von und nach [!DNL Experience Manager] übertragen werden müssen (**Öffnen**, **Bearbeiten**, **Änderungen hochladen** und **Hochladen von Assets**).

   * Wenn Sie mit dem Asset auf dem Desktop arbeiten möchten, müssen Sie es explizit auf Ihrem Desktop öffnen, bearbeiten oder herunterladen, entweder einzeln, in einem Ordner oder über eine Mehrfachauswahl.

   * Wenn Sie möchten, dass lokale Änderungen an Assets nach [!DNL Experience Manager] hochgeladen werden, müssen Sie [!UICONTROL Upload Changes] entweder einzeln oder über eine Mehrfachauswahl auswählen.

   * Das Programm ist kein Synchronisierungs-Client, der Assets auf dem Desktop und in [!DNL Experience Manager] synchronisiert.

   * Das Programm stellt keine Netzwerkfreigabe bereit, die das [!DNL Experience Manager]-Repository als eine virtuelle Ordnerstruktur zuordnet.

* Die Liste der vom Programm angezeigten Assets basiert auf dem Status des Assets-Repositorys. Dateien, die lokal heruntergeladen und anschließend in die lokalen Dateien oder den Cache-Ordner umbenannt wurden, werden nicht mit der Anwendung angezeigt oder verwaltet.

* Wenn das Programm nicht die erwarteten Ergebnisse anzeigt, klicken Sie auf das Aktualisierungssymbol in der oberen Leiste.

* Die lokale Netzwerkfreigabe, bei Verwendung der Aktion [!UICONTROL Reveal File]. Sie zeigt nur Dateien (und Ordner) an, die lokal verfügbar sind. [!UICONTROL Reveal File] und [!UICONTROL Reveal Folder] lädt Assets vorab herunter, damit die richtigen Assets in der lokalen Netzwerkfreigabe angezeigt werden.

* Die lokale Netzwerkfreigabe SMB (Mac)/WebDAV (Win) wird verwendet, wenn eine Adobe Creative Cloud-App die Asset-Dateien liest, die verknüpft sind/in einer nativen Datei des Creative Cloud-Programms platziert wurden.

Das folgende Diagramm zeigt den Fluss von Assets und Dateien von der Cloud zum lokalen Dateisystem und umgekehrt, der durch Benutzeraktionen initiiert wird.

![Fluss von Assets vom [!DNL Experience Manager]-Server zu nativen Desktop-Programmen über das Desktop-Programm](assets/da20_flow_diagram.png)

## Bekannte Probleme {#known-issues-v2}

**Probleme mit der Benutzeroberfläche:**

* Manchmal ist die Oberfläche des Desktop-Programms plötzlich leer. Klicken Sie mit der rechten Maustaste und klicken Sie auf [!UICONTROL Refresh], um das Programm erneut zu laden. Nach einer solchen Aktualisierung beginnen Sie im Stammverzeichnis des DAM-Repositorys. Aktualisierungen oder Status Ihrer Assets werden beibehalten. <!-- CQ-4270267 -->

* Schwierigkeiten beim Navigieren in Ordnern/Suchergebnissen ohne Trackpad oder Mauszeiger. Die Bildlaufleiste wird bei ruderlosen Mausgeräten nicht angezeigt. <!-- CQ-4269947 -->

* In seltenen Fällen wird die Fortschrittsleiste nicht korrekt angezeigt, wenn sich das hochgeladene Asset ändert.

* Nach dem Anwenden und Entfernen des Filters, um alle lokal bearbeiteten Assets zu finden, wechselt das Programm nicht zu den Suchergebnissen oder der Ordneransicht, mit denen die Benutzer begonnen haben. Das Programm zeigt den Stammordner des DAM-Repositorys an.

* Wenn Sie eine Verbindung zu einer URL herstellen, für die kein [!DNL Experience Manager] -Server ausgeführt wird, reagiert der Bildschirm &quot;Verbindung&quot;manchmal nicht mehr. Beenden Sie das Programm und starten Sie es erneut.

**CRUD-Probleme (Erstellen, Lesen, Aktualisieren und Löschen):**

* Beim Hochladen von Änderungen an einem Asset mit Kommentaren werden die Kommentare mit dem Asset in [!DNL Experience Manager] gespeichert, sind jedoch nicht als Versionskommentare sichtbar. Dieses Problem wurde in [!DNL Experience Manager] 6.4.5. und [!DNL Experience Manager] 6.5.1. behoben. Adobe empfiehlt dringend, die neuesten Service Packs zu installieren. <!-- CQ-4268990 -->

* Ein Benutzer kann Asset-Übertragungen nicht abbrechen. Wenn Sie eine unbeabsichtigte große Übertragung ausgelöst haben, beenden Sie das Programm und starten Sie es erneut. <!-- CQ-4278940 -->

**Plattformfragen:**

* Unter Windows ändert sich der Status eines Assets unter Umständen sofort nach dem Öffnen in [!UICONTROL Edited Locally], auch wenn Sie es möglicherweise nicht bearbeitet haben. Klicken Sie zur Aktualisierung auf [!UICONTROL Refresh].

>[!MORELIKETHIS]
>
>* [[!DNL Experience Manager] as a [!DNL Cloud Service] documentation](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service)
>* [[!DNL Experience Manager]  as a [!DNL Cloud Service] [!DNL Assets] documentation](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/overview)
>* [Verwenden des [!DNL Experience Manager] -Desktop-Programms](using.md)
>* [Installieren und Aktualisieren des Desktop-Programms](install-upgrade.md)
>* [Best Practices und Tipps zur Fehlerbehebung](troubleshoot.md)
