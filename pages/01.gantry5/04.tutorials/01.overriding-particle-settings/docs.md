---
title: Überschreiben der Partikeleinstellungen
taxonomy:
    category: docs
    tag: [gantry5]
---

**Partikel** sind extrem flexibel. Sie können über mehrere Ebenen auf ihre Einstellungen zugreifen und ihre Standardeinstellungen für die gesamte Site, eine bestimmte Gliederung oder sogar eine Instanz im Layout-Manager oder Menü-Editor ändern.

Jeder Partikel wird mit einem eigenen Satz von Standardeinstellungen geliefert, die in der YAML-Datei des Partikels konfiguriert werden könnten. Diese Standardeinstellungen werden dann von der Basis-Outline im Panel Partikel-Vorgaben vererbt. Von dort aus können Sie diese Standardwerte innerhalb der Basis-Outline, der Sub-Outline und sogar in der spezifischen Partikelinstanz, wie sie im Layout-Manager, Menü-Editor, Modul oder Widget erscheint, ändern.

Hier ist eine kurze Übersicht über die verschiedenen Vererbungsebenen eines **Partikels**.

| Level                      | Beschreibung           |
| :-----                     | :-----                 |
| Partikel-YAML-Datei                 | Alle in dieser Datei zugewiesenen Standardwerte gelten als absolute Standardwerte der obersten Ebene für das Partikel. Diese Vorgaben werden durch alle vorgenommenen Änderungen in der Basis-Outline und Sub-Outlines überschrieben. |  
| Basis-Outline Partikel-Vorgaben     | Änderungen, die im Panel **Partikel-Standards** in der Basis-Outline vorgenommen werden, werden zu globalen Standard-Werten für die Site.  
| Non-Basis-Outline-Partikelvorgaben       |Das Panel **Partikel-Standards** auf dieser Ebene legt Standardwerte für den Partikel fest, wie er in dieser bestimmten Outline vorkommt, wobei nur diese Outline betroffen ist.  |
| Vorgaben für einzelne Partikel im Layout-Manager, Menü-Editor, Modul oder Widget | Änderungen, die auf dieser Ebene vorgenommen werden, sind die überschriebenen Werte für den Partikel, die nur in diesem Fall oder in direkt vererbten Objekten gelten.    |

Kurz gesagt, die Vererbung für Partikel-Einstellungen läuft wie folgt ab: **Partikel YAML-Datei > Basis-Outline Partikel-Vorgaben > Non-Basis-Outline Partikel-Vorgaben > Individuelle Instanz**. Jeder Schritt erbt und/oder überschreibt die Einstellungen vom vorherigen Schritt.

## Basis-Outline Panel für Partikel-Voreinstellungen

![Default](particle_1.jpg?classes=shadow,border)

Innerhalb der **Basis**-Outline können Sie globale Standard-Einstellungen für jeden Partikel im administrativen Panel **Partikel-Standards** festlegen. Die hier vorgenommenen Einstellungen werden zu den globalen Standardeinstellungen, die für jede Outline und jede einzelne Partikel-Instanz gelten, sofern sie nicht überschrieben werden. Hier setzen Sie die am häufigsten verwendeten Einstellungen für einen bestimmten Partikel.

Wenn Sie beispielsweise für Ihren Logo-Partikel auf allen Seiten, außer einer oder zwei Seiten, dasselbe Quellbild verwenden möchten, legen Sie dieses Bild hier fest und überschreiben es entweder mit den Non-Basis-Outline-Einstellungen, die auf diese Ausnahmeseiten angewendet werden oder in den einzelnen Partikel-Instanzen im Layout-Manager.

## Non-Basis-Outline Panel für Partikel-Voreinstellungen

![Non-Default](particle_2.jpg?classes=shadow,border)

Innerhalb von Outlines, die **nicht** als Standard festgelegt sind, sind im Administrationspanel **Partikel-Standards** die meisten (wenn nicht alle) Ihrer Partikel ausgegraut. Ändern Sie eine Einstellung und/oder aktivieren Sie das Kontrollkästchen auf der rechten Seite des Einstellungsfeldes für diesen Artikel, so können Sie die Standardeinstellungen für diese Outline überschreiben.

Jetzt erhält jeder Partikel, der im Layout-Manager für diese bestimmte Outline positioniert wird, standardmäßig diese neuen Einstellungen.

## Individuelle Partikel-Einstellungen im Layout-Manager

![](particle_4.jpg?classes=shadow,border)

