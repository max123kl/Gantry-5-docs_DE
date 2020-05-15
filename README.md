[![Join the chat at https://gitter.im/gantry/gantry5](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/gantry/gantry5?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

# Deutsche Gantry Dokumentation

Das Repository enthält den Quellcode der [deutschen Gantry-Dokumentation](https://github.com/max123kl/Gantry-5-docs_DE), die auf [http://XXXX](http://VVVVV) zu finden ist.

Die Dokumentation ist im Ordner `pages/` enthalten und in Unterverzeichnissen (pro Kapitel) gegliedert, genau wie Sie sie auf der Hauptwebsite sehen. Das gesamte Repo, das Sie hier finden, ist als `user/` Verzeichnis in einer [Grav](http://getgrav.org) Installation gedacht. Dieses Repo enthält die Themes, Konfigurationsdateien und Einstellungen, die es möglich machen die Dokumentation in der gleichen Optik zu präsentieren wie sie auf der [Dokumentationswebsite](http://docs.gantry.org) erfolgt.

Sie können die gesamte Dokumentation dort lesen (da es sich nur um einfache Textdateien handelt), die mit [Markdown](http://daringfireball.net/projects/markdown/) formatiert sind.

Um eine lokale Kopie zu erstellen und Arbeitsblätter zu laden, empfehlen wir Ihnen, die  [Grav-Dokumentation](http://learn.getgrav.org/) zu lesen, da Sie dort die Informationen finden, die Sie zum Verständnis der Struktur und Syntax der Dokumentationsdatei benötigen.

Wenn Sie eine lokale Kopie der Dokumentation wünschen, können Sie diese entweder [herunterladen](https://github.com/gantry/docs/archive/master.zip) oder Sie können das Repository klonen, indem Sie den folgenden Befehl ausführen:

~~~ .bash
git clone git://github.com/max123kl/Gantry-5-docs_DE gantry-docs_DE
~~~


Mitwirkung
----------
Die Beteiligung an der Erstellung der Dokumentation/Übersetzung ist sehr einfach. Sie können gerne einen Fork des Repositorys anlegen, Ihre Änderungen einfügen und durch einen Pull-Request zurücksenden. Sie können die Dokumente sogar direkt auf GitHub bearbeiten, ohne die Dateien jemals herunterladen zu müssen. Beachten Sie die entsprechenden Konventionen, bevor Sie eine Pull-Anfrage stellen.

Sie sind auch herzlich eingeladen, Vorschläge zu machen oder ein Problem mit der Dokumentation zu melden, indem Sie einen neuen [Issue](https://github.com/max123kl/Gantry-5-docs_DE/issues/new) hier starten.

Wenn Sie sich für einen Fork zur Einreichung neuer Inhalte als Commits entscheiden. Bitte stellen Sie bitte sicher, dass Sie einen Branch für Ihre Änderungen erstellen, bevor Sie diese vornehmen. Dadurch wird der Prozess der Integration erleichtert. Jede Änderung muss zuerst den Branch `develop` durchlaufen, daher stellen Sie bitte sicher, dass Ihre Pull-Requests an den richtigen Branch gerichtet sind.

Um mit einer lokalen Installation in den richtigen `develop` Branch zu verzweigen, können Sie diese Befehle ausführen:

~~~ .bash
git clone git://github.com/gantry/docs gantry-docs
cd gantry-docs
git checkout -b develop origin/develop
~~~


Konventionen
------------

Hier ist eine Liste der wichtigsten Konventionen, an die wir uns beim Verfassen der Dokumentation halten, um das Repository gut organisiert und konsistent zu halten. Sie können gerne jede andere Datei in den Dokumentationen als Referenz verwenden.

* Jede Änderung oder Pull-Request muss auf den Branch [develop](https://github.com/gantry/docs/tree/develop) angewendet oder gerichtet werden. Sobald er geprüft, genehmigt und gepullt wurde, wird er in den **master** Branch eingegliedert und automatisch von der Website übernommen.

* Ordner- und Dateinamen müssen in lisp-case ( mit Bindestrich verkettet) und immer in Kleinbuchstaben geschrieben werden. Wenn Sie z.B. „How to Install“ in lisp-case konvertieren wollten, würden Sie es „how-to-install“ nennen.

* Vor jeder Haupt-Überschrift, mit Ausnahme des Titels, müssen 2 Leerzeilen stehen, und nach einer Überschrift darf keine Leerzeile folgen.

* Unterzeilen von Überschriften (`=` und `-`) müssen immer auf den Text der Titelzeile ausgerichtet sein. Da dies leicht verwirrend sein kann, sollten Sie unbedingt eine monospaced Schriftart verwenden. Hier ein paar Beispiele für gut ausgerichtete Überschriften:

    ~~~
    Header H1
    =========

    Header H2
    ---------
    ~~~


YAML Header
-----------

Unsere Markdown-Implementierung verwendet spezielle [YAML-Header](http://www.yaml.org/spec/1.2/spec.html). Diese Kopfzeilen werden zwischen einem Set von drei Minus-Strichen und einer Leerzeile eingeschlossen. So sieht ein YAML-Header aus:

```yaml
---
title: Getting Started
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
```

Die Kopfzeilen ermöglichen eine sehr flexible Ausgabe. Beispielsweise können wir einen Titel einer Markdown-Datei auf der Grundlage ihrer Header-Titel-Variablen und nicht des Dateinamens selbst definieren.

Nachfolgend finden Sie eine Liste der unterstützten `YAML` Variablen, die verwendet werden können und eine Beschreibung, was sie bewirken:

* **title**: Der Titel des Artikels. Dieser wird immer dann verwendet, wenn eine Seite referenziert werden muss. Wenn der Titel auf eine `TOC` Datei (Inhaltsverzeichnis) gesetzt wird, globalisiert er den Titel für jedes Dokument im Projekt selbst.

    ```yaml
    ---
    title: Hello World!

    ---
    ```

* **taxonomy**: legt die Art des Artikels und seine Tags fest. Standardmäßig sollte jede Dokumentationsdatei die Einstellungen `category: docs` und `tag: [gantry(version)]` enthalten.

  Die Darstellung unterstützt die Markdown-Inline-Syntax, wie z.B. _strong_ (fett), _italic_ (kursiv), _links_ (Verweis). Sie sollten nichts anderes verwenden (d.h.  _headers_ (Kopfzeilen), _images_ (Bilder) und dergleichen).

    ```yaml
    ---
    taxonomy:
        category: docs
        tag: [gantry5]

    ---
    ```


* **gravui**: Diese Einstellungen geben Ihnen die Möglichkeit, bestimmte **gravui** Muster zu laden.

   Die zulässigen `gravui` Einstellungen sind nachfolgend aufgelistet:
   * **enabled**: Legt fest, ob gravui bei der Seitendarstellung überhaupt verwendet wird oder nicht. Am wahrscheinlichsten ist es, wenn diese Funktion `enabled: true` (aktiviert) ist.
   * **tabs**: Wenn diese Option auf `true` gesetzt ist, ermöglicht sie die Verwendung von Tabulatoren zur Unterscheidung zwischen Befehlen, die exklusiv für das eine oder andere CMS gelten. Standardmäßig ist diese Einstellung auf `false` (deaktiviert) gesetzt, wenn die Zeile nicht vorhanden ist.
   * **callouts**: Wenn diese Option auf `true` gesetzt ist, können visuelle Aufrufe über einem Bild platziert werden. Das ist ein nützliches Werkzeug, wenn Sie im Bild auf etwas hinweisen und einen Tooltip bieten möchten, der erscheint, wenn Sie mit dem Mauszeiger darüber fahren.

* **process**: Prozess-Tags geben Ihnen die Möglichkeit, Dinge zu tun, wie z.B. das Twig-Skript innerhalb der Markdown-Datei einzufügen und es ausführen zu lassen. Das ist praktisch, wenn Sie beispielsweise Bilder mit Klassen versehen, um ihnen ein besseres Aussehen zu verleihen. z.B. wendet `{.border .shadow}` nach einem Markdown-Bild die `border` und `shadow` Klassen an, was Ihrem Bild ein eleganteres Aussehen verleiht.

    Hier sehen Sie ein vollständiges Beispiel für eine Zeile in der Dokumentation mit Twig:

    ```markdown
    ![Administrator](../../configure/gantry-admin/admin_access_1.png) {.border .shadow}
    ```

Wenn Sie Fragen haben, können Sie gerne ein [Issue](https://github.com/gantry/docs/issues/new) starten.

_Ihr RocketTheme Team_
