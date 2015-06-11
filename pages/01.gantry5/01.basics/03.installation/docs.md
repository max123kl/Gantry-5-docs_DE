---
title: Installation
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

Das Gantry Framework selbst ist unabhängig von einem Template. Jedes Gantry-fähige Template stützt sich auf das Framework. Die zugrunde liegende Basis und umfangreiche Funktionalität ermöglicht die Realisation von solch leistungsstarken Web-Sites. Ein mit Gantry erzeugtes Template erfordert das Framework um richtig zu funktionieren. Gantry ist nicht notwendigerweise im Template selbst eingebaut.

Gantry Download
------------------

Für Gantry 5 sind jeweils drei Download-Optionen verfügbar:

{% set tab1 %}

* **Bundle**: Dies beinhaltet das Framework (Bibliothek, Komponente & Plugins), das Hydrogen-Template und die zugehörigen Erweiterungen.
* **Framework**: Dies enthält nur das Framework (Bibliothek, Komponente & Plugins).
* **Template**: Dies enthält nur das Hydrogen-Template.

Der Installationsvorgang ist exakt der gleiche für alle drei Varianten. Der einzige Unterschied ist die Datei, welche Sie installieren. Wählen Sie die für Sie beste Download-Option. Wir empfehlen das Bundle für die erstmalige Installation.

<div align="center"><a href="http://gantry.org/downloads" class="button"><i class="fa fa-fw fa-download"></i> Download: Gantry 5 und das Hydrogen-Template</a></div>

>>> Vor der ersten vollständigen Freigabe von Gantry 5 werden **Framework** und **Template** in getrennten Installations-Paketen angeboten. Ein Bundle-Paket ist geplant, wird wahrscheinlich aber erst nach dem Beta-Start zur Verfügung stehen.

{% endset %}
{% set tab2 %}

>>> Die WordPress Version erscheint demnächst.

* __Framework__: Dies enthält nur das Framework-Plugin.
* __Theme__: Dies enthält nur das Gantry-Theme.
* __RocketLauncher__: Dies beinhaltet eine komplette WordPress-Installation, das Framework-Plugin und das vorkonfigurierte Gantry-Theme (nur für neue Instal­la­tio­nen empfohlen).

Das Paket, das Sie zur Installation auswählen wird auf unterschiedliche Weise behandelt, was den Speicherort der Dateien betrifft. Gantry Framework für Wordpress sollte wie ein normales Wordpress-Plugin installiert werden. Das Gantry Default Theme für Wordpress sollte auf die gleiche Weise wie alle anderen Themes installiert werden. 

>>>>> Denken Sie daran , dass das Gantry Framework für alle Gantry-Themes auf Ihrem Computer installiert sein muss.

IWenn Sie auf Ihrem Server Wordpress noch nicht installiert haben, können Sie das **RocketLauncher** Paket benutzen. Es enthält eine vollständige vorkonfigurierte Gantry-Umgebung und ist im Wesentlichen eine vollständige WordPress-Installation. Wählen Sie die für Sie beste Download-Option. Wir empfehlen **RocketLauncher** für erstmalige Wordpress-Installationen.

<a href="http://www.gantry-framework.org/download#wordpress" class="button"><i class="fa fa-fw fa-download"></i> Download</a>

{% endset %}
{{ gravui_tabs({'Joomla':tab1, 'WordPress':tab2}) }}

## Installing the Gantry Framework

{% set tab1 %}

[plugin:youtube](https://www.youtube.com/watch?v=zCH10qrxPSc)

Installieren Sie das **Gantry Framework-Paket** (die Datei ist ähnlich benannt wie `pkg_gantry5-v5.0.0.zip`), indem Sie im Joomla Back-End zu **Erweiterungen → Erweiterungen → Installieren** gehen. Mit **Durchsuchen** wählen Sie die heruntergeladene ZIP-Datei aus. Danach klicken Sie auf **Hochladen & Installieren**, um die Installation zu starten.

![Installation](install-template_joomla.jpeg) {.border .shadow}

Nach der Installation des Gantry Framework-Pakets, werden alle Gantry-Erweiterungen im **Extension-Manager** angezeigt.

![Extensions](gantry_extensions.png) {.border .shadow}

Wenn Sie irgendwelche Probleme haben, einschließlich der folgenden Fehlermeldungen:

* `Failed to load 'g5_hydrogen' template: Please install Gantry5 Framework!` 
* `Error - Please install Gantry5 Framework!`
* `Error - Gantry5 Templates: Please enable 'System - Gantry5 Framework' plugin!`

... dann sollten Sie sicherstellen, dass alle Gantry zugehörigen Erweiterungen aktiviert sind. Um dies zu tun, wählen Sie einfach alle im Bild oben aufgeführten, nicht aktiviert Erweiterungen aus und aktivieren Sie diese, indem Sie die Schaltfläche **Aktivieren** im oberen linken Bereich des **Erweiterungs-Managers**.

{% endset %}
{% set tab2 %}

>>> Die WordPress Version erscheint demnächst.

Um das Gantry-Plugin zu installieren navigieren Sie zu **Plugins → Installieren** im Admin-Bereich von Wordpress. Von hier aus, wählen Sie die Schaltfläche **Durchsuchen** und markiern Sie die heruntergeladene ZIP-Datei. Dann klicken Sie auf **Installieren**, um die Installation zu starten.

![](install-upload_wp.jpg) {.border .shadow}

Das Gantry-Template wird in **Design → Themes** und das Gantry-Plugin in **Plugins** erscheinen.

{% endset %}
{{ gravui_tabs({'Joomla':tab1, 'WordPress':tab2}) }}

## Installieren eines Gantry Templates

{% set tab1 %}

Installieren Sie über **Erweiterungen → Erweiterungen → Installieren → Paketdatei hochladen**. Wählen Sie mit dem **Durchsuchen**-Button die heruntergeladene ZIP-Datei aus und klicken Sie auf **Hochladen & Installieren**, um die Installation zu starten.

![Installation](install-template_joomla.jpeg) {.border .shadow}

Das Gantry-Template wird im **Template-Manager** angezeigt, alle zugehörigen Gantry-Er­wei­te­rungen werden im **Extensions-Manager** angezeigt.

{% endset %}
{% set tab2 %}

... erscheint demnächst!

{% endset %}
{{ gravui_tabs({'Joomla':tab1, 'WordPress':tab2}) }}

## Ein Gantry Template als Standard festlegen

{% set tab1 %}

Wenn Sie das Gantry-Template verwenden, werden Sie es als Standardvorlage festlegen wollen, damit es im Front-End geladen wird. Gehen Sie zu **Erweiterungen → Template-Manager**, wählen Sie das Kontrollkästchen, Gantry, und klicken Sie auf **Standard** in der Schaltfläche in der Symbolleiste.

![](gantry_default.png) {.border .shadow}

{% endset %}
{% set tab2 %}

... erscheint demnächst!

{% endset %}
{{ gravui_tabs({'Joomla':tab1, 'WordPress':tab2}) }}
