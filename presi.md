class: middle, center
background-image: url(background-intro.png)

# git workflows

---
class: middle, center
background-image: url(background.png)

## Ziele

---
class:
background-image: url(background.png)

.right_column[
### Ziele

git Workflows sollen

* die Projektstruktur unterstützen
* die Flexibilität von git nutzen
* die Qualität des Codes verbessern
* zur Sicherheit der Entwickler beitragen
* Wissenstransfer ermöglichen
* die Akzeptanz von VCS steigern
* Agilität fördern
]

---
class: middle, center
background-image: url(background.png)

## Landschaft

---
class:
background-image: url(background.png)

.right_column[

### Landschaft

**Systeme**

1. CI-Server
1. Build-Server/ Test-Server
1. Ticket-System - Support
1. Entwicklung

**Personen**
1. Entwickler
1. Reviewer
1. Product Owner
1. Kunde
]

---
class: center, top
background-image: url(img/s1_map.png)

### Landschaft

---
class:
background-image: url(background.png)

.right_column[

### git-Workflow Allgemein

Viele Arbeitsgruppen wechseln zu git, weil sie die Fähigkeit suchen mit vielen Teams parallel zu arbeiten und 
zu verschiedenen Zeitpunkten (meist spät im Entwicklungsprozess) die Änderungen zusammen zu führen.
]

---
class: middle, center
background-image: url(background.png)

## Workflow Typen

---
class:
background-image: url(background.png)

.right_column[

### Workflow Typen

git ist Flexibel. Die Workflows auch:

* Zentralisiert
* Verteilt
* Baumartig
* Silos
* Wenige/Viele Entwickler
* Gemischte Domänen (Hard-/ Software)

Gerne werden Aspekte kombiniert.
]

---
class:
background-image: url(background.png)

.right_column[

### Workflow Typen

**Beispiel zentraler Workflow**

1. git flow
2. Stash

-> beliebt im Enterprise Umfeld

Häufig bei *Closed Source*-Projekten anzutreffen

]

---
class:
background-image: url(background.png)

.right_column[

### Workflow Typen

**Beispiel dezentraler Workflow**

1. Kernel Entwicklung
2. Public-Repository (Pull-Requests)

-> de facto Standard bei *Open Source*-Projekten

]

---
class:
background-image: url(img/s3_DIC_wf.png)

.right_column_small[

### Dezentraler Workflow - Beispiel

**Diktator Workflow**

Entwickler -> Leutnants -> Diktator -> Repository

* Alle *pullen* von zentraler Quelle
* Nur *Diktator* hat *push* Rechte
* Arbeiten mit Pull-Requests/ Mailing List
]

---
class:
background-image: url(img/s2_IM_wf.png)

.right_column_small[

### Dezentraler Workflow - Beispiel

**Integration Manager Workflow**

* IM *pullt* aus öffentlichen Entwickler Repositories
* Entwickler *pushen* in ihr öffentliches Repository
* IM hat *push* Berechtigung
]

---
class: center, middle
background-image: url(background.png)

## Basic Workflows

---
class:
background-image: url(background.png)

.right_column[

### Basic Workflows

**Einfaches Team**

Das einfachste Umfeld ist das ein bis zwei Entwickler an einem privaten Projekt arbeiten. *Privat* bedeutet hier, *Closed Source*.

* Alle Entwickler haben *push*-Rechte zum Repository

* Dieser Workflow entspricht denen anderer zentralisierten Systeme

* Allerdings hat man die Vorteile von git (einfaches branching/ merging)
]

---
class:
background-image: url(img/s5_wf_private-developer.png)

.right_column[

### Basic Workflows

**Einfaches Team**

* Alice und Bob arbeiten für sich

* keine Vorgaben/ Regeln zum *commit*/*push*/*merge*- Verhalten
]

---
class:
background-image: url(background.png)

.right_column[

### Basic Workflows

**Kleines Managed Team**

Nach einem *Einfachen Team* ist dieser Workflow der nächst einfache.

* Mehrere Entwickler arbeiten agil zusammen
* Entwickler können Teams wechseln und an verschiedenen Stellen arbeiten.
* Es gibt Regeln für die Zusammenarbeit.
]

