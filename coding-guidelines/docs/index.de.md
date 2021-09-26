# Einleitung

## Was ist das?
Dieses Dokument soll versuchen Richtlinien und Standards über mehrere
Programmiersprachen hinweg zu definieren. Natürlich muss man sich auch daran
halten, was man selber predigt, weshalb aus meiner täglichen Arbeitsweise
entstanden sind und diese auch wiederspiegeln. Nicht alle Punkte sind rational
zu begründen, einige sind einfach Entscheidungen, die ich für mich getroffen
habe, da es mehrere _richtige_ Weisen gibt. Am Ende spielt das allerdings
alles keine Rolle, solange man sich konsistent an seine eigenen Regeln hält.

## Warum solltest Du dieses Dokument nutzen?

Auch wenn manche der Meinung sind, dass Coding Guidelines unnötiger Overhead
sind oder die Kreativität einschränken, hat sich dieser Ansatz bereits über
mehrere Jahre hin bewährt. Das liegt daran, dass nicht jedem/jeder Entwickler:

- bewusst ist, dass Code in der Regel 10-mal häufiger gelesen als geändert wird.
- bewusst ist, dass manche Konstrukte Probleme verursachen, selbst wenn sie
  in anderen Programmiersprachen gut funktionieren
- der Einfluss von bestimmten Lösungen in Bezug auf z. B. Sicherheit oder
  Performance, oder das Ignorieren solcher, bekannt ist.
- versteht, dass andere Entwickler eventuell nicht genug Erfahrung oder
  Know-How haben um elegante aber möglicherweise abstrakte Lösungen zu
  verstehen.

## Grundlagen
Selbst wenn dieses Dokument viele Punkte abdeckt, wird es nie alle möglichen
Szenarien behandeln, alleine um es nicht übermäßig aufzublähen. Und entgegen
der Meinung mancher (Junior) Developers, heißt es nicht, nur weil etwas nicht
ausdrücklich als schlecht aufgeführt wird, dass die Nutzung davon okay ist.

Es gibt eine handvoll Regeln, die auf alle Situationen, unabhängig von ihrem
Kontext, angewendet werden können. Dazu zählen folgende:

- [Principle of least astonishment (a.k.a. POLA)][pola]: Entwickler Lösungen die
  jeder Versteht und erwartet.
- [Keep it simple, stupid (a.k.a. KISS)][kiss]: Die einfachste Lösung ist mehr
  als ausreichend.
- [You aren't gonna need it (a.k.a. YAGIN)][yagin]: Erstelle Lösungen nur für
  Probleme und Anforderungen die aktuell bestehen, nicht für welche, von denen
  Du denkst, dass sie in Zukunft gefordert werden. Kannst Du wirklich in Zukunft
  schauen?
- [Don't repeat yourself (a.k.a. DRY)][dry]: Vermeide doppelten Code innerhalb
  einer Komponente, eines VCS Repositories oder einem
  [bounded context][bounded-context], aber beachte die Regel
  [Rule of Three][rule-of-three].
- Die vier Prinzipien von [Objektorientierte Programmierung][oop]: Encapsulation
  (Datenkapselung), Abstraction (Abstraktion), Inheritance (Vererbung) und
  Polymorphism (Polymorphie)
- Automatisch generierter Code muss in der Regel _nicht_ den Coding Guidelines
  entsprechen. Wenn es dennoch möglich ist, den Code weitestgehend den
  Guidelines anzupassen, dann sollte man das machen. Code, der einmalig
  generiert wird, sollte immer angepasst werden.
  
Unabhängig davon, wie elegant etwas gelöst wurde, wenn es zu komplex für
_normale_ Entwickler ist, es zu ungewöhnlichen Verhalten führt oder es versucht
zukünftig Probleme zu lösen, dann ist es vermutlich die falsche Lösung und
sollte neu implementiert werden. Die schlechteste Reaktion eines Entwicklers,
wenn man ihn oder sie darauf aufmerksam macht, ist „But it works!“.

## Wie fange ich an?
- Bitte alle Entwickler dieses Dokument einmal aufmerksam und komplett zu lesen.
  Damit erhalten sie ein erstes Gespür für die hier enthaltenen Regeln.
- Stelle sicher, dass alle mit den Regeln einverstanden sind.
- Erstelle eine [Projekt Checklist][project-checklist] mit den für euch
  wichtigsten Punkten, die bei jeder der [Peer Review][peer-review] genutzt wird.
- Überlegt, ob ihr das Originaldokument forken wollt, um eure eigene Version
  zu erstellen.
- Nutzt Tools, z. B. IDEs, Compiler Plugins oder Buildtools, um die
  Guidelines einhalten zu können. Die meisten IDEs haben eine intelligente
  Code Inspection Engine, die, mit etwas Konfiguration,
  viele der Punkte abdecken kann.

## Inspiration
Dieses Dokument ist stark von den
[C# Coding Guidelines][csharp-coding-guidelines] beeinflusst.

Bereits in den letzten Jahren habe ich regelmäßig Codesytles oder Coding
Guidelines entwickelt und in meine Projekte, sowohl privat als auch beruflich,
eingeführt. Nun möchte ich dieses Wissen nutzen, um etwas allgemein gültiges
zu schreiben und der Masse zur Verfügung zu stellen.

## Handelt es sich hierbei um einen offiziellen Standard?
Nein! Es wird nicht erwartet, dass sich jedes Projekt an diesem Dokument
orientiert. Es soll eine Hilfestellung für jeden sein, der sich nicht selbst
damit beschäftigen möchte, aber dennoch innerhalb eines Teams, aber auch
über mehrere Teams hinweg, eine homogene Developerexperience haben möchte.

Um bei Entscheidungen zu helfen, welche Regeln wie wichtig sein können, habe ich
den Guidelines ein Empfehlungslevel beigefügt:

<img src="/img/1.png" alt="recommendation level 1" /> Guidelines, die Du in
allen Situationen anwenden solltest.

<img src="/img/2.png" alt="recommendation level 2" /> Dringend empfohlene
Guidelines.

<img src="/img/3.png" alt="recommendation level 1" /> Möglicherweise nicht in
allen Situationen anwendbar.


[pola]: https://en.wikipedia.org/wiki/Principle_of_least_astonishment
[kiss]: https://en.wikipedia.org/wiki/KISS_principle
[yagin]: https://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it
[dry]: https://en.wikipedia.org/wiki/Don%27t_repeat_yourself
[rule-of-three]: https://lostechies.com/derickbailey/2012/10/31/abstraction-the-rule-of-three/
[bounded-context]: https://martinfowler.com/bliki/BoundedContext.html
[oop]: https://en.wikipedia.org/wiki/Object-oriented_programming
[project-checklist]: https://www.continuousimprover.com/2010/03/alm-practices-5-checklists.html
[peer-review]: https://www.continuousimprover.com/2010/02/tfs-development-practices-part-2-peer.html
[csharp-coding-guidelines]: https://csharpcodingguidelines.com/
