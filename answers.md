### Welche Vorteile ein Kubernetes Deployment gegenüber einem Kubernetes Pod hat

Kubernetes Deployments gewährleistet eine Hochverfügbarkeit, da Deployments kontinuierlich überwachen und fehlgeschlagene Pods ersetzen, um den gewünschten Zustand aufrechtzuerhalten. Im Gegensatz dazu können Pods bei Knotenausfällen oder Ressourcenüberlastung nur beendet werden. Ein weiterer Vorteil von Kubernetes Deployments, ist das Ermöglichen einer dynamischen Skalierung und Aktualisierung von Anwendungen. Dadurch wird eine hohe Widerstandsfähigkeit und Verfügbarkeit gewährleistet. Außerdem bieten Deployments Funktionen für Rolling Updates ohne Ausfallzeiten oder Rollbacks, falls etwas schief geht. Es ist möglich, Updates durchzuführen, ohne dass der Service unterbrochen wird.

### Wofür ein Kubernetes Service gut ist

Ein Kubernetes Service ist eine Abstraktion, die es Pods ermöglicht, in Kubernetes zu sterben und sich zu replizieren, ohne die Anwendung zu beeinträchtigen. Somit ist der Service für die Erkennung und das Routing zwischen abhängigen Pods (zum Beispiel Frontend- und Backend-Komponenten in einer Anwendung) zuständig. Das heißt, das der Service eine logische Menge von Pods definiert und die Offenlegung des externen Datenverkehrs, Lastverteilung und Diensterkennung für diese Pods ermöglicht. 

### Mehrere Wege wie man eine Kubernetes Anwendung von außen erreichen kann

Ein Weg ist über Ingress, welches den externen Zugriff auf Dienste im Cluster ermöglicht. Es kann LoadBalancer, SSL und ein benutzerdefiniertes Routing bereitstellen. Eine Ingress-Ressource wird verwendet, um Web-Traffic in das Kubernetes Cluster zu leiten, beispielsweise zu einem Service. Eine weitere Möglichkeit ist über einen NodePort, der auf jedem Knoten auf einem bestimmten Port (30000-32767) lauscht und diesen Verkehr an einen Dienst innerhalb des Clusters weiterleitet. 