---
class:
background-image: url(img/s6_wf_managed-team.png)

.left_column_wide[

### Basic Workflows

**Kleines Managed Team**

* mehrere Entwickler
* Branch-Based
* *fetch*-first
* jeder hat *push*-Berechtigung
]

---
class:
background-image: url(background.png)

.right_column[

### Basic Workflows

**Forked Public Project**

Ein realistischerer Workflow (mehr als ein Team, >10 Entwickler)

* Kann zentral und dezentral sein
* Späte Zusammenführung der Änderungen verschiedener Teams

Nachteile:

* Kann Probleme mit der Stabilität hervorrufen

]

---
class: center, top
background-image: url(img/s4_WF_goodness.png)

### Forked Public Project

---
class: middle, center
background-image: url(background.png)

## Entwicklung

---
class: center, top
background-image: url(img/s1_1_map_Dev.png)

## Entwicklung

---
class: middle, center
background-image: url(background.png)

## Start eines Workflows

---
class:
background-image: url(background.png)

.right_column[

### Start eines Workflows

Wie **startet** ein Branch?

* feature
* hotfix
* support

Einem Branch sollte immer einem *Tracking* unterliegen. Beispielsweise ein Ticket oder eine User-Story zu der Änderung.

Im Tracking sind die Anforderungen/ Vorgaben hinterlegt, die umzusetzen sind.
]

---
class:
background-image: url(background.png)

.right_column[

### Start eines Workflows

Wie **endet** ein Branch?

* develop
* master
  * release

Ein Branch endet, wenn die Vorgaben aus dem Ticket/ User-Story/ etc. erfüllt sind. 

Dann werden die Änderungen in andere Branches übernommen.
]

---
class: middle, center
background-image: url(background.png)

## Ende eines Workflows

---
class: center, top
background-image: url(img/s1_1_map_test.png)

## Tests

---
class:
background-image: url(background.png)

.right_column[

### Ende der Tests 

Tests erfolgreich!
-> Peer Review
]

---
class: middle, center
background-image: url(img/s10_peer_review.jpg)

---
class:
background-image: url(background.png)

.right_column[

### Peer Reviews

**Wer?**

1. Ein Erfahrener Entwickler
2. Die Verantwortlichen für die Entwicklung

Faustregel: **nicht mehr** als 3 Entwickler

]

---
class:
background-image: url(background.png)

