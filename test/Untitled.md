KafkaConsumer中的参数众多，远非示例initConfig()方法中的那样只有5个，开发人员可
以根据业务应用的实际需求来修改这些参数的默认值，以达到灵活调配的目的。一般情况下，
普通开发人员无法全部记住所有的参数名称，只能有个大致的印象，在实际使用过程中，诸如
“key.deserializer”“auto.offset.reset”之类的字符串经常由于人为因素而书写错误。为此，我们
可以直接使用客户端中的org.apache.kafka.clients.consumer.ConsumerConfig类来做一定程度上
的预防，每个参数在ConsumerConfig类中都有对应的名称，就以代码清单3-1中的initConfig()
方法为例，引入ConsumerConfig后的修改结果如下：