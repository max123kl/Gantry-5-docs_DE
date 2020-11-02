---
title: Seiten-Einstellungen
taxonomy:
    category: docs
    tag: [gantry5]
---

Das Administrator-Panel **Seiten-Einstellungen** ermöglicht es Ihnen, die Ausgabe der Seite zu optimieren. So können Sie zusätzliche Elemente hinzufügen. Dazu gehören Elemente wie die **Favicon**, Facebook- und Twitter- **Meta-Tags** und sogar JavaScript- und/oder CSS-Dateien. Alle diese Elemente sind dafür gedacht, auf der gesamten Website verwendet zu werden und **Seiten-Einstellungen** erlaubt Ihnen, genau das zu tun.

Beim traditionellen Template-Ansatz müssten Sie, um eines dieser Elemente hinzuzufügen, die Datei, die die Struktur der Seite enthält, manuell bearbeiten. Dies ist normalerweise eine `index.php`-Datei. Page Settings vereinfacht diesen Prozess exponentiell, indem es die manuelle Bearbeitungsarbeit in eine einfache und leistungsfähige Form direkt in der Administration abstrahiert.

Dank des Gantry-Kernkonzepts und der Implementierung von Overrides können die Seiteneinstellungen sowohl global als auch Outline-unabhängig sein, falls jemals erforderlich. Sie können damit ein Analyseskript der gesamten Website hinzufügen oder ein anderes Skript anzeigen lassen, je nachdem, welcher Outline eine Seite zugeordnet ist.

## Steuerung und Kontrolle

![Steuerung und Kontrolle](controls.png?classes=shadow,border)

