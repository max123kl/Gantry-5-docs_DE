---
title: Wie man ein Child-Theme (Grav) erstellt
taxonomy:
    category: docs
    tag: [gantry5]
---

Das Erstellen eines Child-Themes ist seit Gantry 5.4.18 einfach. Dazu dient ein einfacher CLI-Befehl, mit dem Sie schnell und einfach ein untergeordnetes Theme erstellen können, das Sie anpassen können, ohne sich Sorgen machen zu müssen, dass Änderungen, die während eines Updates vorgenommen werden, die Arbeit, die Sie in das Theme investiert haben, wieder zunichte machen.

## CLI-Befehl

Sie können ein Child-Theme in Grav mit dem leistungsstarken CLI-Toolset erstellen. Der Befehl `bin/plugin gantry5 child-theme` initiiert eine Reihe von Fragen, die nach ihrer Beantwortung ein Child-Theme für Sie erstellen, mit oder ohne Klonen bestehender Gliederung(en) und Konfigurationsoptionen.

Hier sehen Sie die Hilfedaten für diesen Befehl:

```text
> bin/plugin gantry5 child-theme --help
Usage:
  child-theme [options]
  child-theme
  childtheme

Options:
  -p, --parent=PARENT   Parent theme name
  -c, --child=CHILD     Child theme name
  -l, --clone           Clone outlines and configuration to the child theme
  -L, --no-clone        Do not clone outlines and configuration to the child theme

Help:
  The child-theme creates a new child theme from an existing Gantry theme
```

Hier folgt ein Beispiel für die Terminal-Befehle im Einsatz:

```text
> bin/plugin gantry5 child-theme
Creating new child theme

Enter parent theme name: g5_helium
Enter child theme name: new_helium
Clone outlines and configuration to the child theme [Y/n]:

Success! Child theme new_helium created.
```

Sobald dies erledigt ist, sollten Sie sehen, dass Ihr Child-Theme nun im **Theme**-Panel des **Admin**-Plugins erscheint.

![](test_1.png?classes=shadow,border)