Wenn Sie einen Partikel im **Layout-Manager** einer Outline platzieren, erzeugen Sie eine **Instanz**. Diese Instanz ermöglicht es Ihnen, die Partikel-Einstellungen für diesen speziellen Partikel anzupassen, wobei _keine anderen Instanzen_ dieses Partikels betroffen sind. Wenn Sie z.B. das Logo in einer Instanz anders aussehen lassen wollten, würden Sie die Einstellungen hier ändern.

![](particle_3.jpg?classes=shadow,border)

Im Beispiel oben haben wir das **Startjahr** für den Partikel geändert, indem wir dessen Einstellungsfeld im **Layout-Manager** verwendet haben. Das angekreuzte Kästchen rechts neben dem Feld zeigt an, dass es überschrieben wird, während die anderen Felder grau und nicht angekreuzt bleiben. Diese Einstellungen werden von höheren Standard-Ebenen geerbt.

Sie können auf diese instanzspezifischen Einstellungen zugreifen, indem Sie auf das Zahnrad, rechts neben dem Partikel, im Layout-Manager klicken.

## Überschreiben der Partikel Quell-Dateien

Manchmal erfordern die Änderungen, die Sie an einem Partikel vornehmen möchten, eine Änderung der Quelldateien. Der Quellcode für alle Partikel besteht aus **Twig**- und **YAML**-Dateien.

In diesem Beispiel fügen wir einen Link zum Partikel **Copyright** hinzu, der vom Inhaber des Copyrights direkt auf dessen Homepage führt. Das ist nur ein kleines Beispiel dafür, was Sie ändern können.

![Source Override](source_1.png?classes=shadow,border)

In der Abbildung oben sehen Sie den **Copyright** Partikel auf der linken Seite. Es gibt keine Links oder irgendetwas, das im Core-Partikel enthalten ist. Wenn Sie den Namen des Copyright-Inhabers als Link zu dessen Website verwenden möchten, können Sie ein paar einfache Änderungen an den Quelldateien des Partikels vornehmen.

[ui-tabs position="top-left" active="0"]
[ui-tab title="Joomla"]

Zuerst sollten Sie die Dateien `copyright.html.twig` und `copyright.yaml` kopieren. Sie befinden sich in `ROOT/media/gantry5/engines/nucleus/particles/`. Fügen Sie die Kopien in `TEMPLATE_DIR/custom/particles` ein. Falls das Verzeichnis `particles` nicht bereits in Ihrem Verzeichnis `custom` existiert, müssen Sie es erstellen.

! Der gesuchte Partikel könnte sich an einem anderen Ort befinden. Zum Beispiel kann ein Template-spezifischer Partikel, der mit dem Template geliefert wurde und nicht zum Kern von Gantry gehört, in `/THEME_DIR/particles` zu finden sein.

Durch das Duplizieren der Dateien und das Ablegen der Kopien im Ordner „custom“ machen Sie Ihre Änderungen update-sicher. Dadurch wird verhindert, dass Ihre Änderungen beim Updaten des Gantry-Frameworks oder des Themes verloren gehen.

Alles, was Sie mit den kopierten Partikel-Dateien in Ihrem Ordner `TEMPLATE_DIR/custom/particles` anstellen, übersteuert das, was in der Originaldatei steht.

[/ui-tab]
[ui-tab title="WordPress"]

Zuerst sollten Sie die Dateien `copyright.html.twig` und `copyright.yaml` kopieren. Sie befinden sich in `ROOT/wp-content/plugins/gantry5/engines/nucleus/particles/`. Fügen Sie die Kopien in `THEME_DIR/custom/particles` ein. Falls das Verzeichnis `particles` nicht bereits in Ihrem Verzeichnis `custom` existiert, müssen Sie es erstellen.

! Der gesuchte Partikel könnte sich an einem anderen Ort befinden. Zum Beispiel kann ein Template-spezifischer Partikel, der mit dem Template geliefert wurde und nicht zum Kern von Gantry gehört, in `/THEME_DIR/particles` zu finden sein.

Durch das Duplizieren der Dateien und das Ablegen der Kopien im Ordner „custom“ machen Sie Ihre Änderungen update-sicher. Dadurch wird verhindert, dass Ihre Änderungen beim Updaten des Gantry-Frameworks oder des Themes verloren gehen.

Alles, was Sie mit den kopierten Partikel-Dateien in Ihrem Ordner `THEME_DIR/custom/particles` anstellen, übersteuert das, was in der Originaldatei steht.