!!! Genau wie bei den [Partikel-Standard-Einstellungen](../particle-defaults#controls), funktioniert das Übersteuern, Filtern und Einklappen der Elemente hier auf die gleiche Weise.

## Head-Eigenschaften

![Partikel-Einstellungen](head_properties.jpg) {.border .shadow}

Der Block **Head-Eigenschaften** erlaubt es Ihnen, alles anzupassen, was zwischen den `<head></head>` Tags liegt. Häufig werden Sie Meta-Tags für Facebook oder Twitter hinzufügen wollen, oder vielleicht möchten Sie einfach etwas Eigenes hinzufügen.

Der vorstehende Screenshot zeigt eine der vielen Möglichkeiten, wie Sie die Head-Eigenschaften erstellen können.

### Meta Tags

**Meta Tags** ist ein Feld, das eine Reihe von Schlüsseln und Werten aufnimmt, diese kombiniert und sie innerhalb `<head></head>` in Form einer `<meta>` Eigenschaft abbildet.
Die Anzahl der verwendeten Meta-Tags ist unbegrenzt. Normalerweise werden Meta-Tags verwendet, um eine Website für Suchmaschinen besser zu definieren und um festzulegen, wie die Website angezeigt wird, wenn sie in Facebook oder Twitter eingebettet ist.

Weitere Einzelheiten zu den Meta-Tags **Facebook's Open Graph** und **Twitter's Cards** finden Sie auf den folgenden Seiten:

- [https://developers.facebook.com/docs/sharing/webmasters](https://developers.facebook.com/docs/sharing/webmasters)
- [https://dev.twitter.com/cards/markup](https://dev.twitter.com/cards/markup)
- [https://dev.twitter.com/cards/getting-started](https://dev.twitter.com/cards/getting-started)


### Custom Content

Das Feld Custom Content (Benutzerdefinierter Inhalt) ist für alles vorgesehen, was man an den `<head>` Tag anhängen möchte. Alle Metadaten, die nach den Spezifikationen innerhalb von <head> erlaubt sind, können hier eingetragen werden, genauso wie Sie es tun würden, wenn Sie eine `index.html`-Datei bearbeiten würden.

Verbreitete Metadaten-Tags sind `<title>`, `<style>`, `<meta>`, `<link>`, `<script>` und `<base>`.

! Es wird dringend empfohlen, Skripte und Stile über den [Assets-Bereich](#assets) oder über [Atoms](#atoms) zu bedienen. Obwohl es verlockend sein kann, Skript- und Tags-Code direkt in dieses Feld zu schreiben, sollte es nur als letzter Ausweg benutzt werden. Prüfen Sie genau, ob Skripte und Stile hier eingefügt werden sollten.

## Body Attributes

![Partikel-Einstellungen](body_attributes.jpg) {.border .shadow}

**Body-Attribute** erlaubt es den Anwendern, die Attribute für das `<body>`-Tag anzupassen und Inhalte direkt nach dem Öffnen von `<body>` oder direkt vor dem Schließen von `</body>` zu setzen.

### Body-ID und Body-Klassen

Das Feld **Body-ID** erlaubt es Anwendern, eine ID für den `<Body>` anzugeben, während **Body-Klassen** es Anwendern erlauben, zusätzliche persönliche Klassennamen hinzuzufügen. Wenn man dem Beispiel im vorstehenden Screenshot folgen möchte, wird die Ausgabe wie folgt gerendert:

```html
<body id="my-site" class="... gantry body-class ...">
```

Gantry selbst fügt dem Body bereits eigene Klassen hinzu, die auf verschiedenen Faktoren basieren, wie z.B. dem betrachteten Menüpunkt, welche Outline verwendet wird, usw.

In den meisten Fällen brauchen Sie keinen benutzerdefinierten Klassennamen hinzuzufügen, aber falls Sie einen solchen benötigen, ist dies der richtige Ort dafür.

### Tag-Attribute

**Tag-Attribute** ist ein Schlüssel/Wert-Feld, das es erlaubt, zusätzliche benutzerdefinierte Attribute für den `<body>` zu rendern. Stellen Sie sich vor, Sie hätten ein Skript geladen, das es dem Benutzer erlaubt, die Scroll-Geschwindigkeit und die automatische Seitenaktualisierung über die Attribute `data-scroll` und `data-refresh` anzupassen.

Das ausgegebene Ergebnis wird gerendert zu:


```html
<body id="my-site" class="... gantry body-class ..." data-scroll="500ms" data-refresh="3mins">
```

### Sections-Layout


Seit Gantry 5.2.0 beziehen sich standardmäßig alle Bereiche im **Layout-Manager** für ihren Stil auf diese Einstellung. Das Feld Sections-Layout bietet drei Arten von Styles an:

1. **Fullwidth (Boxed Content)** (Geschachtelter Inhalt) _[Vorgabe – früher "Fullwidth"]_
2. **Fullwidth (Flushed Content)** (Bündiger Inhalt) _[neu in 5.2.0]_
3. **Boxed**

And this is a visual representation of all three cases

| Fullwidth (Boxed Content) [Vorgabe]                     | Fullwidth (Flushed Content)                         | Boxed                                           |
| :-----:                                                 | :-----:                                             | :-----:                                         |
| ![Fullwidth](fullwidth.jpg?lightbox=963,712&resize=300) | ![Flushed](flushed.jpg?lightbox=963,712&resize=300) | ![Boxed](boxed.jpg?lightbox=963,712&resize=300) |

Diese Stile ermöglichen es den Benutzern, die gesamte Website oder einzelne Abschnitte an ihre eigenen Bedürfnisse anzupassen. Der häufigste Fall ist zum Beispiel, dass ein Abschnitt vollständig bündig sein soll, so dass ein Bild oder ein Hintergrund hinzugefügt werden kann, um ihn an den Rändern abzuschließen.

Um das Verhalten einzelner Abschnitte zu ändern, gehen Sie zum Layout-Manager-Panel und klicken Sie auf das Zahnrad-Aktionssymbol des gewünschten Bereichs. Sie können dann einen anderen Wert für das Feld **Layout** wählen. **Inherit** teilt Gantry mit, dass es die Einstellung aus dem Feld **Seiten-Einstellungen** verwenden soll.

![Layout Section Settings](section-layout.jpg) {.border .shadow}

### Nach `<body>` und Vor `</body>`

Manchmal müssen weitere Stile, Skripte oder Elemente in die Seite eingefügt werden und diese müssen dann entweder am Anfang oder am Ende von `<body>` eingefügt werden.

Ein gutes Beispiel war [Facebooks SDK für JavaScript](https://developers.facebook.com/docs/javascript/quickstart/v1.0) in der Version 1.0. Damals verlangte Facebook von der Website die Angabe eines `<div id="fb-root"></div>` direkt nach dem Öffnen des `<body>`-Tags. Wie Sie aus dem Screenshot-Beispiel von oben sehen können, wäre das der perfekte Ort dafür gewesen.

Sie werden oft Skripte sehen, die erfordern, dass Sie Elemente im Vordergrund auf der Seite rendern und an statt dafür neue Module, Partikel oder Widgets zu erstellen, können Sie Ihr Element hier einfach einfügen. Auch Popups sind hierfür ein gutes Beispiel. Der Inhalt des Modals wird auf der Seite gerendert, ist aber unsichtbar, bis ein Element das Öffnen des Popups auslöst.

## Assets

![Partikel-Einstellungen](assets.jpg) {.border .shadow}

**Assets** ist ein spezieller Abschnitt zum Einfügen spezifischer CSS/JS oder Favicons in die Website. Obwohl alles, was Sie in Assets tun können, auch nur mit [Head-Eigenschaften](#head-properties) und [Body-Attribute](#body-attributes) möglich ist, haben wir diese Teile in einem eigenen Abschnitt entkoppelt.

Assets spielen eine sehr wichtige Rolle beim Custom Templating. Das Einbeziehen von Skripten oder Stilen von Drittanbietern ist sehr üblich geworden, und genau aus diesem Grund ist es wichtig, einen eigenen Abschnitt zu haben, um alles gut organisiert zu halten.

### Favicon und Touch-Symbol

Mit den Eigenschaften **Favicon** und **Touch-Symbol** können Benutzer der Site ein Bild zuweisen, das dann in Form eines Symbols für die Browser-Registerkarte oder in der Startansicht Ihres Bildschirms angezeigt wird.

Beide Felder sind sehr ähnlich, das **Favicon**-Feld verwendet die traditionellere Art der Darstellung und Zuordnung eines Icons zur Website. In der Vergangenheit wurde dies immer mit einer Icon-Datei der Größe **16x16** oder **32x32** realisiert.

Heutzutage sind mit dem Einsatz von Touch-Geräten und der Möglichkeit, eine ganze Website in Lesezeichen oder auf dem Startbildschirm zu speichern neue Standards entstanden, die größere und detailliertere Symbole ermöglichen. **Touch-Symbol** erfüllt diese Anforderungen und ermöglicht es, die Geräte darüber zu informieren, dass Ihre Website Icons mit höheren Auflösungen verwenden kann.

Wenn Sie **Touch-Symbol** verwenden möchten, wird empfohlen, ein Bild zu erstellen, das mindestens **180x180** oder **192x192** Pixel groß ist. Bei kleineren Auflösungen wird das Bild angepasst und verkleinert, aber bei höheren Auflösungen wird ein schöneres Icon angezeigt.

! Gantry beinhaltet nur die gebräuchlichste Verwendung von Touch-Symbolen und arbeitet mit iOS, Android und Windows. Es werden nur Icons herunterskaliert. Wenn Sie eine etwas raffiniertere Verwendung und speziellere Formate suchen, lesen Sie [diesen Artikel](https://mathiasbynens.be/notes/touch-icons). Sie können auch [Online-Tools zum Erstellen von Symbolen](http://realfavicongenerator.net/) verwenden. Die perfekte Stelle für das Hinzufügen von benutzerdefiniert generiertem Icon-Code ist der Bereich [Kopf-Eigenschaften: Benutzerdefinierter Inhalt](#head-properties).

### CSS und JavaScript

Die Funktionen der Felder **CSS** und **JavaScript** sind identisch mit denen von [Custom CSS/JS Atom](#custom-css-js). Das gleiche Verhalten kann durch Hinzufügen eines [Atoms](#atom) erreicht werden, wie unten erläutert.  In einigen Fällen würde man es allerdings vorziehen, die Assets getrennt nach dem Bereich Assets und Atoms zu verwalten. Beide Methoden sind geeignet und es kommt nur darauf an, was Sie bevorzugen.

## Atoms

![Particle Settings](atoms.gif) {.border .shadow}

Seit Gantry 5.2.0 wurden Atome aus dem **Layout-Manager** in den Bereich **Page Settings** (Seiten-Einstellungen) verschoben. Obwohl Atome de-facto Partikel sind und auf die [gleiche Weise](../../advanced/creating-a-new-particle) erstellt werden können, verhalten sie sich unterschiedlich.

Atome sind Partikel, die optisch nicht am Frontend zu sehen sind, aber einem wichtigen Zweck dienen. Sie können auf Basis einzelner Seiten oder als Standard zugewiesen werden, der automatisch für alle Seiten der Website gilt.

Für alle möglichen Zwecke fügen Atoms, wie **Google Analytics** und **Custom CSS / JS**, auf der Seite Skripte ein, die das Rendern der Seite während des Ladens beeinflussen oder ändern. Das ist praktisch für das grundlegende Styling, wie z.B. die Farbgebung und die Auswertung von Analysen.

! Wenn Sie ein Atom verwenden wird der Pfad zu einer lokalen Datei relativ zum Stammverzeichnis der Site und nicht zum Template-Ordner angegeben. Wir empfehlen die Verwendung eines Stream-Links, wie z.B. `gantry-theme://custom/thing.css`, damit der Link auch dann funktioniert, wenn Sie zwischen G5-Themes oder Plattformen wechseln.

### Google Analytics

![Google Analytics](atoms-analytics_settings.png?classes=shadow,border)

Das **Google Analytics** Atom ermöglicht Ihnen das schnelle Hinzufügen Ihres **Google Analytics UA-Codes** zu einem Layout, das während des Ladens der Seite im Hintergrund Ihrer Seite läuft. Es fügt das notwendige Scripting um den Code herum ein, den Sie in den **Einstellungen** des Atoms eingeben.

### Custom CSS / JS

![Custom CSS / JS](atoms-custom_settings.png?classes=shadow,border)

### JavaScript Frameworks

Das Atom **JavaScript Frameworks** gibt Ihnen die Möglichkeit, Ihrer Seite auf eine einfache Weise gängige JS-Bibliotheken hinzuzufügen.

[ui-tabs position="top-left" active="0"]
[ui-tab title="Joomla"]
![JavaScript Frameworks](atoms-frameworks_settings.png?classes=shadow,border)
! In Joomla wird die standardmäßige Bibliotheks-Option **Bootstrap** die aktuelle Implementierung von Bootstrap basierend auf Bootstrap 2.3.2 in Ihre Joomla-Installation laden.
[/ui-tab]
[ui-tab title="WordPress"]
![JavaScript Frameworks](wp_atoms-frameworks_settings.png?classes=shadow,border)
[/ui-tab]
[ui-tab title="Grav"]
![JavaScript Frameworks](grav_atoms-frameworks_settings.png?classes=shadow,border)
[/ui-tab]
[/ui-tabs]

### Lightcase

Lightcase ist ein kleines, handliches Lightbox-Atom, das Ihnen die Möglichkeit gibt, Ihre Bilder zum Leben zu erwecken. Es arbeitet im Hintergrund als ein Atom, das mit einfachem HTML aufgerufen wird. Hier ist ein Beispiel:

```html
<a href="path/to/media.jpg"
   data-rel="lightcase"
   title="Your title"
>
    Your link description or thumb
</a>
```

Um die Vorteile von Lightcase zu nutzen, müssen Sie es lediglich als Atom auf der entsprechenden Seite aktivieren und Bilder, wie oben gezeigt, in HTML einbetten.

Zusätzliche Dokumentation für Lightcase finden Sie hier: [http://cornel.bopp-art.com/lightcase/](http://cornel.bopp-art.com/lightcase/)
