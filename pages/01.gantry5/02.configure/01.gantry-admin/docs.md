---
title: Gantry-Admin
taxonomy:
    category: docs
    tag: [gantry5]
---

Der **Gantry-Admin** ist eine Reihe von Einstellungen, die zum Einrichten und Konfigurieren eines mit Gantry arbeitenden Themes verwendet werden. Er fungiert als zentrale Kommandozentrale für so ziemlich alles und jedes, das Sie im Zusammenhang mit dem Theme, dem Layout, den Voreinstellungen, dem Menü und den Zuweisungen ändern können.

Sie erreichen den Gantry Admin, wenn Sie diesen Schritten folgen:

[ui-tabs position="top-left" active="0"]
[ui-tab title="Joomla"]

[plugin:youtube](https://www.youtube.com/watch?v=JWKpeFRqcDI)

Als erstes müssen Sie sicherstellen, dass das Gantry-Framework und ein aktives Gantry-Template installiert und ausgewählt sind. Eine detaillierte Schritt-für-Schritt-Anleitung hierzu finden Sie in [unserer Anleitung](../../basics/installation).

![Kontroll-Panel Methode](../../basics/installation/gantry_default.png?classes=shadow,border)

Sobald dies erledigt ist, navigieren Sie zu **Administrator → Erweiterungen → Templates** und wählen Sie das Gantry-Template aus, das Sie konfigurieren möchten. Das sollte Sie zum Abschnitt **Übersicht** des Gantry-Admin für diese Vorlage führen.

![Kontroll-Panel Methode](gantry_update_1.png?classes=shadow,border)

Alternativ können Sie auf den Gantry 5-Administrator zugreifen, indem Sie zum **Kontrollzentrum** im Backend von Joomla navigieren und **Gantry 5 Themes** in der Seitenleiste links unter dem Abschnitt **Erweiterungen** auswählen.

![Komponenten-Methode](admin_access_1.png?classes=shadow,border)

Es gibt eine dritte Methode, die einfach durch Navigation zu **Komponenten → Gantry 5 Themes** im Administrationsmenü des Backend von Joomla erreicht werden kann.

[/ui-tab]
[ui-tab title="WordPress"]

Als erstes müssen Sie sicherstellen, dass das Gantry-Framework und ein aktives Gantry-Template installiert und ausgewählt sind. Eine detaillierte Schritt-für-Schritt-Anleitung hierzu finden Sie in [unserer Anleitung](../../basics/installation).

[Timber](https://wordpress.org/plugins/timber-library/) ist ein Plugin eines Drittanbieters, durch das WordPress mit dem Gantry5-System zusammenarbeiten kann. Da Timber automatisch mit Gantry installiert wird, brauchen Sie es nicht separat zu installieren, um Gantry nutzen zu können.

![Sidebar](wp_sidebar.png?classes=shadow,border)

Sobald dies erledigt ist, navigieren Sie zu **Administrator → (Theme-Name)-Theme**. Dadurch sollten Sie zum Abschnitt **Übersicht** des Gantry-Administrators für dieses Theme gelangen.

[/ui-tab]
[ui-tab title="Grav"]

Als erstes müssen Sie sichergehen, dass das Gantry-Framework installiert und aktiv ist. Eine detaillierte Schritt-für-Schritt-Anleitung dazu finden Sie in [unserer Anleitung](../../basics/installation).

![Sidebar](grav_sidebar.png?classes=shadow,border)

Sobald dies erledigt ist, navigieren Sie zu **Administrator → Gantry 5** in der Seitenleiste. Klicken Sie auf das Gantry-Logo. Dadurch sollten Sie zum Abschnitt **Available Themes** des Gantry-Administrators gelangen. Hier können Sie das Theme wählen, das Sie konfigurieren möchten, indem Sie auf die Schaltfläche **Konfigurieren** klicken.

[/ui-tab]
[/ui-tabs]

Admin-Panels
-----

Jeder Karteireiter im oberen Bereich vom **Gantry Admin** gibt dem Benutzer einen schnellen Zugriff auf verschiedene Elemente des von Gantry gesteuerten Themes. Diese Abschnitte, die als *Panels* bezeichnet werden, machen es einfach, schnell zu der Einstellung zu navigieren, die Sie anpassen wollen.

Es gibt zwei verschiedene Arten von Panels. Die erste, die sich ganz oben im **Gantry Admin** befindet, sind globale Einstellungen, die sich nicht nur auf die von Ihnen gewählte Outline, sondern auf die Website als Ganzes auswirken. Dazu gehören die Panels **Menu** und **About**. Zusätzlich können Sie das **Outlines**-Panel verwenden, um neue Outline-Entwürfe für Ihre Site zu verwalten und zu erstellen.

Die zweite Art von Elementen ist auf der grauen Registerkartenleiste zu finden und ermöglicht es Ihnen, die Einstellungen für die aktuell ausgewählte Outline zu optimieren. Diese **Outline-spezifischen** Panels ermöglichen es Ihnen, jeder Seite Ihrer Website ein individuelles Aussehen zu geben, indem Sie z.B. Ihre Startseite visuell von Ihrer About-Seite abheben.

Eine kurze Beschreibung jedes dieser Panels finden Sie weiter unten.

### Globale Admin-Panels

Die **globalen Admin-Panels** betreffen nicht eine einzelne Outline, sondern haben Einfluss auf das gesamte Theme. Diese Panels ermöglichen es Ihnen, zwischen einzelnen Outlines zu wechseln und diese zu bearbeiten, die Menüs zu bearbeiten und zu konfigurieren und mehr über das Gantry-gestützte Theme zu erfahren.

#### Outlines

![Outlines](outlines.jpg?classes=shadow,border)

In diesem Panel können Sie neue Outlines verwalten und erstellen, jede mit einem eigenen Set aus Layout, Stil, Zuweisungen und Partikeleinstellungen. Es gibt zwei Arten von Outlines, **Standard** und **System**.

**Standard Outlines** können vom Benutzer erstellt werden, basierend auf einem der vorhandenen **Layout-Presets** und den unterschiedlichen Seitentypen zugewiesen werden, um ihnen ein eigenes Layout und/oder einen eigenen Satz von Einstellungen zu verleihen. Ihre **Base** Outline verhält sich wie die **Master** Outline in Gantry 4, wobei alle übrigen Outlines Vorrang haben, so dass Sie die Voreinstellungen entsprechend den Anforderungen einer bestimmten Seite ändern können.

**System-Outlines** sind zentrale Outlines, die mit bestimmten Seitentypen, wie 404 oder Offline, verlinkt sind. Diese Outlines können bearbeitet, aber nicht erstellt, umbenannt oder gelöscht werden, da sie den zentralen Bestandteil von Gantry bilden.

Sie können auf zwei Arten zu einer individuellen Outline wechseln. In diesem Panel können Sie eine bestimmte Outline in den Outline-spezifischen Panels des Admin als aktiv einstellen, indem Sie auf die zugehörigen **Bearbeiten**-Buttons klicken. Alternativ können Sie zwischen diesen Schaltflächen mit Hilfe des Dropdown-Menüs auf der linken Seite der Symbolleiste wechseln, in der sich die **outline-spezifischen administrativen Panels** befinden.

![Outlines](outlines2.jpg?classes=shadow,border)

Outlines können sehr einfach umbenannt werden, und zwar an mehreren verschiedenen Stellen. Sie können dies sowohl vom administrativen Panel **Outlines** als auch von jedem outline-spezifischen Panel (Stile, Seiteneinstellungen, Layout und Zuweisungen) aus tun, indem Sie das kleine Bleistift <span class="fa fa-pencil"></span> Symbol neben der Dropdown-Liste für die Outline-Auswahl anklicken.

<div align="center"><a href="../configure/outlines" class="button"><i class="fa fa-fw fa-graduation-cap"></i> Mehr über das Admin-Panel für Outlines erfahren</a></div>

#### Menü

![Menü](menu_module_1.png?classes=shadow,border)

Der **Menü-Editor** macht es einfach, Menüs zu konfigurieren und Informationen zu Menüs hinzuzufügen, wie sie auf Ihrer Website erscheinen. Praktisch jeder Aspekt des Erscheinungsbildes und der Anordnung der Menüs kann von diesem Panel aus geändert werden.

Das Gantry-Menüsystem greift auf Informationen aus dem CMS-eigenen Menüsystem zu und erstellt einen Override, der es Ihnen ermöglicht, Elemente neu anzuordnen und so zu konfigurieren, wie Sie es am Frontend angezeigt haben möchten. Diese Anpassungen werden dann dem Besucher präsentiert. Die Änderungen, die Sie am Menü vornehmen, haben keinen Einfluss auf die Art und Weise, wie das CMS das Menü verwendet. Wenn Sie Änderungen an der Seitenanordnung oder an einer anderen CMS-spezifischen Eigenschaft vornehmen müssen, müssen Sie dies weiterhin über den nativen Menümanager tun.

<div align="center"><a href="../configure/menu-editor" class="button"><i class="fa fa-fw fa-graduation-cap"></i> Mehr über den Menü-Editor erfahren</a></div>

#### Über

![Über](about.png?classes=shadow,border)

Das Panel **Über** ermöglicht es dem Entwickler des Themes, Informationen über das Theme zu platzieren, wie z.B. eine Feature-Liste und Credits, sowie Links zur Dokumentation und einen Referenz-Screenshot. Hier können Benutzer auch schnell den aktuell aktivierten Theme-Namen, die Versionsnummer und Informationen zum Entwickler finden.

#### Seiten-Einstellungen

[ui-tabs position="top-left" active="0"]
[ui-tab title="Joomla"]

![Inhalt](page.jpg?classes=shadow,border)

Der Administrationsbereich **Seiten-Einstellungen** gibt Ihnen schnellen Zugriff auf globale Seiten-Einstellungen, die sich auf die Site auswirken. Dazu gehören **Atome**, **Body-Attribute**, **Head-Eigenschaften** und **Assets** wie das Favicon und CSS/JavaScript, die der Seite zur Verfügung stehen sollen.

[/ui-tab]
[ui-tab title="WordPress"]

![Inhalt](wp_page.jpg?classes=shadow,border)

Der Administrationsbereich **Seiten-Einstellungen** gibt Ihnen schnellen Zugriff auf globale Seiten-Einstellungen, die sich auf die Site auswirken. Dazu gehören **Atome**, **Body-Attribute**, **Head-Eigenschaften** und **Assets** wie das Favicon und CSS/JavaScript, die der Seite zur Verfügung stehen sollen.

[/ui-tab]
[ui-tab title="Grav"]

![Inhalt](grav_page.jpg?classes=shadow,border)

Der Administrationsbereich **Seiten-Einstellungen** gibt Ihnen schnellen Zugriff auf globale Seiten-Einstellungen, die sich auf die Site auswirken. Dazu gehören **Atome**, **Body-Attribute**, **Head-Eigenschaften** und **Assets** wie das Favicon und CSS/JavaScript, die der Seite zur Verfügung stehen sollen.

[/ui-tab]
[/ui-tabs]

### Outline-spezifische Panels

**Outline-spezifische Panels** bieten Benutzern die Möglichkeit, das Layout, die Einstellungen und Zuordnungen einer bestimmten Outline anzupassen. In Gantry 4 wurden *Outlines* als *Overrides* bezeichnet.

#### Styles

![Styles](styles.jpg?classes=shadow,border)

[plugin:youtube](https://www.youtube.com/watch?v=I0f4bXxZkVQ)

Mit Hilfe des **Styles**-Panels lassen sich visuelle Elemente, die mit dem Gantry-gesteuerten Theme verbunden sind, schnell und einfach anpassen. Dazu können farbcodierte Voreinstellungen, Schriftarten, Akzentfarben und Farben für bestimmte Bereiche der Seite sowie benutzerdefinierte Elemente wie Farben, Blockstile und Hintergründe gehören. Grundsätzlich kann hier alles konfiguriert werden, was von der Gestaltung mit CSS beeinflusst wird und sich auf das Seitendesign bezieht.

<div align="center"><a href="../configure/styles" class="button"><i class="fa fa-fw fa-graduation-cap"></i> Mehr über das Styles-Panel erfahren</a></div>

#### Partikel-Standards

![Partikel-Standards](settings.jpg?classes=shadow,border)

Das Panel **Partikel-Standards** ist eine virtuelle Kommandozentrale für Partikel. Hier können Sie Partikel schnell ein- und ausschalten und ihre globalen Einstellungen konfigurieren.

<div align="center"><a href="../configure/particle-defaults" class="button"><i class="fa fa-fw fa-graduation-cap"></i> Mehr über das Panel Partikel-Standards erfahren</a></div>

#### Layout

![Layouts](layout.jpg?classes=shadow,border)

Das ist das Panel **Layout-Manager**, mit dem Sie Partikel, Inhalt und Widget-/Modulpositionen für Ihr Theme anordnen können. In diesem Panel legen Sie im Prinzip fest, wie die Elemente der Seite angeordnet werden und was sie enthalten sollen. Zusätzlich können Sie auf individuelle Einstellungen für Partikel, Blöcke, Abschnitte und Raster zugreifen.

<div align="center"><a href="../configure/layout-manager" class="button"><i class="fa fa-fw fa-graduation-cap"></i> Mehr über das Layout-Panel erfahren</a></div>

#### Zuweisungen

![Zuweisungen](assignments.jpg?classes=shadow,border)

Das Panel **Zuweisungen** ist Ihre zentrale Stelle für die Zuweisung von Outlines zu bestimmten Seiten. Wenn Sie zum Beispiel eine Outline eingerichtet haben, die Sie speziell für Ihre **Über** Seite anwenden möchten, können Sie dies hier tun.

<div align="center"><a href="../configure/assignments" class="button"><i class="fa fa-fw fa-graduation-cap"></i> Mehr über das Zuweisungs-Panel erfahren</a></div>

#### Inhalt (WordPress)

[ui-tabs position="top-left" active="1"]
[ui-tab title="Joomla"]

Das administrative Panel **Inhalt** ist unter Joomla nicht verfügbar, da Joomla diese Einstellungen in seinem eigenen integrierten System verwaltet.

[/ui-tab]
[ui-tab title="WordPress"]

![Inhalt](wp_content.jpg?classes=shadow,border)

Das administrative Panel **Inhalt** gibt Ihnen die Möglichkeit, schnell und einfach zu definieren, wie der Inhalt auf einer vorgegebenen Seite angezeigt werden soll.

Sie können dieses Panel beispielsweise verwenden, um festzulegen, welche Kategorien auf einer Seite erscheinen, sowie Metainformationen wie Autoren-Tags, Kommentare, die Größe der dargestellten Bilder und mehr.

Die folgenden Seitentypen haben jeweils ihre eigene Sammlung von Einstellungen:

* Blog
* Page
* Post
* Archive

Auf diese Weise können Sie die Anzeige der Daten je nach Art der Seite, auf der sie angezeigt werden, verfeinern. Ihre Outlines erhalten dadurch eine größere Flexibilität und verkürzen dadurch die Entwicklungszeit erheblich.

[/ui-tab]
[ui-tab title="Grav"]

Das administrative Panel **Inhalt** ist derzeit in Grav nicht verfügbar.

[/ui-tab]
[/ui-tabs]
