# Hiobmon Homepage [![Build Status](https://travis-ci.org/hiobmon/hiobmon.github.io.svg?branch=develop)](https://travis-ci.org/hiobmon/hiobmon.github.io)
Auf diesem Repository liegt der Sourcecode zu unserer Klosterhomepage.
Die Klosterseite ist derzeit nur unter [https://hiobmon.github.io](https://hiobmon.github.io) zu erreichen.

Es ist geplant, dass unsere Webseite unter folgender URL erreichbar ist:
- https://hiobmon.org _(Hauptseite)_
- https://hiobmon.de _(Weiterleitung auf die .org Domain)_

## Allgemeines Setup
Für die Homepage werden folgende Technologien verwendet:
- [Jekyll](https://jekyllrb.com/) zum generieren von statischen HTML-Seiten.
- [GitHub Pages](https://pages.github.com/) zum Hosten der Webseite.
- [Travis CI](https://travis-ci.org/hiobmon/hiobmon.github.io) als Buildtool.
- Geplant, aber noch nicht umgesetzt: [Forestry.io](https://forestry.io/) als CMS-System.

Um den grundlegende Struktur bzw. die Architektur des Codes zu verstehen, ist es gut,
folgende Seiten aufmerksam durchzulesen, bevor Änderungen an dieser Seite vorgenommen werden.
- Die offizielle [Jekyll Dokumentation](https://jekyllrb.com/docs/).
- Unsere Webseite baut auf diesem [Template](http://incorporated.sendtoinc.com/) auf, welches jedoch im Nachgang stark modifiziert wurde.
- Um die Mehrsprachigkeit zu gewährleisten, wurde das [Jekyll Multiple Languages Plugin](https://github.com/Anthony-Gaudino/jekyll-multiple-languages-plugin) verwendet.
- Viele Template-Seiten enthalten [Liquid-Tags](https://shopify.github.io/liquid/). Dies ist Bestandteil von Jekyll.

## Development
Bevor Du Dich an die Entwicklung der Seite wagst, brauchst Du folgende Dinge:
- Du bist mit der Kommandozeile, Git und GitHub vertraut.
- Du hast Git und Ruby auf deinem Computer installiert.
- Du bist weißt, was [Branching im Kontext](https://nvie.com/posts/a-successful-git-branching-model/) von Git bedeutet.
- Du kennst den GitHub Pull-Request Workflow.
- Du verstehst HTML und CSS und [SASS](https://sass-lang.com/).
- Du hast ein grundlegendes Verständnis von Jekyll bzw. statischen HTML-Generatoren.

Sofern diese Grundlagen vorhanden sind, kannst Du mit der Programmierung beginnen!
So fängst Du an:
- Zuerst brauchst Du einen GitHub Account.
- Anschließend musst Du dieses Repository forken.
- Sobald Du das Repo geforkt hast, musst Du Deinen Fork clonen.

__Wichtig!__ Es wird ausschließlich auf dem ```development``` Branch entwickelt.
Der ```master``` Branch enthält eine jederzeit lauffähige Version der Webseite und wird niemals angetastet. Um die Gründe zu verstehen, scrolle bitte runter zum Kapitel ```Deployment```.

- Du erstellst einen lokalen Feature- oder Bugfix-Branch, z.B. "feature/add_new_page" oder "bugfix/fix_css_rule".
- Jetzt kannst Du Deine Änderungen in den Code einpflegen. Mithilfe des ```bundle exec jekyll serve --watch``` Kommandos kannst Du Dir die statische Seite generieren lassen und unter ```localhost:4000``` im Browser betrachten.
- Du pushst deinen Feature- oder Bugfix-Branch auf Deinen Fork (```origin```).
- Danach erstellst Du einen [Pull-Request auf diesem Repository](https://github.com/hiobmon/hiobmon.github.io/pulls).

## Deployment
Das Deployment und Go-Live erfolgt vollautomatisch und ohne Zutun des Programmierers. Der Deployment-Status lässt sich am Travis CI Build-Badge ablesen: [![Build Status](https://travis-ci.org/hiobmon/hiobmon.github.io.svg?branch=develop)](https://travis-ci.org/hiobmon/hiobmon.github.io). Dieser Build-Badge befindet sich auch weiter oben, rechts neben der Überschrift.

Sobald eine Änderung auf dem ```development``` Branch committed wird, erkennt Travis CI automatisch die Änderungen und generiert den statischen HTML-Code. Der statische HTML-Code wird dann auf dem ```master``` Branch abgelegt.
Der ```master``` Branch wird automatisch mit [https://hiobmon.github.io](https://hiobmon.github.io) gesynct.

Geplant, aber noch nicht umgesetzt: [https://hiobmon.github.io](https://hiobmon.github.io) wird automatisch mit [https://hiobmon.org](https://hiobmon.org) und [https://hiobmon.de](https://hiobmon.de) gesynct.

## Content hinzufügen
Es ist geplant, [Forestry.io](https://forestry.io/) als CMS aufzusetzen. Dieses Plugin erlaubt es, ohne Programmierkenntnisse Blogposts hinzuzufügen. Wie das genau erfolgt, wird in Zukunft auf dem [Wiki](https://github.com/hiobmon/hiobmon.github.io/wiki) dokumentiert werden.
