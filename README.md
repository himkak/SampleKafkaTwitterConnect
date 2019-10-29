# SampleKafkaTwitterConnect
Kafka connector usage to fetch twitter tweets.
Configure the twitter.properties to fetch the topics.
# Usage
- update the twitter properties, fetch the secrtes and api access keys from twitter devloper
- start the zookeeper
`zookeeper-server-start.sh config\zookeeper.properties`
- start kafka broker
`kafka-server-start.bat config\server.properties`
- Create a topic : twitter_status_connect `kafka-topics.sh --create --topic twitter_status_connect --zookeeper localhost:2181 --replication-factor 1 --partitions 1`
- Create another topic: twitter_delete_connect `kafka-topics.sh --create --topic twitter_delete_connect --zookeeper localhost:2181 --replication-factor 1 --partitions 1`
- Run the command : `connect-standalone.bat" connect-standalone.properties`
