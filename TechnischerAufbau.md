# Technischer Aufbau

## Server

Google Cloud hat zahlreiche Serverfarmen, verteilt auf der ganzen Welt, mit Ausnahme von Afrika. Speziell in Europa und Nordamerika kann man sehr viele dieser Farmen finden.

![server_standorte](server_standorte.png)

## SPI Model

Das SPI Model lässt sich in die 3 Teile IaaS (Infrastructure as a Service), PaaS (Planform as a Service) und SaaS (Software as a Service) aufteilen. Dienste in allen 3 Bereichen kann man in der Google Cloud finden.

### IaaS

Die grundlegende Ebene des Cloud-Computings ist IaaS, denn hier werden Hardware-Ressourcen in virtualisierter Form bereitgestellt. Ob Speicherplatz, Prozessoren oder Netzwerk – alle Recheninstanzen können in beliebiger Menge hinzugefügt und auch wieder entfernt werden. Manchmal wird deswegen auch von einem virtuellen Rechenzentrum (Virtual Data-Center) gesprochen.

Bei IaaS kommen die Kostenvorteile des Cloud-Computings wohl am deutlichsten zum Tragen: Gerade Hardware ist in der Anschaffung sehr teuer, veraltet schnell und sollte zudem unter besonders gesicherten Bedingungen (Stichwort: Rechenzentrum vs. Unternehmenskeller) aufgestellt werden. Findet die Bereitstellung der IT-Ressourcen virtualisiert und bedarfsgerecht statt, sparen Anwender in der Regel enorm.



### PaaS

PaaS ist das Bindeglied zwischen IaaS und SaaS und ermöglicht erst das Zusammenspiel der beiden anderen Ebenen. Denn auf der Plattformebene werden die Entwicklungs- und Laufzeitumgebungen für Software bereitgestellt, aufbauend auf IaaS-Ressourcen wie etwa Betriebssystemen. Die anderen beiden Ebenen IaaS und SaaS werden in der Regel durch APIs angesprochen. Für PaaS interessieren sich demzufolge vor allem Software-Entwickler.



### SaaS

SaaS geht noch einen Schritt weiter: Alles ist über das Web verfügbar. Der Anbieter hostet, verwaltet und liefert die gesamte Infrastruktur inklusive Anwendungen. Die Benutzer melden sich einfach in der Cloud an, um auf die als Service bereit gestellten Ressourcen zuzugreifen. Solche Service können eine Anwendungssoftware oder IT-Lösungen wie z.B. Backup- und Recovery-Tools sein.

Eine weitere Möglichkeit, durch das vielfältige Angebot an Lösungen der Google Cloud Platform zu navigieren, ist die Auswahl von Services. Zu den wichtigsten Kategorien an Services gehören:

* Compute Leistung
* Computer Vernetzung
* Datenspeicher und Datenbanken
* Künstliche Intelligenz und Machine Learning
* Big Data
* Identifizierung und Sicherheit
* Management Tools

Die wichtigsten Dienstleistungen im Bereich SaaS sind:

|      Compute       |          Networking           |    Storage & Databases    |        AI & ML         |    Big Data     |  Identity & Security   |     Management Tools     |
| :----------------: | :---------------------------: | :-----------------------: | :--------------------: | :-------------: | :--------------------: | :----------------------: |
|  Computer Engine   | Google Cloud  Virtual Network |       Cloud Storage       | Cloud Machine Learning |    Big Query    |    Google Cloud IAM    |       Stackdriver        |
|     App Engine     |     Cloud Load Balancing      |         Cloud SQL         |    Cloud Vision API    | Cloud Dataflow  | Cloud Resource Manager |    Deployment Manager    |
|  Container Engine  |           Cloud CDN           |         Bigtable          |    Cloud Speech API    |    Dataproc     | Cloud Security Scanner |       Cloud Shell        |
| Container Registry |   Google Cloud Interconnect   |      Cloud Datastore      |  Natural Language API  | Cloud  Datalab  |                        | Google Cloud Billing API |
|  Cloud Functions   |           Cloud DNS           |       Cloud Spanner       |     Translate API      | Google Genomics |                        |                          |
|   Cloud Pub/Sub    |                               |      Persistant Disk      |                        |                 |                        |                          |
|                    |                               | Cloud Source Repositories |                        |                 |                        |                          |

