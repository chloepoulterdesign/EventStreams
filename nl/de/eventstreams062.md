---

copyright:
  years: 2015, 2019
lastupdated: "2019-01-14"

keywords: IBM Event Streams, Kafka as a service, managed Apache Kafka

subcollection: eventstreams

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}

# Kafka-Client zur Verwendung mit {{site.data.keyword.messagehub}} auswählen
{: #kafka_clients}

Wenn Sie die Kafka-API mit {{site.data.keyword.messagehub}} verwenden möchten, wählen Sie einen der folgenden Clienttypen aus:

* Der offizielle Java-Client. Dieser stellt die am besten geeignete Option dar, da er die neuesten für Apache Kafka verfügbaren Features enthält.
* Einen der [empfohlenen Clients anderer Anbieter](/docs/services/EventStreams?topic=eventstreams-kafka_clients#clients_table).

Für beide Clienttypen sollte stets die neueste Clientversion ausgewählt werden. 
{: shortdesc}

## Clientvoraussetzungen für die Verbindung mit Event Streams

Für eine Verbindung mit {{site.data.keyword.messagehub}} müssen Clients die Authentifizierung mit dem SASL Plain-Mechanismus unterstützen und die SNI-Erweiterung (Server Name Indication) für das TLSv1.2-Protokoll verwenden.

Die Mindestversion des Kafka-Protokolls, die unterstützt wird, ist 0.10.

	
## Clients anderer Anbieter
{: #third_party_clients}

Wenn Sie die offiziellen Java-Clients nicht ausführen können, sollten Sie einen der [empfohlenen Clients anderer Anbieter](/docs/services/EventStreams?topic=eventstreams-kafka_clients#clients_table) ausführen, die alle mit {{site.data.keyword.messagehub}} getestet wurden. 

Möglicherweise können weitere Clients anderer Anbieter, die die Mindestanforderungen für Clients unterstützen, mit {{site.data.keyword.messagehub}} eingesetzt werden. Die durchgeführten Test und die vorhandenen Erfahrungen beziehen sich jedoch ausschließlich auf die empfohlenen Clients anderer Anbieter.

## Zusammenfassung der Unterstützung für alle empfohlenen Clients
{: #client_summary}

<table id="clients_table">
    <caption>Tabelle 2. Zusammenfassung der Clientunterstützung</caption>
      <tr>
		    <th id="client" scope="col">Client</th>
		    <th id="language" scope="col">Sprache</th>
			<th id="version" scope="col">Empfohlene Version</th>
		    <th id="minimum version" scope="col">Unterstützte Mindestversion [<sup>1</sup>](/docs/services/EventStreams?topic=eventstreams-kafka_clients#footnote1)</th>
			<th id="sample link" scope="col">Link zum Beispiel</th>
        </tr>
			<tr>
			<td colspan="3">**Offizieller Client**</td>
			</tr>
	  		<tr>
			<td>[Apache Kafka-Client ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://kafka.apache.org/downloads)</td>
			<td>Java</td>
			<td>Neueste Version</td>
			<td>0.10.2 <p> Informationen zu älteren Clients finden Sie in [Kompatibilität mit früheren Versionen](/docs/services/EventStreams?topic=eventstreams-kafka_clients_classic#compatibility_classic).</p></td>
			<td>[Beispiel für Java-Konsole
![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://github.com/ibm-messaging/event-streams-samples/tree/master/kafka-java-console-sample)<br/>
			[Beispiel für Liberty
![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://github.com/ibm-messaging/event-streams-samples/tree/master/kafka-java-liberty-sample)
			</td>
			</tr>
			<tr>
			<td colspan="3">**Clients anderer Anbieter**</td>
			</tr>
	  		<tr>
			<td>[node-rdkafka ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://github.com/Blizzard/node-rdkafka)</td>
			<td>Node.js</td>
			<td>Neueste Version</td>
			<td>2.2.2</td>
			<td>[Beispiel für Node.js ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://github.com/ibm-messaging/event-streams-samples/tree/master/kafka-nodejs-console-sample)</td>
		</tr>
		<tr>
			<td>[confluent-kafka-python ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://github.com/confluentinc/confluent-kafka-python)</td>
			<td>Python</td>
			<td>Neueste Version</td>
			<td>0.11.0</td>
			<td>[Beispiel für Kafka Python ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://github.com/ibm-messaging/event-streams-samples/tree/master/kafka-python-console-sample)</td>
		</tr>
		<tr>
			<td>[confluent-kafka-go ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://github.com/confluentinc/confluent-kafka-go)</td>
			<td>Golang</td>
			<td>Neueste Version</td>
			<td>0.11.0</td>
			<td></td>
		</tr>
		<tr>
			<td>[librdkafka ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://github.com/edenhill/librdkafka)</td>
			<td>C oder C++</td>
			<td>Neueste Version</td>
			<td>0.11.0</td>
			<td></td>
		</tr>

</table>
### Fußnote
1. {: #footnote1}Hierbei handelt es sich um die früheste Version, die in kontinuierlichen Tests validiert wurde. Normalerweise ist dies ursprüngliche, innerhalb der letzten 12 Monate verfügbare Version, es kann jedoch auch eine neuere Version sein, falls signifikante Probleme bekannt sind.


<!--
## Unsupported clients

The following clients are not supported by {{site.data.keyword.messagehub}}:

### kafka-node
The kafka-node client does not fully support SASL authentication with the PLAIN mechanism so cannot currently be used with {{site.data.keyword.messagehub}}.


### no-kafka 
The no-kafka client does not fully support SASL authentication with the PLAIN mechanism so cannot currently be used with {{site.data.keyword.messagehub}}.

-->

## Clients mit {{site.data.keyword.messagehub}} verbinden
{: #connect_client}

Informationen zur Konfiguration des Java-Clients für die Verbindung mit {{site.data.keyword.messagehub}} finden Sie in [Client konfigurieren](/docs/services/EventStreams?topic=eventstreams-kafka_connect).












