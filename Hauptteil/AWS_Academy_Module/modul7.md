# Modul 7

## AWS EBS

Elastic Block Store ist die Disk einer EC2 Instanz. Ein EBS kann nur an einer EC2 Instanz gleichzeitig sein. Eine EC2 Instanz kann aber mehrere EBS Instanzen angehängt haben. Innerhalb einer Availability Zone werden EBS Instanzen automatisch repliziert.

Die Kosten für eine Instanz lassen sich anhand der provisionierten Grösse und dem spezifischen Typ berechnen. Eine SSD kostet mehr als eine HDD zum Beispiel.

## AWS S3

DerS3 Storage arbeitet mit sogenannten Buckets. In Buckets können Files abgelegt werden, mit einer Ordnertiefe von 0. Das heisst die Files befinden sich alle auf der obersten Ebene. Ein Bucket hat unbegrenzten Speicherplatz, ein File kann dabei maximal 5 TB gross sein.

S3 unterstützt Notifications für Uploads / Downloads, womit AWS Lambda Funktionen ausgeführt werden können.

Jeder Bucket muss einen einzigartigen Namen haben, da dieser Name für die URL benutzt wird, mit welcher der Bucket erreicht werden kann.

## AWS EFS

EFS ist ein Netzwerk File System, ähnlich wie NFS. NFS kann sogar als effektives Protokoll gewählt werden.

Der grosse Vorteil ist, dass mehrere Maschinen dieses File System gleichzeitig nutzen können.

EFS implementiert Mount Targets, welche sich in einem spezifischen Subnetz befinden und die Requests weiter routen.

Es gibt nur ein Mount Target pro Availabilty Zone. Das heisst, wenn eine Availabilty Zone mehrere Subnets hat, muss man entscheiden in welches Subnetz das Mount Target kommt.

## AWS S3 Glacier

Der S3 Glacier ist eine langfristige Datenbackup und Storagelösung. Man kann damit Daten langfristig zu tiefen Kosten in der Cloud speichern.

Ein Archive ist dabei der Content welcher gespeichert wird, der Vault ist der Bucket für den Glacier. Man kann definieren innert welcher Zeit man die Daten allenfalls wieder bruacht. Je höher die Holzeit, umso tiefer der Preis.

Einen S3 Glacier erstellt man in der AWS Console, anschliessend kann dieser aber nur noch über die SDKs oder die AWS CLI erreicht werden.

-----

[Zurück zum Unterverzeichnis](../README.md)

[Zum nächsten Modul](./modul8.md)