.right_column[

### Peer Reviews

**Warum**?

1. Wissenstransfer
2. Qualitätssicherung 

[Peer Reviews](http://blogs.atlassian.com/2014/03/every-team-needs-kick-ass-code-reviews/)
]

---
class:
background-image: url(background.png)

.right_column[

### Peer Reviews

**Wie?**

Dabei laufen verschiedene Qualitätsprozesse ab:

* Der Entwickler entdeckt selbst Verbesserungen
* Der Reviewer stellt Verständnisfragen 
* Der Reviewer entdeckt Verbesserungsmöglichkeiten
* Der Reviewer empfiehlt diese dem Programmierer
]

---
class:
background-image: url(background.png)

.right_column[

### Peer Reviews

**Wie?**

Der Reviewer muss dabei folgendes beachten:

* Es geht nicht um *Zeigefinger*
* Vermeidung von: "Das ist Falsch!"; "Das verstößt gegen die Konventionen"
* besser: "Warum wurde das so umgesetzt?"; "Ist das problematisch?";
  "Können wir das besser?"
* Hilfestellung geben
* Teamgefühl stärken
]

---
class: center, middle
background-image: url(background.png)

### Peer Reviews - Tools

---
class: center, top
background-image: url(img/s14_diff.jpg)


### Peer Reviews - Tools
---
class:
background-image: url(background.png)

.right_column[

### Peer Reviews - Tools

* [OS X Tools](http://www.git-tower.com/blog/diff-tools-mac/)
* [Übersicht](https://en.wikipedia.org/w/index.php?title=Comparison_of_file_comparison_tools&oldid=691537231)
]

---
class: middle, center
background-image: url(background.png)

## Pull Requests

---
class:
background-image: url(background.png)

.right_column[

### Pull Requests

Eine Möglichkeit für Entwickler ohne *pusch*-Berechtigung, Änderungen mit Anderen zu teilen.

Viele Möglichkeiten:

* Mailingliste
* Webseiten
* Portale
* ...

]

---
class: middle, center
background-image: url(background.png)

## Pull Request - Beispiel

---
class: middle, center
background-image: url(background.png)

## Vorstellung spezieller Workflows

---
class: center, middle
background-image: url(background.png)

## GitHub- Workflow

---
class: top, center
background-image: url(img/s7_GH_wf.png)

### GitHub- Workflow 

---
class:
background-image: url(background.png)

.right_column[

#### GitHub-Workflow Zusammenfassung

* aufbauend auf Pull Requests.
* simpel
* automatisches Deployment
* keine Unterteilung der *feature*-Branches
]

---
class: center, middle
background-image: url(background.png)

## Stash Workflow

---
class: center, top
background-image: url(img/s8_Stash_wf.png)

### Stash Workflow 

---
class:
background-image: url(background.png)

.right_column[

#### Stash Workflow Zusammenfassung

* Der master-Zweig wird stabil gehalten, nicht aber in Produktionsqualität 
* Die Qualität bzw. Buildstabilität schwankt zwischen *Alpha* und 
  *Release Candidate*
* Pro User Story ein Zweig 
* Pro Release ein Zweig
* Pro Bugfix ein Zweig (automatisch zurück integriert in Release-Zweig)
* Pull Requests werden für fertige Implementierungen erstellt und nach Peer Review übernommen 
]

---
class: center, middle
background-image: url(img/s11_flow_start.jpg)

---
class: center, top
background-image: url(img/s9_GF_wf.png)

### git-flow Workflow 

---
class:
background-image: url(background.png)

.example_page[

#### git-flow Workflow Zusammenfassung 


Dauerhafte Zweige:

* **develop**: Enthält die zurzeit in Entwicklung befindliche Codebasis 
* **master**. Enthält Snapshots von stabilen (= getesteten, gereviewten) Ständen der Software

Temporäre Branches:

* **feature**-Branches: Werden vom Entwickler erstellt (z.B. wenn ein Ticket bearbeitet wird)
* **release**-Branches: Werden von develop gebrancht und enthalten den Veröffentlichungskandidaten

Eine gute Praxis: Im *release*-Branch werden keine neuen Features implementiert, sondern nur noch Fehler ausgemerzt und die Codebasis nochmals intensiv getestet.

]

---
class:
background-image: url(background.png)

.right_column[

### git-flow Workflow 

Detailierte Vorstellung von [git flow](http://cmg-dev.github.io/git-flow-bestpractice)
]

---
class: center, middle
background-image: url(img/s13_flow_finish.jpg)

---
class: center, middle
background-image: url(img/s12_best_practice.jpg)


---
class:
background-image: url(img/s10_SemVer.png)

.right_column[

### Semantic Versioning

Verwendung von *SemVer* für Releasekennzeichnun.

Bei einer Versionsnummer der Art MAJOR.MINOR.PATCH, bedeuten:

* **MAJOR** Version, die inkompatible Änderungen beinhaltet
* **MINOR** Inkrement, wenn Änderungen abwärtskompatibel
* **PATCH** Inkrement, wenn abwärtskompatibler Bugfix

Zusätzliche Label sind als Erweiterung verfügbar zum MAJOR.MINOR.PATCH- Format
]

---
class:
background-image: url(background.png)

.right_column[

### git-flow 

[git-flow](https://github.com/nvie/gitflow) Verwenden!

Leistungsstarke Abläufe und Tool für eine auf git basierende Entwicklung. 
Eine Beschreibung und Erklärung gibt der [Autor](http://nvie.com/posts/a-successful-git-branching-model) selbst.

Eine [git-flow Einführung](http://5minds.github.io/git-flow-bestpractice).

]

