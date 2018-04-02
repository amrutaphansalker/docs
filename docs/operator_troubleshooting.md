
Operator Troubleshooting Guide
================================================================================

#### What to do when downstream operators are slower than the input operators?

#### What must be done if an Operator gets killed after every 60 secs (Timeout issue).

#### How to handle exceptions thrown from the operators?

####  How to create new tuples for every emit?<not clear>

#### How to use multiple-threads in an operator?

#### How to debug slow operators?

#### How to debug blocked operators?

####  Why do I get this exception - "Kryo not deserializable"?
<Please also see, How to troubleshoot Serialization issues?>

####  How to change the operator log level?

####  How to handle idle time in the operator?
<Is this a troubleshoot item?>

#### What are the settings required in YARN and Apex when I get the "Out of memory" error?

#### How do I find the operator checkpoint size?

#### Processing mode Attributes in the Operators
<Is this a troubleshoot item?>

#### Useful Operator Attributes
<Please elaborate>

#### How to locate the operator that is a bottleneck?
<can this be part of FAQ>

#### How to handle bad data that comes in from the port?

#### How to get custom metrics from an operator?
<can this be part of FAQ>

#### How to control CPU allocated to the operator?
<can this be part of FAQ>

#### Can an operator have an optional port?
<can this be part of FAQ>

#### How to configure Operator Memory?

Operator memory for an operator can be configured in one of the following two ways:
* Use the same default values for all the operators:
```<property>
  <name>dt.application.<APPLICATION_NAME>.operator..attr.MEMORY_MB</name>
  <value>2048</value>
</property>
```
This will set 2GB as the size of all the operators in the given application.

* Set a specific value for an operator. In the following example, the operator op is set with 8 GB memory.
```<property>
  <name>dt.application.<APPLICATION_NAME>.operator.Op.attr.MEMORY_MB</name>
  <value>8192</value>
</property>
```
The memory required by an operator should be based on the maximum data that the operator will store in-memory for all the fields: both transient and non-transient. Default value for this attribute is 1024 MB.

#### How to configure Buffer Server memory?

There is a buffer server in each container that hosts an operator with an output port. This output port is connected to an input port outside the container. The buffer server memory of a container can be controlled by BUFFER_MEMORY_MB. This can be configured in any of the following ways:

* Use the same default values for all the output ports of all the operators.
```<property>
  <name>dt.application.<APPLICATION_NAME>.operator..port..attr.BUFFER_MEMORY_MB</name>
  <value>128</value>
</property>
```
This sets 128 MB as the buffer memory for all the output ports of all the operators.

* Set a specific value for a specific output port of a specific operator.  The following example sets 1 GB as buffer memory for output port p of an operator Op:
```<property>
  <name>dt.application.<APPLICATION_NAME>.operator.Op.port.p.attr.BUFFER_MEMORY_MB</name>
  <value>1024</value>
</property>
```
Default value for this attribute is 512 MB

#### How to meet serializability requirements for operators and tuples in an Apex application?

An Apex application needs to satisfy serializability requirements on operators and tuples as follows:
* **Operators**
After an application is launched, the DAG is serialized using a combination of [Java Serialization](https://docs.oracle.com/javase/8/docs/platform/serialization/spec/serialTOC.html) and [Kryo](https://github.com/EsotericSoftware/kryo/blob/master/README.md) and then the DAG is transferred over the network from the launching node to the application master node.
Checkpointing also involves serializing and persisting an operator state to a store and deserializing from the store in case of recovery. The platform uses Kryo serialization in this case. Kryo imposes additional requirements on an operator Java class to be deserializable. For more details check out this [page](https://github.com/EsotericSoftware/kryo/blob/master/README.md#object-creation).
* **Tuples**
Tuples are serialized (and deserialized) according to the specified stream codec when transmitted between Yarn containers. When no stream codec is specified, Apex uses the default stream codec that relies on the [Kryo](https://github.com/EsotericSoftware/kryo/blob/master/README.md) serialization library to serialize and deserialize tuples. A custom stream codec can be specified to use a different serialization framework.

Thread and container local streams do not use a stream codec, hence tuples don't need to be serializable in such cases.

#### How to troubleshoot Serialization issues?

There is no guaranteed way to uncover serialization issues in your code. An operator may emit a problematic tuple only in very rare and hard to reproduce conditions while testing. Kryo deserialization problem in an operator will not be uncovered until the recovery time, and at that point it is most likely too late. It is recommended to unit test an operator's ability to restore itself properly similar to this [example](https://github.com/apache/apex-malhar/blob/master/library/src/test/java/com/datatorrent/lib/io/fs/AbstractFileOutputOperatorTest.java).
To exercise tuple serialization, run your application in [local mode](http://apex.apache.org/docs/apex/application_development/#local-mode) that could uncover many tuple serialization problems. Use the [ApexCLI](http://apex.apache.org/docs/apex/apex_cli/) to launch your application with the -local option to run it in local mode. The application will fail at a point when the platform is unable to serialize or deserialize a tuple,and the relevant exception will be logged on the console or a log file as described in the [Kryo exception](http://docs.datatorrent.com/troubleshooting/#application-throwing-following-kryo-exception) section. Check out that section further for hints about troubleshooting serialization issues.
Transient members
Certain data members of an operator do not need to be serialized or deserialized during deployment or checkpointing/recovery because they are [transient](http://docs.oracle.com/javase/specs/jls/se7/html/jls-8.html#jls-8.3.1.3) in nature and do not represent stateful data. Developers should judiciously use the [transient](http://docs.oracle.com/javase/specs/jls/se7/html/jls-8.html#jls-8.3.1.3) keyword for declaring such non-stateful members of operators (or members of objects that are indirectly members of operators) so that the platform skips serialization of such members and serialization/deserialization errors are minimized. Transient members are further described in the context of the operator life-cycle [here](http://apex.apache.org/docs/apex/operator_development/#setup-call). Typical examples of transient data members are database or network connection objects which need to be initialized before they are used in a process, so they are never persisted across process invocations.

#### How to check the killed operator’s state?

On dtconsole, click the retrieve killed button of the container List. Containers List widget’s default location is on the physical dashboard. Then select the appropriate container of the killed operator and check the state.

#### How to handle high ingestion Rate in OAS?

Usually, OAS consumes the Kafka topic data as soon as it is available from upstream. However, if it cannot cope with the incoming rate, there can be failures in the Input operator. To avoid such issues, the following approaches are suggested:
 OlapParser Operator partitioning
OlapParser operator can be partitioned, if the ingestion rate is very high. For example, for creating 4 partitions, the property dt.operator.OlapParser.attr.PARTITIONER can be used with value as com.datatorrent.common.partitioner.StatelessPartitioner:4
 Increase Retention period for kafka topic
If OAS is overloaded and not processing the data at the same rate as upstream, the retention period for the kafka topic can be increased. This gives sufficient time for OAS to process all the topic data.
 Specify 'auto.offset.reset' consumer property
There can be cases where OAS is unable to keep pace with the upstream and the older data in Kafka topic gets expired because of the retention policy that is set before getting processed by OAS. In such cases the OAS Input operator may fail. To avoid this failure, the consumer property dt.operator.Input.prop.consumerProps(auto.offset.reset) can be set in OAS with value as earliest. With this property, in case of older topic data expiry, the offset used for reading the data is earliestthat is whichever oldest offset that is currently available with the topic. This avoids the Input operator failure but also involves some loss of data. Caution: This is not the recommended approach, as it may result in data loss without any notification.
