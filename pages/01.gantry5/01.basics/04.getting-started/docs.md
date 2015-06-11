---
title: Erste Schritte
taxonomy:
    category: docs
    tag: [gantry5]
gravui:
    enabled: true
    tabs: true
    callouts: true
process:
    twig: true
---

Bereit, um mit Gantry 5 loszulegen? Großartig! Wir sind hier um zu helfen.

Auf dieser Seite finden Sie ein paar einführende Tipps, die Ihnen helfen, Gantry 5 Grundlagen kennen zu lernen. Die mehr detailliertere Dokumentation für jeden dieser Tipps erhalten Sie durch Klicken auf die Schaltfläche **Weitere Infos** am Ende jedes Abschnitts. 

Wir hoffen, dass Sie so viel Spaß mit jedem Bit von Gantry 5 haben werden, wie wir es während der Entwicklung hatten.

## Installieren von Gantry 5 und des Hydrogen-Templates

Gantry 5 ist ein Framework, mit dem Gantry-Themes erstellt werden. Um ein Gantry-Theme einsetzen zu können, muss sowohl das **Framework** als auch das **Theme** installiert sein. Das ist insgesamt eine einfache Sache.

Zuerst müssen Sie die neueste Version von Gantry 5 und das Hydrogen-Theme herunterladen indem Sie auf die Schaltfläche klicken, altenativ auch über [GitHub](http://github.com/gantry/gantry5).

<div align="center"><a href="http://gantry.org/downloads" class="button"><i class="fa fa-fw fa-download"></i> Download Gantry 5 und Hydrogen-Theme</a></div>

Sobald Sie die neusten Pakete haben, ist die Installation einfach. Eine Schritt-für-Schritt-Anleitung finden Sie im Abschnitt **Installation** dieser Dokumentation.

<a href="../basics/installation" class="button"><i class="fa fa-fw fa-graduation-cap"></i> Weitere Infos</a>

## Zugriff auf den Gantry-Administrator

{% set tab1 %}

![Administrator](../../configure/gantry-admin/admin_access_1.png) {.border .shadow}

Wenn Sie sowohl Framework als auch Hydrogen-Theme installiert und aktiviert haben, können Sie auf unterschiedliche Weise auf die Gantry 5 Administration zugreifen. Am einfachsten navigieren Sie zu **Komponenten → Gantry 5 Themes** aus dem Back-End von Joomla. 


{% endset %}
{% set tab2 %}

... erscheint demnächst!

{% endset %}
{{ gravui_tabs({'Joomla':tab1, 'WordPress':tab2}) }}

Hier finden Sie eine Liste mit allen installierten Gantry-Themes. Sie können ein Theme über **Preview** anschauen oder Sie wählen **Configure** um direkt zu dem **Gantry-Administrator** zu wechseln, wo man Änderungen an Ihrer Gantry-betriebenen Website vornehmen kann.

## Navigieren im Gantry 5 Administrator

Der Gantry-Administrator hat mehrere Verwaltungstools. Sie können damit Ihr Gantry-betriebenes Theme in Aussehen und Funktion konfigurieren. Hier folgt eine kurze Beschreibung von jedem dieser Werkzeuge, und was man mit ihnen machen kann.

{% set callout_items %}
Menu Editor [8%, 62%, se]
    : Dieses Verwaltungs-Panel erweitert die Möglichkeit des Menüsystems der Plattform. Sie können hier das Aussehen ändern und Menüpunkte ordnen bwz. neu einfügen, unabhängig vom integrierten Menü-Manager des CMS.

About (Pictured) [8%, 69%, se]
    : Diese Seite zeigt Ihnen einen schnellen Überblick zu dem aktuell angezeigten Theme einschließlich: Name, Versionsnummer, Ersteller, Support-Links, Funktionseigenschaften und vieles mehr.

Platform Settings [8%, 76%, se]
    : Mit dieser Taste gelangen Sie zur Einstellungsseite des CMS für Gantry 5. In Joomla, ist dies die Konfigurationsseite **Berechtigungen**.

Clear Cache [8%, 88%, se]
    : Diese Schaltfläche löscht die Cache-Dateien, die Gantry 5 betreffen. Dies schließt alle temporären Dateien außerhalb des CSS und Konfigurationsinformationen ein.

Outline Dropdown [17%, 2%, se]
    : Dieses Dropdown-Menü macht es einfach, schnell zwischen Outlines zu wechseln, ohne den Gantry-Administrator zu verlassen.

Styles [17%, 23%, se]
    : Das **Styles** Verwaltungs-Panel ermöglicht Ihnen Zugriff auf stilbezogene Ein­stellungen. Dazu gehören Dinge wie Theme-Farben, Schriftarten, Stil-Presets und mehr.

Settings [17%, 31%, se]
    : Dieses Verwaltungs-Panel bietet Ihnen die Möglichkeit, die Funktionseinstellungen des Themes zu konfigurieren. Dazu gehören die Einstellung von Standardwerten für Partikel sowie das Aktivieren/Deaktivieren einzelner Partikel.

Layout [17%, 39%, se]
    : Im **Layout** Verwaltungs-Panel konfigurieren  Sie das Layout für Ihr Theme. Das Erstellen von Modulpositionen, Partikeln, Abstandshaltern, und nicht-gerenderten Skripts, wie Google Analytics-Code, wird in diesem Fenster durchgeführt.

{% endset %}

{{ gravui_callout(page.media['getting_started_1.png'].url, callout_items, 'shadow border') }}

1. **Menu Editor**: Dieses Verwaltungs-Panel erweitert die Möglichkeit des Menüsystems der Plattform. Sie können hier das Aussehen ändern und Menüpunkte ordnen bwz. neu einfügen, unabhängig vom integrierten Menü-Manager des CMS.

2. **About (Pictured)**: Diese Seite zeigt Ihnen einen schnellen Überblick zu dem aktuell angezeigten Theme einschließlich: Name, Versionsnummer, Ersteller, Support-Links, Funktionseigenschaften und vieles mehr.

3. **Platform Settings**: Mit dieser Taste gelangen Sie zur Einstellungsseite des CMS für Gantry 5. In Joomla, ist dies die Konfigurationsseite **Berechtigungen**.

4. **Clear Cache**: Diese Schaltfläche löscht die Cache-Dateien, die Gantry 5 betreffen. Dies schließt alle temporären Dateien außerhalb des CSS und Konfigurationsinformationen ein.

5. **Outline Dropdown**: Dieses Dropdown-Menü macht es einfach, schnell zwischen Outlines zu wechseln, ohne den Gantry-Administrator zu verlassen.

6. **Styles**: Das **Styles** Verwaltungs-Panel ermöglicht Ihnen Zugriff auf stilbezogene Ein­stellungen. Dazu gehören Dinge wie Theme-Farben, Schriftarten, Stil-Presets und mehr.

7. **Settings**: Dieses Verwaltungs-Panel bietet Ihnen die Möglichkeit, die Funktionseinstellungen des Themes zu konfigurieren. Dazu gehören die Einstellung von Standardwerten für Partikel sowie das Aktivieren/Deaktivieren einzelner Partikel.

8. **Layout**: Im **Layout** Verwaltungs-Panel konfigurieren  Sie das Layout für Ihr Theme. Das Erstellen von Modulpositionen, Partikeln, Abstandshaltern, und nicht-gerenderten Skripts, wie Google Analytics-Code, wird in diesem Fenster durchgeführt.

<a href="../configure/gantry-admin" class="button"><i class="fa fa-fw fa-graduation-cap"></i> Weitere Infos</a>

## Was sind Outlines, Partikel, Atome, usw.?

Da Gantry 5 so verschieden von jeder früheren Version von Gantry ist, sind einige Begriffserklärungen nötig, die helfen Sinn zu verstehen die Beziehungen zwischen den neuen Gantry-Funktionen untereinander haben. Hier ist eine kurze Übersicht der häufigsten verwendeten Begriffe in Gantry 5.

| Begriff     | Definition                                                                                                                                             |
| :-----   | :-----                                                                                                                                                 |
| Outline  | Eine konfigurierbarer Stil, der in einem oder mehreren Bereichen Ihrer Site verwendet wtrd. Es dient als Container, in dem Styles, Einstellungen, Layout und Zuweisungen festgelegt werden.         |
| Partikel | Typischerweise ein kleiner Datenblock, der im Front-End eingesetzt wird. Es wirkt sich wie ein Widget/Modul aus, kann aber leicht im Gantry 5 Administrator konfiguriert werden. |
| Atom     | Eine spezielle Art von Partikel, der nicht-gerenderten Code, wie benutzerdefinierte Skripts (JS, CSS, usw.) oder Analyse Skripte für Traffic Tracking enthält.                |

<a href="../basics/terminology" class="button"><i class="fa fa-fw fa-graduation-cap"></i> Weitere Infos</a>

## Wo Sie Hilfe bekommen

A chat room has been set up using [Gitter](https://gitter.im/gantry/gantry5) where you can go to talk about the project with developers, contributors, and other members of the community. This is the best place to go to get quick tips and discuss features with others.

Eine [Documentation](http://docs.gantry.org) ist ebenfalls verfügbar und wird ständig je nach Entwicklungsfortschritt ergänzt. Fehlt Ihnen noch etwas? Sie können selbst zu der Dokumentation über GitHub beitragen.
