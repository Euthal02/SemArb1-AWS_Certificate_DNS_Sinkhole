# 2.1.9 Modul 9

## AWS Well-Architected Framework Design Principles

Das AWS Well-Architected Framework ist ein Guide, mit welchem man eine Cloud Umgebung optimal designen und aufsetzen kann.

Es ist dabei in fünf Punkte unterteilt:

* Operational excellence
* Security
* Reliability
* Performance Efficiency
* Cost Optimization

Mehr zu diesen Punkten später.

### Operational Excellence

Der erste Punkte ist darauf ausgelegt, dass Cloud Systeme einen Business Value generieren, anstatt einfach nur "the Way to Go" zu sein.

Dies basiert auf fünf Prinzipien, welche es erleichtern sollen, den Punkt umzusetzen:

* Perform operations as code, unsere ganze Umgebung sollte soweit wie möglich mittels IaC Technologien als Code geschrieben werden.
* Make frequent, small, reversible changes, die ganze Umbegung sollte so aufgebaut werden, sodas man einzelne kleine Changes machen kann.
* Refine operations procedures frequently, ist ein Scrum Ansatz, in welchem man immer wieder zurückschaut und Möglichkeiten zur optimisierung wahrnimmt.
* Anticipate failure, immer vom schlimmsten Fall ausgehen und verschiedene Backups / Failover Methoden einsetzen.
* Learn from all operational failures

### Security

Der zweite Punkt ist darauf ausgelegt, Informationen, Systeme und Ressourcen zu  schützen.

* Implement a strong identity foundation, man sollte seine Umgebung mit einer zentralen Nutzerverwaltung einrichten und anschliessend die Rechte von diesem zentralen Punkt verteilen. Dies anhand Least Privilege.
* Enable traceability, jede Umgebung sollte gemonitored werden und alles alerten, was nicht Standardverhalten ist.
* Apply Security at all layers, es reicht nicht, wenn man nur auf Layer 5 eine Firewall einrichtet und alle darauf aufbauenden Services vernachlässigt. Jeder Layer sollte seine Securitymechanismen haben.
* Automate security best practices, hiermit ist gemeint, dass man möglichst nicht jedes Mal eine neue Securitygruppe aufsetzen muss, sondern vordefineirte Gruppen nutzen kann, oder das Aufsetzen automatisiert ist.
* Protect data in transit and at rest, Daten sollten sowohl bei der Speicherung wie auch bei der Übertragung geschützt und verschlüsselt sein.
* Keep people away from data, z.B. Abstrahierung der Datenbank, möglichst wenige Leute sollten direkt auf die Datenbank zugreifen können.
* Prepare for security events, sollte trotz alledem noch etwas passieren, sollten Abläufe vorbereitet sein, welche genau definieren was getan werden sollte.

### Reliability

Dieser Punkt wird genutzt um die Verfügbarkeit / Verlässlichkeit einer Cloud Umgebung zu verbessern.

* Automatically recover from failure, wenn ein gutes Monitoring existiert, kann eine Cloud Umgebung automatisch auf Events reagieren und vorprogrammierte Abläufe durchführen um diesen Failure zu beheben.
* Test recovery procedures, ähnlich wie beim Backup sollten Recovery Prcedures hin und wieder überprüft werden.
* Scale horizontally to increase aggregate workload availability, man sollte darauf verzichten einzelne Ressourcen immer wieder zu vergrössern und stattdessen mehr Ressourcen einsetzen. Dies verhindert ein Klumpenrisiko.
* Stop guessing capacity, die Ressourcen sollten genau gemonitort werden und bei Anzeichen von Überlastung sollte gehandelt werden, nicht erst beim Ausfall.
* Manage change in automation, so viel wie möglich sollte automatisiert werden.

### Performance Efficiency

Genutzte Ressourcen sollten effizient genutzt werden. Dadurch kann der Service besser angeboten werden und Kosten können gespart werden.

* Democratize advanced technologies, nicht jede Technologie muss von unserem Team im Griff sein. Man kann auch neuere Technoligen konsumieren und wie einen Service benutzen.
* Go global in minutes, anstatt manuell einen Service an einem anderen Ort aufzubauen kann man mit AWS innerhalb von Minuten weltweit Services zur Verfügung stellen.
* Use serverless architectures, wo immer möglich sollten PaaS und SaaS genutzt werden, anstatt IaaS und On-Premise. Das verhindert das Ressourcen intesive aufsetzen und verwalten von Betriebssystemen.
* Experiment more often
* Consider mechanical sympathy, man sollte immer die Technologie nutzen, welche am besten zu meinem Use-Case passt.

### Cost Optimization

Der "Cost Optimization" Punkt legt Fokus auf den Nutzen der kostengünstigsten Technologie.

* Adopt a consumption model, man sollte die Möglichkeit der Cloud nutzen, die Ressourcen anhand meines Loads zu scalen. Wenn man weiterhin versucht zukünftige Requirements zu erraten, wird man mehr Kosten haben, alseigentlich notwendig.
* Measure overall efficiency, wenn man die ganze Effizienz im Blick hat, also den Gewinn mit dem Aufwand konstant vergleicht, fallen Verbesserungen schneller auf und können besser gemessen werden.
* Stop spending money on undifferentiated heavy lifting, wie bereits öfters erwähnt, muss man mit AWS kein Datacenter mehr unterhalten und kann sich diese Kosten sparen.
* Analyze and attribute expenditure, wenn man zusätzlich noch die einzelnen Kostenpunkte im Griff hat, kann man einfacher Massnahmen ergreifen um diese Kostenpunkte zu senken.

## Reliability & High Availability

Die Verlässlichkeit eines System ist ein Messwerkzeug für die Messung ob ein System in der Lage ist, den Service zu liefern wann immer der Kunde dies möchte. Dies lässt sich mit dem MTBF (Mean time between failures) Wert beziffern. Nebst dem MTBF gibt es noch den Wert MTTF (Mean Time to Failure) und MTTR (Mean Time to Repair). MTTR und MTTF zusammengerechnet ergibt den MTBF.

Um die Verfügbarkeit eines System zu beziffern, nehmen wir die Gesamtlaufzeit des Systems und vergleichen diese mit der eigentlichen Zeit in welcher das Programm lief. Dieser Wet sollte möglichst nah bei 100% sein. Je näher an 100% dieser ist, um so verlässlicher ist unser Service. Abgekürzt wird dies meist mit der "Number of 9s", also fünf 9s wären 99.999% Verfügbarkeit.

## AWS Trusted Advisors

Mit dem Well-Architected Framework Design Prinzip hat man ein statisches Handbuch um eine "Best Practice" Cloud Umgebung aufzubauen. Mit dem Trusted Advisor kann man dynamische Feedbacks erhalten und Verbesserungsvorschläge anschauen. Diese sind in 5 Kategorien eingeteilt.

* Cost Optimization
* Performance
* Security
* Fault Tolerance
* Service Limits

-----

[2.1.10 Erfahrungen Modul 10](./modul10.md)

[Zurück zum Unterverzeichnis](../README.md)
