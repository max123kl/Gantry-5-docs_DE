---
title: Einführung
taxonomy:
    category: docs
    tag: [gantry5]
---

Gantry 5 ist die neueste Generation eines leistungsstarken, flexiblen Open-Source-Frameworks zur Erstellung von Themes, das derzeit für Joomla, WordPress und Grav verfügbar ist.

Eines der Hauptziele bei der Weiterentwicklung von Gantry 5 ist, es Nicht-Entwicklern leichter zu machen, wesentlich mehr Aufgaben selbst zu erledigen, ohne jemals einen Code-Editor aufrufen oder Dateien direkt ändern zu müssen.

In diesem Handbuch stellen wir Ihnen kurz vor, was Gantry ist und wie es die Verwaltung des Designs Ihrer Website unglaublich einfach machen kann.

## Was ist Gantry?
Gantry 5 wurde von Grund auf neu entwickelt, um sowohl dem Entwickler als auch dem Anwender das Leben zu erleichtern. Die mit Gantry 5 erstellten Themes bieten eine gemeinsame Benutzeroberfläche, wodurch die Lernkurve für beide Seiten reduziert wird. Unabhängig davon, ob Sie eine oder fünfzig Websites betreuen, ist der Ablauf für die Bearbeitung Ihres Designs immer gleich, unabhängig davon, wie viele verschiedene Themes Sie verwenden.

Der Schwerpunkt liegt vor allem auf der Anwendung einer GUI zur Gestaltung Ihrer Website, damit Sie nicht alles von Hand programmieren müssen. Viele Optionen können im Administrationsbereich des Template Frameworks geändert werden. Für die fortgeschrittenen Webentwickler unter Ihnen gibt es viele Möglichkeiten, das Styling und andere Dinge zu ändern, da Gantry auf einer Textdatei-Konfiguration (YAML) basiert, deren Bearbeitung einfach ist.

Gantry 5 ist wirklich einfach zu bedienen. Es verfügt über Drag-and-Drop-Funktionalität, mit der Sie das Layout Ihrer Website in Sekundenschnelle dramatisch verändern können, ohne Ihre Tastatur auch nur berühren zu müssen.
Gantry ist ein Themes-Framework. Um die Funktion von Gantry auf Ihrer Website besser zu bestimmen, finden Sie hier einige hilfreiche Definitionen:

[ui-tabs position="top-left" active="0"]
[ui-tab title="CMS"]

Wenn Ihre Webseite ein Haus wäre, dann ist das Content Management System **CMS** das Fundament. Hier werden Ihre Daten abgelegt und verwaltet. Es ist das System, das Sie verwenden, um Inhalte wie Beiträge, Artikel, Seiten, Bilder und mehr einzufügen.

Gantry ist derzeit für drei Content Management Systeme verfügbar:

* WordPress
* Joomla
* Grav

[/ui-tab]
[ui-tab title="Framework"]

Das Framework ist der Rohbau, der Ihrem Haus Struktur verleiht, wie Wände, Fenster, Türen und ein Dach. Es ist das Instrument, mit dem Sie festlegen, wie Ihr Design angewendet wird, wann und wo Inhalte angezeigt werden und wie Ihr Haus im Allgemeinen aussieht.

Bei Gantry ist das Framework das System, mit dem Sie im Backend kommunizieren. Es ermöglicht Ihnen die Auswahl von Farben, Layouts und fast allen anderen Parametern, die das Aussehen der Website beeinflussen.

Es verarbeitet die Elemente simultan, damit Ihre Website genau so funktioniert, aussieht und sich genau so verhält, wie Sie es erwarten.

Ein gutes Framework ermöglicht Ihnen eine nahezu vollständige Kontrolle über das visuelle Erscheinungsbild Ihrer Website. Praktisch alles, was der Benutzer außerhalb der Inhalte sieht, die direkt aus dem Content-Management-System angeboten werden, wird durch das Framework verwaltet.

[/ui-tab]
[ui-tab title="Theme"]

Das Theme oder das Template ist die Vorlage, auf der das Erscheinungsbild Ihrer Website basiert. Im Hausbeispiel sind es die Zierleisten, der Anstrich, die Türgriffe, die Leuchten und so ziemlich jedes kleine Detail, die dem Haus sein unverwechselbares Aussehen und die Atmosphäre verleihen.

Bei Websites, die ein Gantry-basiertes Theme verwenden, profitiert das Theme von dem durch das Framework erstellten Fundament. Dadurch können Sie unterschiedliche Gantry-basierte Themes mit der gleichen, konsistenten Benutzerführung über Themes und Plattformen hinweg konfigurieren.

