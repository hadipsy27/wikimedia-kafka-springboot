## Implement Kafka with Springboot and consume Real time Data Resource

#### Consume Data URI
- Wikimedia url : https://stream.wikimedia.org/v2/stream/recentchange

#### How to Run Kafka
In this Project use Windows OS

#### STEP 1: DOWNLOAD AND INSTALL KAFKA
I use Kafka Binary Download in Scala 12.2 : https://kafka.apache.org/downloads <br>
The Guide to use Kafka in this link : https://kafka.apache.org/quickstart

#### STEP 2: START THE KAFKA ENVIRONMENT (PRIMARY)
Start the ZooKeeper service <br>
`C:\kafka>.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties`

Start the Kafka broker service <br>
`C:\kafka>.\bin\windows\kafka-server-start.bat .\config\server.properties`

#### STEP 3: CREATE A TOPIC TO STORE YOUR EVENTS (DON'T NEED, Because we create from this project) <br>
`C:\kafka>.\bin\windows\kafka-topics.bat --create --topic wikimedia_recentchange --bootstrap-server localhost:9092`

#### STEP 4: WRITE SOME EVENTS INTO THE TOPIC (DON'T NEED, Because we Consume producer from Wikimedia)<br>
`C:\kafka>.\bin\windows\kafka-console-producer.bat --topic wikimedia_recentchange --bootstrap-server localhost:9092`
- hello world
- topic demo

#### STEP 5:  READ THE EVENTS (OPTIONAL, If you need check Kafka consumer, but in this project we use Spring logging)<br>
`C:\kafka>.\bin\windows\kafka-console-consumer.bat --topic wikimedia_recentchange --from-beginning --bootstrap-server localhost:9092`

