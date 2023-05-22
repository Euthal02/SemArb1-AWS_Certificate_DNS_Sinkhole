# Modul 5

Ich persönlich würde mein Wissen bezüglich Networking als Fortgeschritten bezeichnen und daher werde ich in diesem Modul nicht allzu viel bezüglich Subnetting oder sonstigen Network Basics schreiben.

## Amazon VPC

VPC bedeutet Virtual Private Cloud. Amazon bietet mit diesem Produkt ein virtualisiertes Netzwerk in der ausgewählten Region an.

Server können innerhalb dieses Netzwerks miteinander kommunizieren und es bietet einige weitere Features eines normalen Netzwerks.

Ein VPCkann sich nur in einer Region befinden. Mehrere Regionen werden nicht unterstützt. Innerhalb eines VPC können mehrere Subnets koexistieren und mehrere Gateways bestimmen das Routing.

Jedes Subnet kann nur auf einer Availabilty Zone gleichzeitig sein. Diese können als Public oder auch als Private Netz konfiguriert werden.

Beim erstellen eines VPC muss man einen CIDR Range angeben. Dieser CIDR Range kann nach dem erstellen nicht geändert werden.

Die Grösse des CIDR Range kann zwischen /16 und /28 sein. Also zwischen 65'536 und 16 IP Addressen.

Öffentliche IP Adressen kann man entweder mit Elastic IPs an den Servern assignen, oder man fügt die Server in eine öffentliches Netz hinzu und sie werden automatisch eine öffentliche zugeteilt bekommen.

Elastic IPs kommen immer mit Elastic Network Interfaces, welche zwischen Maschinen hin und her gemoved werden können.

## VPC Networking

NAT Gateways erlauben Server, welche nur in privaten Netzwerken sind, eine Connection ins Internet herzustellen. Diese müssen immer in einem öffentlichen Subnetz stehen und sind mittels Routing auch für die Clients in Privaten Netzwerken verfügbar.

Internet Gateways sind dazu da, für Public IP Netzwerke den nächsten Hop bereitzustellen. Von dort aus können sie dann mit ihrer IP Adresse ins Internet.

VPC können mit anderen Accounts geteilt werden. So dass andere Maschinen von einem anderen AWS Kunden im gleichen Subnet sind. Diese Accounts müssen dazu aber in der selben [Organisation](modul2.md#aws-organizations) sein.

VPC Peering erlaubt das Routing zwischen zwei separaten VPC, ohne dass diese in der gleichen Organisation sind. Das Peering ist NICHT auf die Region beschränkt.

## VPC Security



-----

[Zurück zum Unterverzeichnis](../README.md)
