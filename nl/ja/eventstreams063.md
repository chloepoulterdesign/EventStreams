---

copyright:
  years: 2015, 2019
lastupdated: "2019-01-30"

keywords: IBM Event Streams, Kafka as a service, managed Apache Kafka

subcollection: eventstreams

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:note: .note}

# Kafka API クライアントの構成
{: #kafka_api_client}

Kafka API は、{{site.data.keyword.messagehub}} に接続するために、以下のいずれかの資格情報セットを使用します。 
* <code>kafka_brokers_sasl</code> 資格情報と、[VCAP_SERVICES 環境変数](/docs/services/EventStreams?topic=eventstreams-connecting#connect_standard_cf)からの <code>user</code> と <code>password</code>。
* サービス・キー。 詳しくは、[クラスターへの接続](/docs/services/EventStreams?topic=eventstreams-connecting)を参照してください。
{: shortdesc}



ここで、USERNAME および PASSWORD は、{{site.data.keyword.Bluemix_notm}} の {{site.data.keyword.messagehub}} **「サービス資格情報」**タブからの値です。

<code>sasl.jaas.config</code> を使用する場合、同じ JVM で稼働している複数のクライアントはそれぞれ異なる資格情報を使用できます。 詳しくは、[Configuring Kafka clients  ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://kafka.apache.org/documentation/#security_sasl_plain_clientconfig){:new_window} を参照してください。

次の例は、<code>consumer.properties</code> という名前のサンプル構成ファイルです。

```
key.deserializer=org.apache.kafka.common.serialization.StringDeserializer
value.deserializer=org.apache.kafka.common.serialization.StringDeserializer
#
client.id=kafka-java-console-sample-consumer
group.id=kafka-java-console-sample-group
#
security.protocol=SASL_SSL
sasl.mechanism=PLAIN
sasl.jaas.config=org.apache.kafka.common.security.plain.PlainLoginModule required username="USERNAME" password="PASSWORD";
ssl.protocol=TLSv1.2
ssl.enabled.protocols=TLSv1.2
ssl.endpoint.identification.algorithm=HTTPS
#
# please read the Kafka docs about this setting
auto.offset.reset=latest
```
{: codeblock}

<!--17/10/17 - Karen: following info duplicated at messagehub104 -->
## sasl.jaas.config プロパティーの使用 (Java アプリケーションでの接続と認証)
{: #kafka_java notoc}
0.10.2.1 以降の Kafka クライアントを使用している場合、JAAS ファイルの代わりに、クライアント構成に <code>sasl.jaas.config</code> プロパティーを使用できます。 {{site.data.keyword.messagehub}} に接続するためには、<code>sasl.jaas.config</code> を次のように設定します。
<pre>
<code>    sasl.jaas.config=org.apache.kafka.common.security.plain.PlainLoginModule required \
    username="USERNAME" \
    password="PASSWORD";</code>
</pre>
{:codeblock}

以前の Kafka クライアントでは、JAAS 構成ファイルを使用して資格情報を指定する必要がありました。 この方法は不便なため、代わりに <code>sasl.jaas.config</code> プロパティーを使用することをお勧めします。
## Java 以外のアプリケーションでの接続と認証
{: #kafka_notjava notoc}

{{site.data.keyword.messagehub}} サービスは現在、TLS 上の SASL PLAIN を使用してクライアントを認証します。 資格情報は、暗号化された接続を介して伝送されます。
これは、Kafka 0.10.0.X で追加された新機能です。 

SASL PLAIN と Kafka 0.10 をサポートするクライアントであれば、{{site.data.keyword.messagehub}} で機能します。 以下にクライアントの例を示します。

* [librdkafka ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://github.com/edenhill/librdkafka/){:new_window} 
* [confluent-kafka-python ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://github.com/confluentinc/confluent-kafka-python){:new_window} 