[/ui-tab]
[ui-tab title="Grav"]

Zuerst sollten Sie die Dateien `copyright.html.twig` und `copyright.yaml` kopieren. Sie befinden sich in `ROOT/user/plugins/gantry5/engines/nucleus/particles/`. Fügen Sie die Kopien in `ROOT/user/data/gantry5/themes/THEME_NAME/particles/` ein. Falls das Verzeichnis `particles` in diesem Pfad noch nicht existiert, müssen Sie es erstellen.

! Der gesuchte Partikel könnte sich an einem anderen Ort befinden. Zum Beispiel kann ein Template-spezifischer Partikel, der mit dem Template geliefert wurde und nicht zum Kern von Gantry gehört, in `/user/themes/THEME_NAME/particles/` zu finden sein.

Durch das Duplizieren der Dateien und das Ablegen der Kopien im Ordner „custom“ machen Sie Ihre Änderungen update-sicher. Dadurch wird verhindert, dass Ihre Änderungen beim Updaten des Gantry-Frameworks oder des Themes verloren gehen.

Alles, was Sie mit den kopierten Partikel-Dateien in Ihrem Ordner `ROOT/user/data/gantry5/themes/THEME_NAME/particles/` anstellen, übersteuert das, was in der Originaldatei steht.

[/ui-tab]
[/ui-tabs]

Weil wir dem Partikel **Copyright** ein neues Feld hinzufügen, müssen wir die YAML-Datei bearbeiten. Hier sehen Sie, wie die YAML-Datei `copyright.yaml` vor den Änderungen aussieht.

```yaml
name: Copyright
description: Display copyright information.
type: particle

form:
  fields:
    enabled:
      type: input.checkbox
      label: Enabled
      description: Globally enable the particle.
      default: true

    date.start:
      type: input.text
      label: Start Year
      description: Select the copyright start year.
      default: now

    date.end:
      type: input.text
      label: End Year
      description: Select the copyright end year.
      default: now

    owner:
      type: input.text
      label: Copyright owner
      description: Add copyright owner name.
```

![Particle Override](source_3.png?classes=shadow,border)

Dadurch werden die Felder erstellt, die im Panel **Partikel-Vorgaben** des Gantry-Administrators sowie in allen Instanzen im **Layout-Manager** erscheinen, in denen der Partikel **Copyright** positioniert wurde. Diese Einstellungen werden dann mit der **Twig**-Datei des Partikels verknüpft. In diesem Fall fügen wir ein Link-Feld hinzu, so dass der Anwender einen Link zu dem Partikel erstellen kann.

Das Link-Feld können wir erstellen, indem wir am Ende der YAML-Datei Folgendes hinzufügen:

```yaml
    site:
      type: input.url
      label: Copyright Link
      description: Add the link to the copyright owner's site.
```

![Particle Override](source_2.png?classes=shadow,border)

Sie werden feststellen, dass das neue Feld auf dem Backend erscheint.

Die Datei `copyright.html.twig` muss ebenfalls geändert werden, um die neuen Daten aufzunehmen und die Verbindung herzustellen. Unten sehen Sie den Inhalt der ursprünglichen Twig-Datei:

```twig
{% extends '@nucleus/partials/particle.html.twig' %}

{% set start_date = particle.date.start|trim in ['now', ''] ? 'now'|date('Y') : particle.date.start|e %}
{% set end_date = particle.date.end|trim in ['now', ''] ? 'now'|date('Y') : particle.date.end|e %}

{% block particle %}
Copyright &copy;
{% if (start_date != end_date) %}{{ start_date|e }} - {% endif %}
{{ end_date|e }}
{{ particle.owner|e }}
{% endblock %}
```

Die Zeile `{{{ particle.owner|e }}}` muss geändert werden, um den Link einzufügen, der auf der Variablen basiert, die über die YAML-Datei zugewiesen wurde. In diesem Beispiel werden wir sie durch diese drei Zeilen ersetzen:

```twig
{% if particle.site %}<a href="{{ particle.site | default(gantry_base) }}">{% endif %}
{{ particle.owner }}
{% if particle.site %}</a>{% endif %}
```


![Particle Override](source_4.png?classes=shadow,border)

Nun erscheint auf dem Frontend der Website der Partikel mit einem Link zu dem Namen des Copyright-Inhabers. Das ist nur ein kleines Beispiel dafür, was Sie tun können, um die Möglichkeiten eines Partikels mit Twig und YAML zu erweitern.
