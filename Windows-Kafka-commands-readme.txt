
1. Start zookeeper (Powershell)
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties

2. Start nodes
.\bin\windows\kafka-server-start.bat .\config\server-0.properties
.\bin\windows\kafka-server-start.bat .\config\server-1.properties
.\bin\windows\kafka-server-start.bat .\config\server-2.properties

3. Create a valid transaction
.\bin\windows\kafka-topics.bat --create --bootstrap-server localhost:9092 --replication-factor 3 --partitions 3 --topic valid-transactions


11. Create a suspicious transaction
.\bin\windows\kafka-topics.bat --list --bootstrap-server localhost:9092

5. Check that the topics are created
.\bin\windows\kafka-topics.bat --list --bootstrap-server localhost:9092