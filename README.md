[![Join the chat at https://gitter.im/gantry/gantry5](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/gantry/gantry5?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

# Deutsche Gantry Dokumentation

Das Repository enthält den Quellcode der [Gantry-Dokumentation](https://github.com/gantry/gantry5), die auf [http://docs.gantry.org](http://docs.gantry.org) zu finden ist.

Die Dokumentation ist in [Pages/](Pages) und seinen Unterordnern enthalten. Die Ordner-Struktur entspricht genau der Kapitel-Struktur wie sie auf der Haupt-Website zu sehen ist. Das gesamte, hier gefundene Repo ist geeignet als `user/` Verzeichnis in einer [Grav](http://getgrav.org) Installation zu fungieren. Das Repo enthält Themes, Konfigurationsdateien und Einstellungen, die es möglich machen die Dokumentation in der gleichen Optik zu präsentieren wie sie der [Dokumentationswebsite](http://docs.gantry.org) erfolgt.

Die gesamte Dokumentation (alles einfache Textdateien) ist lesbar und mit der [Markdown](http://daringfireball.net/projects/markdown/)-Auszeichnungssprache formatiert.

Eine lokale Kopie und eigene, funktionierende Seiten erstellen - dann empfehlen wir die [Grav](http://learn.getgrav.org/)-Dokumentation zu lesen. Sie enthält die Informationen, die Sie benötigen um Dateistruktur und Syntax zu verstehen.

Wenn Sie eine lokale Kopie der Dokumentation möchten, können Sie entweder [herunterladen](https://github.com/gantry/docs/archive/master.zip) oder Sie können das Repository mit dem folgenden Befehl zu klonen:

~~~ .bash
git clone git://github.com/gantry/docs gantry-docs
~~~


Mitarbeit
------------
Mitarbeit an der Dokumentation ist sehr einfach. 

Contributing to the documentation is very simple. Feel free to fork the repository, add your changes and give back by issuing a pull request. You can even edit the docs directly on GitHub, without having to ever download the files. Make sure to follow the conventions before issuing a pull request.

You are also very welcome to make any suggestions or report any kind of problem with the documentation by opening a new [Issue](https://github.com/gantry/docs/issues/new).

If you decide to fork for providing new content as commits. Please ensure you create a branch for your changes, before making them. This will make the process of integrating them more easier. Every change must pass through the `staging` branch first, so please ensure your pull-requests are directed to the proper branch.

To get started with a local environment into the proper `staging` branch, you can run these commands:

~~~ .bash
git clone git://github.com/gantry/docs gantry-docs
cd gantry-docs
git checkout -b develop origin/develop
~~~


Conventions
-----------

This is a list of few conventions we follow when writing documentation that help keep the repository well organized and consistent. Feel free to use any other file in the docs as reference. We also have a [skeleton](Skeleton.md) with all the conventions in place and with many examples of Markdown in use.

* Every change/pull request must be applied or requested to the [develop branch](https://github.com/gantry/docs/tree/develop). Once reviewed, approved and pulled, it will get merged into the **master** branch and automatically picked up by the website.

* Folder and file names must be written in snake_case and always lowercase. For example, if you wanted to convert “How to Install” in snake_case, you would name it “how_to_install”. Filenames in the "assets" folders must be instead dash concatenated.

* There are some reserved names that can’t be used for anything but the scope they are intended for:

    * **README.md**: [ _file_ ] This is a reserved name of GitHub, used to describe the content of a particular repository directory, like this you are reading right now.

    * **chapter.md**: [ _file_ ] Chapter files introduce chapters in the documentation. These are top-level markdown files that introduce a collection of pages.

    * **docs.md**: [ _file_ ] Docs files are individual markdown files that make up the meat and potatoes of documentation. These files explain a particular subject related to Gantry, such as the [installation guide](pages/01.gantry5/02.basics/03.installation/docs.md) or [tutorial for creating new particles](pages/01.gantry5/06.advanced/01.creating-a-new-particle/docs.md).

    * **REDIRECT.md**: [ _file_ ] This file sorely purpose is to redirect projects to different locations. For example, if a project `/docs/project/subproject/` contains a `REDIRECT.md`, when hitting on the web the `subproject` page, you’ll get redirect to `project`. By default it takes you back one level, although you can configure where to redirect to through YAML headers ([read more about YAML headers below](#yaml-headers)).

* Every header, except for the title one, must be preceded by 2 empty lines and succeeded by no empty line.

* Headers sub lines (`=` and `-`) must always align to the header text. Because this can easily get confusing, be sure to use a mono-spaced fonts. Here a couple of examples of well aligned headers:

    ~~~
    Header H1
    =========

    Header H2
    ---------
    ~~~


YAML Headers
------------

Our Markdown implementation uses special [YAML headers](http://www.yaml.org/spec/1.2/spec.html). These headers are encapsulated in between a set of three dashes and an empty line. This is how a YAML header looks like:

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

The headers allow for a much flexible output. For example we can define a title of a Markdown file based on its header title variable, rather than the file name itself.

Below is a list of supported `YAML` variables that can be used and a description on what they do:

* **title**: The title of the article. This is used whenever a page needs to be referenced. When the title is set on a `TOC` file, it globalize the title for each document in the project itself.

    ```yaml
    ---
    title: Hello World!

    ---
    ```

* **taxonomy**: sets the type of article, and its tags. By default, any documentation file should have `category: docs` and `tag: [gantry(version)]` settings.

    The description supports Markdown inline syntax, such as _strong_, _italic_, _links_. You should not be using anything else (ie, _headers_, _images_ and such).

    ```yaml
    ---
    taxonomy:
        category: docs
        tag: [gantry5]

    ---
    ```


* **gravui**: These settings give you the ability to load specific **gravui** patterns. 

   The supported `gravui` settings are listed below:
   * **enabled**: Sets whether or not gravui is used at all during page rendering. This is most likely to be `enabled: true`.
   * **tabs**: When set to `true` this enables the use of tabs to differentiate between commands that are exclusive to one CMS or another. This defaults to `false` if the line isn't present.
   * **callouts**: When set to `true`, this enables visual callouts to be placed over an image. This is a useful tool when you want to point something out in the image, and provide a tooltip that appears when you move your mouse cursor over it.

* **process**: Process tags give you the ability to do things like inject **Twig** script within the markdown file, and have it execute. This comes in handy when you are doing things like adding classes to images to give them an enhanced appearance. For example, `{.border .shadow}` after a markdown image will apply the `border` and `shadow` classes, giving your image a more refined appearance.
    
    Here is a more complete example of a line in documentation with Twig:

    ```markdown
    ![Administrator](../../configure/gantry-admin/admin_access_1.png) {.border .shadow}
    ```

If you have any questions, feel free to open an [Issue](https://github.com/gantry/docs/issues/new).

_The RocketTheme Team_
