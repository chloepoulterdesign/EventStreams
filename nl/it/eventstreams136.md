---

copyright:
  years: 2015, 2019
lastupdated: "2018-06-06"

keywords: IBM Event Streams, Kafka as a service, managed Apache Kafka

subcollection: eventstreams

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}

# Scelta tra le tre API sul piano Classic 
{: #choose_api_classic}

{{site.data.keyword.messagehub}} supporta tre API nel piano Classic. Ecco alcune informazioni per aiutarti a scegliere quella più appropriata:
{: shortdesc}

## Perché utilizzare l'API Kafka?
{: #why_kafka_classic notoc}

Ci sono alcuni motivi per cui si potrebbe scegliere di utilizzare l'API Kafka rispetto alle altre interfacce fornite da {{site.data.keyword.messagehub}}. I motivi includono i seguenti:
{:shortdesc}


* È più facile integrare la tua applicazione con i sistemi esistenti che hanno il supporto Kafka, ad esempio {{site.data.keyword.IBM}} {{site.data.keyword.streaminganalyticsshort}} e {{site.data.keyword.sparks}}.
* Offre una latenza più bassa e una velocità effettiva superiore rispetto alle altre API.
* Offre un'API più articolata dell'API REST Kafka.

## Perché utilizzare l'API REST Kafka?
{: #why_rest_classic notoc}

** L'API Kafka REST è disponibile solo come parte del piano Classic.**
<br/>

L'API REST Kafka è una pratica interfaccia che può essere utilizzata nelle seguenti situazioni:

* Laddove uno sviluppatore vuole iniziare a utilizzare {{site.data.keyword.messagehub}}
* In alcuni casi d'uso a bassa velocità effettiva dove la latenza non è un fattore critico
* Per eseguire il debug e la ricerca di malfunzionamenti

L'API REST Kafka non è stata concepita per essere un'interfaccia ad elevata velocità effettiva e a bassa latenza.Per questi tipi di requisiti, si consiglia di utilizzare l'API Kafka per la connessione da e verso {{site.data.keyword.messagehub}}. Per ulteriori informazioni, vedi [Utilizzo di un client Kafka](/docs/services/EventStreams?topic=eventstreams-kafka_using#kafka_using).

## Perché utilizzare l'API {{site.data.keyword.mql}}?
{: #why_mql_classic notoc}

** L'API MQ Light è disponibile solo come parte del piano Classic.**
<br/>

L'API {{site.data.keyword.mql}} fornisce un'interfaccia di messaggistica basata su AMQP per Java™, Node.js, Python e Ruby. L'API viene fornita per la compatibilità con le versioni precedenti del servizio {{site.data.keyword.mql}}.
