[/ui-tab]
[/ui-tabs]

## Was sind Outlines, Partikel, Atoms, usw.? (github + me)

Gantry verwendet einfache Namen für seine verschiedenen Features, wie das Hydrogen- und Helium-Template. Das ist bei der Bezeichnung von Gantry-Objekten wie Partikeln und Atomen sehr hilfreich.
Da sich Gantry 5 von allen früheren Gantry-Versionen erheblich unterscheidet, haben wir einige neue Begriffe definiert. Diese sollen helfen, die Zusammenhänge zwischen den neuen Gantry-Funktionen zu verstehen. Hier ist eine kurze Übersicht der gebräuchlichsten Begriffe hinsichtlich Gantry 5.

| Begriff   | Beschreibung                                                                                                                                                                                                                                    |
| :----    | :-----                                                                                                                                                                                                                                         |
| **Outline**  | Ein konfigurierbarer Style, der in einem oder mehreren Bereichen Ihrer Website verwendet wird. Er dient als Container, in dem der Seitenstil, die Seiteneinstellung und das Layout festgelegt werden. Das entspricht einem Template. Auf diese Weise legt Gantry die verschiedenen Elemente auf einer Seite an. |
| **Partikel** | Typischerweise handelt es sich dabei um einen kleinen Daten-Block, der auf dem Frontend verwendet wird. Er verhält sich ähnlich wie ein Widget/Modul, kann aber im Gantry 5 Administrator einfach konfiguriert werden.                                                                                         |
| **Atom**     | Eine besondere Form von Partikel, der nicht gerenderte Daten enthält, wie z.B. individuelle Skripte (JS, CSS usw.) oder Analyse-Skripte für die Überwachung des Datenverkehrs.                                                                                                        |
| **Nucleus**  | Dabei handelt es sich um das eigene Frontend-Framework von Gantry 5. Es handelt sich um ein sehr einfaches und schlankes, nur aus CSS/SCSS-Dateien bestehendes Framework.                                                                                                                                       |

Eine vollständige, detailliertere Übersicht über die in Gantry 5 verwendeten Begriffe finden Sie in unserem [Terminologie](../terminology/)-Leitfaden.

Ein Grund, warum Gantry sich entschieden hat, diesen Elementen eindeutige Namen zu geben, ist die Schaffung einer konsistenten Benutzeroberfläche über mehrere Plattformen hinweg. Zum Beispiel werden Begriffe wie Modul (Joomla) und Widget (WordPress) verwendet, um modulare Inhaltsblöcke zu beschreiben, die auf dem Frontend erscheinen. In Gantry werden Partikel nicht nur anders verwaltet als entweder Module oder Widgets, sondern es würde auch Verwirrung stiften, ihnen einen der beiden Namen zu geben. Deshalb haben wir uns entschieden, stattdessen ein eigenes Namensschema zu schaffen.

## Den Gantry Administrator aufrufen

![Admin](intro_admin.jpeg?classes=shadow,border)

Das Backend von Gantry ist vollgepackt mit Funktionen, mit denen Sie praktisch jeden Aspekt Ihrer Website konfigurieren und anpassen können. Es gibt zwar einige geringfügige Unterschiede in dem/den Panel(s), die im Administrator von CMS zu CMS sichtbar sind, aber die Bedienung ist einheitlich, egal welches CMS Sie verwenden.

Es gibt verschiedene Möglichkeiten, auf den Gantry 5 Administrator zu gelangen, je nachdem, welches CMS Sie verwenden. Wir haben hier ein [vollständiges Handbuch](../../configure/gantry-admin), das Ihnen helfen soll, den für Sie am besten geeigneten Weg zu finden.

Hier sind einige der administrativen Panels, die Sie aufrufen können:

#### Stile

![Admin](intro_style.jpeg?classes=shadow,border)

Das administrative Panel **Stile** ermöglicht Ihnen die schnelle und einfache Konfiguration von Einstellungen, die sich auf das Erscheinungsbild des Gantry-basierten Designs beziehen. Dazu gehört die Möglichkeit, zwischen vorkonfigurierten Presets zu wechseln und das Aussehen einer Outline mit Hilfe einer Reihe von Stileinstellungen, die mit dem Theme verknüpft sind, zu verfeinern.

Wenn Sie das Farbschema Ihrer Website, die Schriftarten oder die Animation der Dropdown-Funktion Ihres Menüs ändern möchten, sind Sie hier richtig.