#### Kubernetes

| Entwicklung von Anwendungen beschleunigen, ohne die Sicherheit zu gefährden |          Vorgänge mit Release- Versionen optimieren          |    Vorgänge am 2. Tag mithilfe von Google SREs reduzieren    |
| :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| Entwickeln Sie unterschiedlichste Anwendungen, die Unterstützung für zustandsorientierte, serverlose und Anwendungsbeschleuniger bieten. Sichern und beschleunigen Sie mit Kubernetes-eigenen CI/CD-Tools jede Phase des Erstellungs- und Bereitstellungszyklus. | Wählen Sie die Release-Version, die Ihren Unternehmensanforderungen entspricht. Schnelle, regelmäßige und stabile Release-Versionen haben unterschiedliche Rhythmen für Knoten-Upgrades und bieten Supportstufen, die der jeweiligen Version entsprechen. | Dank der Site Reliability Engineers (SREs) von Google sparen Sie Zeit und können sich ganz auf Ihre Anwendungen konzentrieren. Unsere SREs haben Ihren Cluster und seine Computing-, Netzwerk- und Speicherressourcen ständig im Blick. |

Quelle: https://cloud.google.com/kubernetes-engine

Google Kubernetes bietet 2 Betriebsarten:

* Standard: Bei dieser Form werden alle Container vom Benutzer verwaltet und administriert. Der Benutzer kann neue Container erstellen und diese auch wieder löschen, wenn sie nicht mehr benötigt werden
* Autopilot: Beim Autopilot haben die Benutzer keinen Zugriff auf die Verwaltung der Container. Der Modus übernimmt die komplette Verwaltung der Clusterinfrastruktur, ohne dass sich der Nutzer um Monitoring und konfigurieren kümmern muss.

#### Anthos

Doch Google Kubernetes selbst ist heutzutage nicht mehr für alle "der Way to go". Google hat mittlerweile einen viel umfangreicheren Dienst, der viele der altbekannten Dienste zu einem kombiniert, nämlicht Anthos Vorteile von Anthos:

|                Anwendungen überall verwalten                 |               Software schneller bereitstellen               |         Anwendungen und Softwarelieferkette schützen         |
| :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| Anthos ist eine verwaltete  Plattform für alle Ihre  Anwendungs-Deployments,  sowohl traditionelle als auch  cloudnative. Sie können damit  globale Flotten aufbauen und  verwalten sowie Betriebskonsistenz  übergreifend über diese schaffen. | Mit cloudnativen Tools und Anleitungen von Google können Sie die Produktivität Ihrer Entwickler und die Softwarebereitstellung beschleunigen, indem Sie die Vorteile von Cloud-Dienste, Container und serverloses Computing übergreifend für Ihre Bereitstellungen nutzen. | Sicherheit wird mit Anthos in jeder Phase des Lebenszyklus von Anwendungen integriert, d. h. während der Entwicklung, Erstellung und Ausführung. Die Sicherheits- und Richtlinienverwaltung erfolgt für alle Ihre Deployments automatisch. |

Quelle: https://cloud.google.com/anthos?hl=de

Mit diesem System umgeht Google das Problem, dass manche Anwendungen nicht mit allen Systemumgebungen kompatibel sind. Google beschreibt Anthos wie folgt: "Anthos ist eine offene Hybrid- und Multi-Cloud-Plattform, auf der Sie bestehende Anwendungen modernisieren, neue entwickeln und diese überall sicher ausführen können. Anthos basiert auf Open-Source-Technologien, die von Google federführend entwickelt wurden, darunter Kubernetes, Istio und Knative." Somit spart man sich die Anwendung vieler kleinerer Cloud Dienste und vereint sie somit zu einem Dienst.



