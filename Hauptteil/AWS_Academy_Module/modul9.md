# Modul 9

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



-----

[Zurück zum Unterverzeichnis](../README.md)