<div align="center"><a href="../configure/styles" class="button"><i class="fa fa-fw fa-graduation-cap"></i> Mehr über Styles erfahren</a></div>

#### Partikel Standard

![Admin](intro_particle.jpeg?classes=shadow,border)

Das Panel **Partikel Standard** ist ausgesprochen nützlich, wenn Sie Ihren Partikeln globale Standardeinstellungen geben wollen. In der Regel erscheint es nur in der **Basis Outline** und alle Änderungen, die Sie hier vornehmen, werden zur Standardeinstellung des Partikels. In den meisten Fällen werden Sie hier Dinge einstellen, die statisch sind, wie das Logo und die Copyright-Informationen.

Es ist auch eine gute Wahl, wenn Sie eine bestimmte Art von Partikeln global **an** oder **aus** schalten wollen. Diese Option ist sinnvoll, wenn Sie einen benutzerdefinierten Partikel für ein temporäres Event auf Ihrer Website verwenden wollen, wie z.B. eine Verkaufsankündigung. Sie haben diesen Partikel an mehreren verschiedenen Stellen in verschiedenen Layouts platziert.

Sie müssen diesen Partikel ausschalten, um zu verhindern, dass er nach dem Ende des Angebots auf Ihrer Website erscheint. Sie könnten jede Seite einzeln durchgehen und den Partikel nacheinander entfernen, oder Sie könnten den Partikel in dem Panel **Partikel Standard** ausschalten, sodass er auf Ihren Seiten verschwindet. Wenn Sie ihn bei Ihrer nächsten Verkaufsaktion mit **an** wieder aktivieren, erscheint er erneut auf Ihren Seiten.

<div align="center"><a href="../configure/particle-defaults" class="button"><i class="fa fa-fw fa-graduation-cap"></i> Mehr über Partikel-Standards erfahren</a></div>

#### Seiten-Einstellungen

![Admin](intro_pagesettings.jpeg?classes=shadow,border)

Möchten Sie Google Analytics-Code zu einer Outline hinzufügen? Wie wäre es, ein Favicon für Ihre Website festzulegen? Sie können diese Einstellungen und vieles mehr im Verwaltungsbereich **Seiten-Einstellungen** vornehmen. In diesem Panel können Sie Meta-Tags, JavaScript-/CSS-Dateien und vieles mehr auf Ihrer Webseite einsetzen. Es ist die zentrale Schaltstelle für das Hinzufügen von Skripten im Header und Footer Ihrer Website.

Sie können diese Anpassungen in Ihre **Basis Outline** einfügen, damit sie global gelten oder in eine individuelle **Outline**, damit sie nur für die der Outline zugewiesenen Seiten gelten.

<div align="center"><a href="../configure/page-settings" class="button"><i class="fa fa-fw fa-graduation-cap"></i> Mehr über Seiten-Einstellungen erfahren</a></div>

#### Layout Manager

![Admin](intro_layout.jpeg?classes=shadow,border)

Ihnen missfällt, wo auf der Seite ein bestimmtes Element steht? Klicken Sie einfach darauf und ziehen Sie es im **Layout Manager** mit der Maus auf die gewünschte Position. Sie können Dinge hinzufügen, entfernen, die Größe ändern, Modul-/Widget-Positionen erstellen und Partikel konfigurieren, ohne die Tastatur zu berühren.

