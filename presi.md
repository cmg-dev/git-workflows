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

**systeme**

1. CI-Server
1. Build-Server/ Test-Server
1. Ticket-System - Support
1. Entwicklung

**Personen**
1. Entwickler
1. Reviewer
1. Produkt Owner
1. Kunde
]

---
class: center, top
background-image: url(img/s1_map.png)

### Landschaft


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

-> Beliebt im Enterprise Umfeld

Häufig bei cloesd Source Projekten 

]

---
class:
background-image: url(background.png)

.right_column[

### Workflow Typen

**Beispiel dezentraler Workflow**

1. Kernel Entwicklung
2. Public-Repository (Pull-Requests)

-> de facto Standard bei OpenSource Projekten

]

---
class:
background-image: url(img/s3_DIC_wf.png)

.right_column_small[

### Dezentraler Workflow - Beispiel

**Diktator Workflow**

Entwickler -> Leutnants -> Diktator -> Repo

* Alle *pullen* von zentraler Quelle
* Nur *Diktator* hat *push* rechte
* Arbeiten mit Pull-Requests/ Mailing List
]

---
class:
background-image: url(img/s2_IM_wf.png)

.right_column_small[

### Dezentraler Workflow - Beispiel

**Integration Manager Workflow**

* IM *pullt* aus öffentlichen Entwickler Repos
* Entwickler *pushen* in ihr öffentliches Repo
* IM hat Berechtigung *push* Berechtigung
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

Das einfachste Umfeld ist wahrscheinlich das ein bis zwei Entwickler an einem privaten Projekt arbeiten. *Privat* bedeutet hier, *Closed Source*.

Alle Entwickler haben *push*-Rechte zu dem Repository.

Dieser Workflow entspricht denen anderer zentralisierten Systeme (SVN...)

Allerdings hat man die Vorteile von git. 
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

Mehrere Entwickler arbeiten agil zusammen. Entwickler können Teams wechseln und an verschiedenen Stellen arbeiten.

Es gibt Regeln für die Zusammenarbeit.

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

Ein etwas realistischerer Workflow (mehr als ein Team, >10 Entwickler)

* Kann zentral und dezentral sein
* Späte Zusammenführung von Änderungen verschiedener Teams

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

## Start eines Workflows

---
class:
background-image: url(background.png)

.right_column[

### Start eines Workflows

Wie **startet** ein Branch

* feature
* hotfix
* support

Einem Branch sollte immer einem *Tracking* unterliegen. Bspw. ein Ticket oder eine User-Story.
]

---
class:
background-image: url(background.png)

.right_column[

### Start eines Workflows

Wie **endet** ein Branch

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
class:
background-image: url(background.png)

.right_column[

### Ende eines Workflows

Tests erfolgreich!
-> Code Review

]

---
class: middle, center
background-image: url(background.png)

## Code Reviews

---
class:
background-image: url(background.png)

.right_column[

### Code Reviews

[Code Reviews](http://blogs.atlassian.com/2014/03/every-team-needs-kick-ass-code-reviews/)
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

Entwickler

Reviewer

]

---
class: middle, center
background-image: url(background.png)

## Vorstellung spezieller Workflows

---
class:
background-image: url(background.png)

.right_column[

### git-Workflow Allgemein

Viele Arbeitsgruppen wechseln zu git, weil sie dir Fähigkeit suchen mit vielen Teams parallel zu arbeiten und 
zu verschiedenen Zeitpunkten (meist spät im Entwicklungsprozess) die Änderungen zusammen zu führen.

Many groups switch to Git because of this ability to have multiple teams working in parallel, merging the different lines of work late in the process. The ability of smaller subgroups of a team to collaborate via remote branches without necessarily having to involve or impede the entire team is a huge benefit of Git. The sequence for the workflow you saw here is something like this:
]

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

.example_page[

#### GitHub- Workflow Zusammenfassung

Aufbauend auf Pull Requests.
]

---
class: center, middle
background-image: url(background.png)

## Stash_Workflow

---
class: center, top
background-image: url(img/s8_Stash_wf.png)

### Stash_Workflow 

---
class:
background-image: url(background.png)

.example_page[

#### Stash_Workflow Zusammenfassung

* Der master-Zweig wird stabil gehalten, nicht aber in Produktionsqualität wie beim GitHub-Workflow
* Die Qualität bzw. Buildstabilität schwankt zwischen „Alpha“ und „Release Candidate“. Unterstützt wird dies durch den Einsatz von branch-aware Continous Integration, automatischer Testabdeckung und Performance-Monitoring der Buildresultate.
* Pro User Story ein Zweig (wird von master aus erstellt)
* Pro Release ein Zweig
* Pro Bugfix ein Zweig (automatisch zurück integriert in Release-Zweig)
* Pull Requests werden für fertige Implementierungen erstellt und nach einem erfolgten Code Review durch mindestens zwei Team-Mitglieder in den master-Zweig aufgenommen.
]

---
class: center, middle
background-image: url(background.png)

## git-flow Workflow 

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

* develop: Enthält die zurzeit in Entwicklung befindliche Codebasis. Aktuellster Stand immer im zentralen Repo.
* master: Enthält Snapshots von stabilen (= getesteten, gereviewten) Ständen der Codebasis. Aktuellster Stand ist immer im zentralen Repo.

Temporäre Branches:
* Feature-Branches: Werden vom Entwickler erstellt, z.B. wenn ein Ticket, welches ein Feature beschreibt, bearbeitet wird. Abgeschlossene Arbeiten werden nach develop gemerged
* Release-Branches: Werden von develop gebranched und enthalten den Veröffentlichungskandidaten. In Release-Branches werden keine neuen Features implementiert, sondern nur noch Fehler ausgemerzt und die Codebasis nochmals intensiv getestet.

]

---
class:
background-image: url(background.png)

.right_column[

### git-flow Workflow 

Vorstellung von [git flow](http://5minds.github.io/git-flow-bestpractice)
]

---
class: center, middle
background-image: url(background.png)

## git Workflows - Best Practice

---
class:
background-image: url(img/s10_SemVer.png)

.right_column[

### Semantic Versioning

Verwendung von *Semantic Verwendung* für Releasekennzeichnun.

Bei einer Versionsnummer der Art MAJOR.MINOR.PATCH, bedeuten:

* **MAJOR** Version, die inkompatible Änderungen beinhaltet
* **MINOR** Inkrement, wenn Änderungen abwärtskompatibel
* **PATCH** Erhöhung, wenn abwärtskompatibler Bugfix

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

