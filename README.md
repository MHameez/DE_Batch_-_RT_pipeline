# DE_Batch_-_RT_pipeline
Run Kafka

-Start Zookeaper  >> zookeeper-server-start.bat ../../config/zookeeper.properties
-Start Kafka Server >> kafka-server-start.bat ../../config/server.properties
-Create Topic >> kafka-topics.bat --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic crowdedness

-Start Producer >> kafka-console-producer.bat --broker-list localhost:9092 --topic crowdedness
-Start Consumer >> kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic crowdedness --from-beginning

-Create Topics >> kafka-topics.bat --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic delays
Topic Name = "delays"


-Check topics >> kafka-topics.bat --zookeeper localhost:2181 --list
-Delete topic >> kafka-topics.bat --zookeeper localhost:2181 --delete --topic delays



Start ElasticSearch

-Go into ElasticSearch installation folder
-Open CMD
-run .\bin\elasticsearch.bat
-open server in browser http://localhost:9200/

Start Kibana 

-Go into Kibana installation folder
-Open CMD
-run .\bin\kibana.bat
-open server in browser http://localhost:5601

Python Files
1) Skyscanner_Batch_mySQL.ipynb
2) Skyscanner_Real_Stream.ipynb