[plugin:youtube](https://www.youtube.com/watch?v=DN_U_W7LT_c)

Elemente wie Ihr Logo, Copyright-Informationen, Branding, Social-Symbole und mehr können ebenfalls direkt vom Layout-Manager aus angepasst werden.

Befürchten Sie, Sie könnten etwas falsch machen? Sie können alle während einer Sitzung im Layout-Manager durchgeführten Aktionen mit einem Mausklick rückgängig machen und wiederherstellen.

<div align="center"><a href="../configure/layout-manager" class="button"><i class="fa fa-fw fa-graduation-cap"></i> Mehr über den Layout-Manager erfahren</a></div>

#### Zuweisungen

![Admin](intro_assignments.jpg?classes=shadow,border)

Das Panel **Zuweisungen** bietet Ihnen die Möglichkeit, bestimmten Seiten oder Inhaltskategorien **Outlines** zuzuweisen. Das funktioniert von einer Plattform zur anderen etwas anders, die Grundfunktion bleibt jedoch die gleiche. Wenn Sie beispielsweise eine **Outline** speziell für die Startseite Ihrer Website erstellen, können Sie diese hier der Startseite zuweisen.

<div align="center"><a href="../configure/assignments" class="button"><i class="fa fa-fw fa-graduation-cap"></i> Mehr über Zuweisungen erfahren</a></div>

#### Menü-Editor

![Admin](intro_menu.jpg?classes=shadow,border)

Der Menü-Editor von Gantry 5 bietet eine schnelle und unkomplizierte Methode zur nicht-destruktiven Kontrolle der Darstellung von Menüs im Frontend Ihrer Website. Sie können Menüelemente einfach per Drag & Drop neu positionieren, Partikel einfügen und vieles mehr.

Im Grunde genommen nimmt er Ihre Menüs aus dem CMS und gestaltet sie um, bevor er sie an den Betrachter weiterleitet.

[plugin:youtube](https://www.youtube.com/watch?v=Ny0KgUz5JH8)

Alles, was Sie in Gantry 5 ändern, ist nicht-destruktiv, d.h. Ihre Inhalte und Menüs werden genau so belassen, wie sie waren. Sie müssen sich also keine Sorgen machen, wenn Sie irgendetwas tun, das das endgültige Erscheinungsbild Ihrer Website innerhalb des Gantry 5-Administrators stören würde.

<div align="center"><a href="../configure/menu-editor" class="button"><i class="fa fa-fw fa-graduation-cap"></i> Mehr über den Menü-Editor erfahren</a></div>

#### Outlines

![Outlines](../../configure/outlines/outline_1.png?classes=shadow,border)

Das Administrator-Panel **Outlines** ist ein globaler Startpunkt für die Erstellung, Duplizierung und den Zugriff auf Ihre Outlines.

Sie werden auf dieser Seite feststellen, dass es zwei verschiedene Arten von Outlines gibt: **Standard** und **System**. Eine Standard-Outline enthält alles, was Sie einer typischen Seite zuordnen können. Dazu gehört die **Basis-Outline**, mit der Sie globale Stil- und Einstellungsstandards für Ihr Theme festlegen können, sowie Outlines, die Sie normalen Seiten wie der Homepage zuweisen oder die Sie als Standard für Ihre Inhaltsseiten verwenden können.

![Outlines](../../configure/outlines/outline_5.png?classes=shadow,border)

**System-Outlines** sind in den Kern von Gantry eingebaut. Sie sind mit bestimmten Seitentypen, wie Error oder Offline, verknüpft. Diese Outlines können bearbeitet, aber nicht erstellt, umbenannt oder gelöscht werden, da sie den Kern von Gantry bilden.

Dieses Panel ermöglicht es Ihnen, Ihre Outlines auf unterschiedliche Arten zu bearbeiten und wir werden diese jetzt näher analysieren.

#### Extras

[ui-tabs position="top-left" active="0"]
[ui-tab title="Joomla"]

![Admin](intro_extras_joomla.jpeg?classes=shadow,border)

[/ui-tab]
[ui-tab title="WordPress"]

![Admin](intro_extras_wp.jpeg?classes=shadow,border)

[/ui-tab]
[ui-tab title="Grav"]

![Admin](intro_extras_grav.jpeg?classes=shadow,border)

[/ui-tab]
[/ui-tabs]

Die Dropdown-Auswahl **Extras** gibt Ihnen raschen Zugriff auf einige praktische Optionen, die der gesamte Administrator direkt nutzen kann. Dazu gehören der Umschalter **Entwicklungsmodus**, ein **Cache leeren** sowie ein **Plattform-Einstellungen** Auswahlfeld, das Sie zu einer plattformspezifischen Konfigurationsseite für Gantry führt.

<div align="center"><a href="../configure/extras" class="button"><i class="fa fa-fw fa-graduation-cap"></i> Mehr über Extras erfahren</a></div>

## Partikel-System

Dank des Partikel-Systems von Gantry kann ein Entwickler Inhaltsblöcke für Ihre Website erstellen, die Sie hinzufügen, entfernen und aktualisieren können, ohne Angst haben zu müssen, die Website zu beschädigen oder sich mit einer einzigen Codezeile befassen zu müssen. Einfache Eingabefelder und Umschalter machen es leicht, praktisch alles auf Ihrer Website zu finden und zu ändern.

Das bedeutet, dass Sie für einfachere Anpassungen seltener mit dem Entwickler sprechen müssen. Melden Sie sich einfach an, greifen Sie auf den Gantry 5 Administrator zu, nehmen Sie Ihre Änderungen vor und speichern Sie.

[ui-tabs position="top-left" active="0"]
[ui-tab title="Joomla"]

Kennen Sie sich mit dem Modul-System von Joomla aus? Gantry 5 integriert sich vollständig in Joomla, so dass Sie Modulpositionen weiterhin wie gewohnt verwenden können. Es ist super einfach, eine neue Modulposition in wenigen Augenblicken mit dem Layout-Manager und dem Menü-Editor zu erstellen.

[/ui-tab]
[ui-tab title="WordPress"]

Kennen Sie sich mit dem Widget-System von WordPress aus? Gantry 5 integriert sich vollständig in WordPress, so dass Sie Widget-Positionen weiterhin wie gewohnt benutzen können. Es ist super einfach, mit dem Layout-Manager in wenigen Augenblicken eine neue Widget-Sektion zu erstellen.

[/ui-tab]
[ui-tab title="Grav"]

Die Grav ist in einer eindeutigen Ausgangsposition, um die Vorteile der Partikel in Gantry 5 voll auszunutzen. Neben der Möglichkeit, an beliebiger Stelle auf der Seite Partikel hinzuzufügen, können Grav-Benutzer die Vorteile des neuen Administrationsbereichs **Positionen** nutzen, mit dem Sie Positionen erstellen können, die mehrere, gestaffelte Partikel aufnehmen können, die problemlos in jedem Layout platziert werden können.

Das spart mit Grav viel Zeit und schafft ein modernes Layout-System, das normalerweise größeren Content-Management-Systemen wie Joomla vorbehalten ist.

[/ui-tab]
[/ui-tabs]

Das Partikel-System in Gantry 5 verleiht seinen Themes eine außerordentliche Flexibilität. Für Entwickler ist es einfacher, benutzerdefinierte Elemente zu erstellen und sie direkt auf Ihrer Website anzuwenden - ganz unabhängig vom Content-Management-System. Für Endbenutzer ist es eine einfache und leichte Möglichkeit, Inhalte zu Ihren Seiten hinzuzufügen. Sie können ein Formular ausfüllen, anstatt einen Code-Editor zu öffnen. Sie können Ihre Website mit Inhalten und Funktionen vollpacken, ohne auch nur eine einzige Zeile Code ansehen zu müssen.

<div align="center"><a href="../particles/particles" class="button"><i class="fa fa-fw fa-graduation-cap"></i> Mehr über das Partikel-System erfahren</a></div>

## Wo kann man Hilfe finden?

Wenn Sie irgendwelche Probleme mit Gantry haben, können Sie uns gerne informieren, indem Sie ein Issue über das [GitHub-Projekt](http://github.org/gantry/gantry5) verfassen oder uns über den [Gitter-Chat](http://gitter.im/gantry/gantry5) kontaktieren.

Falls Sie sich die neuesten Gantry-Versionen ansehen möchten, um einen Überblick über die neuesten Entwicklungen im Gantry-Projekt zu erhalten, laden wir Sie ein, sich unsere CI-Builds anzusehen, die für Joomla, WordPress und Grav verfügbar sind. Außerdem stehen CI-Builds für das kostenlose Theme „Hydrogen“ zum Download bereit.

Mit [Gitter](https://gitter.im/gantry/gantry5) wurde ein Chat-Room eingerichtet, in dem Sie sich mit Entwicklern, Autoren und anderen Mitwirkenden aus der Community über das Projekt austauschen können. Dies ist der beste Ort, um schnelle Tipps zu erhalten und Funktionen mit anderen zu diskutieren.

<div align="center"><a href="http://gitter.im/gantry/gantry5" class="button"><i class="fa fa-fw fa-support"></i> Chatten Sie mit uns auf Gitter</a></div>

Sie können sich auch die Quell-Dateien ansehen und frühere und aktuelle Versionen von Gantry 5 [direkt über GitHub](http://github.com/gantry/gantry5) herunterladen. Dort können Sie außerdem am besten Probleme und Fehlerberichte melden, auf die Sie bei der Verwendung von Gantry 5 stoßen.

<div align="center"><a href="http://github.org/gantry/gantry5" class="button"><i class="fa fa-fw fa-github"></i> Ein Issue auf GitHub verfassen</a></div>

Viele weitere Informationsquellen finden Sie auch hier in der Gantry-Dokumentation. Im nächsten Kapitel gehen wir auf die verschiedenen Bereiche des Gantry 5-Administrators ein und erläutern, wie er Ihnen dabei helfen kann, mehr aus Gantry 5 herauszuholen.
