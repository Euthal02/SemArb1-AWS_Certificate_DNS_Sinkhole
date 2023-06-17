# Modul 10

## Elastic Load Balancing

Elastic Loadbalancing ist die InHouse Lösung für eine HA Umgebung. Man kann damit hinter einem Endpunkt mehrere Amazon Services aggregieren.

Unterschieden wird zwischen drei Typen:

* Application Load Balancer, Traffic wird auf Layer 7 verteilt. Hauptsächlich für HTTP und HTTPS gedacht.
* Network Load Balancer, Traffic wird auf Layer 4 verteilt. Für jegliche Services auf IP Basis gedacht.
* Classic Load Balancer, welcher beides kann.

Der Service integriert sich mit CloudWatch, womit ein gutes Monitoring gegeben ist.

## Amazon CloudWatch

CloudWatch ist der integrierte Monitoring-Service von AWS. Er sammelt Metric Daten und speichert diese zentral ab.

Anhand dieser Daten können dann Alerts generiert werden und via Amazon SNS (Simple Notification Service) versendet werden.

Es können auch eigene Metrics erstellt und abgefüllt werden, mit welchen man anschliessend auch Auswertungen machen kann.

## Amazon EC2 Auto Scaling

Mit Auto Scaling können EC2 Instanzen automatisch am Load angepasst werden. Je nach Load können zusätzliche EC2 Instanzen kreiert oder gelöscht werden.

Pro Auto Scaling Group werden drei Werte gesetzt. Die minimale Anzahl, die gewollte Anzahl und die maximale Anzahl Server. 

Innerhalb dieser Werte kann Auto Scaling Server erstellen und löschen. Wenn neue Server erstellt werden müssen, nutzt Auto Scaling dazu eine Launch Configuration.

Darin kann unter anderem mit einem AMI gearbeitet werden, welche den Service bereits vorkonfiguriert. 

Auto Scaling kann unter anderem mittels CloudWatch getriggert werden, wenn z.B. die CPU Werte einer Auto Scaling Group überdurchschnittlich hoch sind.



-----

[Zurück zum Unterverzeichnis](../README.md)
