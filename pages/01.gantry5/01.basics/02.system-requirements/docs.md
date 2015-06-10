---
title: Systemvoraussetzungen
taxonomy:
    category: docs
    tag: [gantry5]
gravui:
    enabled: true
    tabs: true
process:
    twig: true
---

Das Gantry Framework hat gewisse Systemanforderungen. Im Folgenden sind diese Anforderungen in Gruppen aufgelistet:

CMS-Anforderungen
-------------------

{% set tab1 %}

**Joomla 3.4+**

Es wird dringend empfohlen, dass Sie immer die neueste stabile Version von Joomla verwenden, um sicherzustellen, dass alle bekannten Bugs und Sicherheitsprobleme ausgeschlossen werden. Zum Zeitpunkt als dieses Dokument geschrieben wurde ist 3.4 die neueste stabile Version von Joomla. Gantry 5 wird erst richtig mit Joomla 3.4 und höher funktionieren.

{% endset %}
{% set tab2 %}

**WordPress 4.2.2**

Es wird dringend empfohlen, dass Sie immer die neueste stabile Version von WordPress verwenden, um sicherzustellen, dass alle bekannten Bugs und Sicherheitsprobleme ausgeschlossen werden. Zum Zeitpunkt als dieses Dokument geschrieben wurde ist 4.2.2 die neueste stabile Version von WordPress. Wir empfehlen ein WordPress Update falls Sie eine andere Version benutzen.

>>> Die WordPress Version erscheint demnächst.

{% endset %}
{{ gravui_tabs({'Joomla':tab1, 'WordPress':tab2}) }}

## Server-Anforderungen

Wir versuchen sicher zu stellen, dass die Gantry-Vorlagen (und speziell die Gantry Library) mit jeder modernen und sicheren Server-Umgebung arbeitet. Die empfohlenen Mindestanforderungen sind:

    * PHP 5.4+
    * Curl
    * OpenSSL Bibliotheken
    * Multibyte String Unterstützung

## Browser-Anforderungen

Die Back-End Administrations-Anforderungen von Gantry in der empfohlenen Reihenfolge sind wie folgt:

* Google Chrome 41+
* Firefox 36+
* Safari 8+
* Opera 28+
* Internet Explorer 10+ (9 mit begrenzten Funktionalität)

## Entwicklungsumgebungen

Die lokale Entwicklung ist die bevorzugte Methode um mit jedem Gantry basierten Template zu arbeiten. Da die Verarbeitungsgeschwindigkeit und Komfort hier am besten ist. Nachfolgend finden Sie eine Liste der geeigneten Server-Umgebungen, die lokal auf Ihrem Computer installiert werden können:


| Mac OS X                                                                                              | Windows                                                                     | Linux                                                                       |
| :-----                                                                                                | :-----                                                                      | :-----                                                                      |
| [MAMP & MAMP Pro](http://www.mamp.info/)                                                              | [EasyPHP](http://www.easyphp.org/)                                          | [LAMP Bundle](http://en.wikipedia.org/wiki/LAMP_(software_bundle))          |
| [XAMPP for Mac OS X](http://www.apachefriends.org/en/xampp-macosx.html)                               | [WampServer](http://www.wampserver.com/en/)                                 | [XAMPP for Linux](http://www.apachefriends.org/en/xampp-linux.html)         |
| [Zend Server Community Edition](http://www.zend.com/en/products/server-ce/)                           | [Zend Server Community Edition](http://www.zend.com/en/products/server-ce/) | [Zend Server Community Edition](http://www.zend.com/en/products/server-ce/) |
| [Mac Port](http://www.techiecorner.com/174/how-to-install-apache-php-mysql-with-macport-in-mac-os-x/) | [XAMPP for Windows](http://www.apachefriends.org/en/xampp-windows.html)     |                                                                             |


