Operator Library
================

The following operators, classified into four groups, are available:

| **Operator** | **Type** | **Guide** | **Java Docs** |
| --- | --- | --- | --- |
| ActiveMQ |   |   | [Java Docs](https://www.datatorrent.com/docs/saarang/apidocs/latest/com/datatorrent/activemq/AbstractActiveMQInputOperator.html)|
| Avro Parser |   |   |   |
| Azure Blob |   | [Guide](operators/azure\_blob.md) | [Java Docs](https://www.datatorrent.com/docs/saarang/apidocs/latest/com/datatorrent/azure/blob/package-summary.html)|
| Azure Event Hub |   | [Guide](operators/eventhuboutput.md) | [Java Docs]( https://www.datatorrent.com/docs/saarang/apidocs/latest/com/datatorrent/azure/eventhub/package-summary.html)
| Cassandra Output |   |   | [Java Docs](https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/contrib/cassandra/CassandraPOJOOutputOperator.html) |
| CSV Formatter |   | [Guide](http://apex.apache.org/docs/malhar/operators/csvformatter/) | [Java Docs](https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/contrib/formatter/CsvFormatter.html) |
| CSV Parser |  Process | [Guide](http://apex.apache.org/docs/malhar/operators/csvParserOperator/) | [Java Docs](https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/contrib/parser/AbstractCsvParser.html) |
| Deduper |  Process | [Guide](operators/deduper.md) | [Java Docs](https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/org/apache/apex/malhar/lib/dedup/AbstractDeduper.html) |
| Drools |  Process | [Guide](operators/drools\_operator.md) | [Java Docs](https://www.datatorrent.com/docs/saarang/apidocs/latest/com/datatorrent/drools/operator/DroolsOperator.html) |
| Elastic Search Output | Output  | [Guide](operators/elasticsearch.md) | [Java Docs](https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/contrib/elasticsearch/AbstractElasticSearchOutputOperator.html) |
| Elastic Search Input |   |   | [Java Docs](https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/contrib/elasticsearch/AbstractElasticSearchInputOperator.html) |
| File Splitter + Block Reader (Block Reading) |   |   | [Java Docs – File Splitter]( https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/lib/io/fs/AbstractFileSplitter.html), [Java Docs – Block Reader]( https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/lib/io/block/AbstractBlockReader.html) |
| File Splitter + Block Reader (Line Reading) |   |   |   |
| Filter | Process  | [Guide](http://apex.apache.org/docs/malhar/operators/filter/) | [Java Docs]( https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/lib/util/JavaScriptFilterOperator.html) |
| Flume input |   |   |   |
| FS Enrichment |   |   | [Java Docs]( https://www.datatorrent.com/docs/saarang/apidocs/latest/com/datatorrent/operators/fs/RepeatableLineByLineReader.html) |
| FS Output Operator |   |   |   |
| Hbase Input |   |   | [Java Docs](https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/contrib/couchbase/AbstractCouchBaseInputOperator.html) |
| HBase Output |   |   | [Java Docs](https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/contrib/couchbase/AbstractCouchBaseOutputOperator.html) |
| Hive Output Operator |   |   |   |
| JDBC Enrichment |   |   |   |
| JDBC Input Operator |  Input | [Guide](https://github.com/apache/apex-malhar/blob/master/docs/operators/jdbcPollInputOperator.md) | [Java Docs](https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/lib/db/jdbc/AbstractJdbcInputOperator.html) |
| JDBC output | Output  |   | [Java Docs](https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/lib/db/jdbc/AbstractJdbcPOJOOutputOperator.html) |
| JMS Input Operator |  Input | [Guide](http://apex.apache.org/docs/malhar/operators/jmsInputOperator/) | [Java Docs](https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/lib/io/jms/AbstractJMSInputOperator.html) |
| JMS Output Operator | Output  | [Guide](http://apex.apache.org/docs/malhar/operators/jmsMultiPortOutputOperator/) | [Java Docs](https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/lib/io/jms/AbstractJMSOutputOperator.html) |
| Json Formatter | Process  | [Guide](http://apex.apache.org/docs/malhar/operators/jsonFormatter/) | [Java Docs](https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/lib/formatter/JsonFormatter.html) |
| Json Parser | Process  | [Guide](http://apex.apache.org/docs/malhar/operators/jsonParser/) | [Java Docs](https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/contrib/parser/JsonParser.html) |
| Kafka Input Operator (Version 0.8) | Input | [Guide](operators/kafkaInputOperator.md) | [Java Docs](https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/contrib/kafka/KafkaSinglePortStringInputOperator.html) |
| Kafka Input Operator (Version 0.9) |   |   |  |
| Kafka Output Operator |   |   | [Java Docs](https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/contrib/kafka/AbstractKafkaOutputOperator.html) |
| Kinesis Input Operator |   |   | [Java Docs](https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/contrib/kinesis/AbstractKinesisInputOperator.html) |
| Kinesis Output Operator |   |   | [Java Docs](https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/contrib/kinesis/AbstractKinesisOutputOperator.html) |
| Parquet Parser |   |   | [Java Docs](https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/contrib/parquet/AbstractParquetFileReader.html) |
| PMML | Process  |   | [Java Docs](https://www.datatorrent.com/docs/saarang/apidocs/latest/com/datatorrent/pmml/operator/AbstractPMMLScoringOperator.html) |
| Pravega Input |   |   | [Java Docs](https://www.datatorrent.com/docs/saarang/apidocs/latest/com/datatorrent/pravega/AbstractPravegaInputOperator.html) |
| RabbitMQ Input Operator |   |   | [Java Docs](https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/contrib/rabbitmq/AbstractRabbitMQInputOperator.html) |
| RabbitMQ Output Operator |   |   | [Java Docs](https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/contrib/rabbitmq/AbstractRabbitMQOutputOperator.html) |
| Reconciler plugin |   |   |  |
| Regex splitter |   |   |  |
| S3 Input Operator (Block reading) |   |   | [Java Docs](https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/lib/io/fs/S3InputModule.html) |
| S3 Input Operator (Line reading) |   |   |  |
| S3 Output Operator (block) |   |   |  |
| S3 Output Operator (line) |   |   |  |
| SMTP output |   |   | [Java Docs](https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/lib/io/SmtpOutputOperator.html) |
| Solace |   |   |  |
| Solr Output |   |   | [Java Docs](https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/contrib/solr/AbstractSolrOutputOperator.html) |
| SQS Input |   |   |  |
| Stateless Transform | Process  |   |  |
| TcpInputOperator | Input  | [Guide](operators/tcpinputoperator.md) | [Java Docs](https://www.datatorrent.com/docs/saarang/apidocs/latest/com/datatorrent/web/TcpInputOperator.html) |
| WAL plugin |   |   |  |
| Web - AbstractHttpServerOperator | Input/Output  | [Guide](operators/abstracthttpserver.md) | [Java Docs](https://www.datatorrent.com/docs/saarang/apidocs/latest/com/datatorrent/web/AbstractHttpServerOperator.html) |
| Web - AbstractWebSocketServlet |   | [Guide](operators/abstracthttpserver.md) | [Java Docs]( https://www.datatorrent.com/docs/saarang/apidocs/latest/com/datatorrent/web/AbstractWebSocketServlet.html) |
| xml Formatter |   |   | [Java Docs](https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/lib/formatter/XmlFormatter.html) |
| xml Parser |   |   | [Java Docs](https://www.datatorrent.com/docs/dt-malhar/apidocs/latest/com/datatorrent/lib/parser/XmlParser.html) |

- Input
    + TCP Input Operator [Guide](operators/tcpinputoperator.md)
    + Event Hub Input Operator [Guide](operators/eventhubinput.md)
    + Kafka Input [Guide](http://apex.apache.org/docs/malhar/operators/kafkaInputOperator/)
      and [Java Doc](https://ci.apache.org/projects/apex-malhar/apex-malhar-javadoc-release-3.6/com/datatorrent/contrib/kafka/KafkaSinglePortStringInputOperator.html)
    + HDFS Input [Guide](http://apex.apache.org/docs/malhar/operators/fsInputOperator/)
      and [Java Doc](https://ci.apache.org/projects/apex-malhar/apex-malhar-javadoc-release-3.6/com/datatorrent/demos/wordcount/LineReader.html)
    + HDFS Input for large files [Guide](http://apex.apache.org/docs/malhar/operators/file_splitter/)
      and [Java Doc](https://ci.apache.org/projects/apex-malhar/apex-malhar-javadoc-release-3.6/com/datatorrent/lib/io/fs/FileSplitter.html)
    + JDBC Input [Guide](https://github.com/apache/apex-malhar/blob/master/docs/operators/jdbcPollInputOperator.md)
       and [Java Doc](https://ci.apache.org/projects/apex-malhar/apex-malhar-javadoc-release-3.6/com/datatorrent/lib/db/jdbc/JdbcPollInputOperator.html)
    + JMS Input [Guide](http://apex.apache.org/docs/malhar/operators/jmsInputOperator/)
      and [Java Doc](https://ci.apache.org/projects/apex-malhar/apex-malhar-javadoc-release-3.6/com/datatorrent/lib/io/jms/JMSStringInputOperator.html)

- Process
    + PMML Operator [Guide](operators/PMML_operator.md)
    + Drools Operator [Guide](operators/drools_operator.md)
    + Block Reader [Guide](http://apex.apache.org/docs/malhar/operators/block_reader/)
      and [Java Doc](https://ci.apache.org/projects/apex-malhar/apex-malhar-javadoc-release-3.6/com/datatorrent/contrib/parser/AbstractBlockReader.html)
    + CSV Parser [Guide](http://apex.apache.org/docs/malhar/operators/csvParserOperator/)
      and [Java Doc](https://ci.apache.org/projects/apex-malhar/apex-malhar-javadoc-release-3.6/com/datatorrent/contrib/parser/CsvParser.html)
    + JSON Parser [Guide](http://apex.apache.org/docs/malhar/operators/jsonParser/)
      and [Java Doc](https://ci.apache.org/projects/apex-malhar/apex-malhar-javadoc-release-3.6/com/datatorrent/contrib/parser/JsonParser.html)
    + JSON Formatter  [Guide](http://apex.apache.org/docs/malhar/operators/jsonFormatter/)
      and [Java Doc](https://ci.apache.org/projects/apex-malhar/apex-malhar-javadoc-release-3.6/com/datatorrent/lib/formatter/JsonFormatter.html)
    + Deduper  [Guide](http://apex.apache.org/docs/malhar/operators/deduper/)
      and [Java Doc](https://ci.apache.org/projects/apex-malhar/apex-malhar-javadoc-release-3.6/org/apache/apex/malhar/lib/dedup/AbstractDeduper.html)
    + Enrich [Guide](http://apex.apache.org/docs/malhar/operators/enricher/)
      and [Java Doc](https://ci.apache.org/projects/apex-malhar/apex-malhar-javadoc-release-3.6/com/datatorrent/contrib/enrich/AbstractEnricher.html)
    + Filter  [Guide](http://apex.apache.org/docs/malhar/operators/filter/)
      and [Java Doc](https://ci.apache.org/projects/apex-malhar/apex-malhar-javadoc-release-3.6/com/datatorrent/lib/filter/FilterOperator.html)
    + Transform  [Guide](http://apex.apache.org/docs/malhar/operators/transform/)
      and [Java Doc](https://ci.apache.org/projects/apex-malhar/apex-malhar-javadoc-release-3.6/com/datatorrent/lib/filter/TransformOperator.html)

- Output
    + Elasticsearch Output Operator [Guide](operators/elasticsearch.md)
    + Event Hub Output Operator [Guide](operators/eventhuboutput.md)
    + Azure Blob Output Operator [Guide](operators/azure_blob.md)
    + HDFS Output [Guide](http://apex.apache.org/docs/malhar/operators/file_output)
      and [Java Doc](https://ci.apache.org/projects/apex-malhar/apex-malhar-javadoc-release-3.6/com/datatorrent/lib/io/fs/AbstractFileOutputOperator.html)
    + JMS Output [Guide](http://apex.apache.org/docs/malhar/operators/jmsMultiPortOutputOperator/)
      and [Java Doc](https://ci.apache.org/projects/apex-malhar/apex-malhar-javadoc-release-3.6/com/datatorrent/lib/io/jms/JMSMultiPortOutputOperator.html)

- Input/Output
    + AbstractHttpServer Operator [Guide](operators/abstracthttpserver.md)
