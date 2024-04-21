## Kafka
### Unit testing
1. Make sure your Docker is running.
2. Generate gRPC client and server interface from .proto file:
```
make dc.generate
```
Or if you only want to generate codes in certain module:
```
make dc.{module}.generate
```
For example:
```
make dc.video.generate
```
3. Test your implementation
```
make dc.test
```
Or if you only want to test certain module:
```
make dc.{module}.test
```
For example:
```
make dc.video.testS
```
#### Result
![image](https://github.com/yaoyao0103/NTHU-Distributed-System/assets/76504560/07aec27a-e582-4646-a316-685abde67a55)
![image](https://github.com/yaoyao0103/NTHU-Distributed-System/assets/76504560/78a162fc-ba27-49ba-a3c3-deb9f317a905)
![image](https://github.com/yaoyao0103/NTHU-Distributed-System/assets/76504560/d367ac47-3e9f-4726-a98a-4ba22cf18d17)
![image](https://github.com/yaoyao0103/NTHU-Distributed-System/assets/76504560/2e4c2380-91ac-4d1a-a887-be184d3fce48)
![image](https://github.com/yaoyao0103/NTHU-Distributed-System/assets/76504560/69f4f203-6771-40a9-93ea-1b9ed33c4358)

### Test like the example video:
1. Make sure your Docker is running, and set the memory space to 10GB
2. Generate docker image
```
make dc.image
```
3. Start up Kafka server, it may take a while
```
docker compose up -d kafka
```
You can test whether kafka runs successfully, if you do not get an error after entering the below command, kafka is running. This command try to have Kafka list all topics
```
docker exec -it nthu-distributed-system-kafka-1 kafka-topics --bootstrap-server kafka:9092 --list
```

4. Start up video-api, video-gateway server
```
docker compose up -d video-api video-gateway
```
5. Start up video-stream server
```
docker compose up -d video-stream
```
6. Send request to the video server
```
curl -X POST localhost:10080/v1/videos -F "file=@/{Your path}/NTHU-Distributed-System/modules/video/service/fixtures/big_buck_bunny_240p_1mb.mp4"
```
7. Check database
You can enter mongo CLI by below commands
```
docker exec -it nthu-distributed-system-mongo-1 bash
```
Then, enter below commands to get records in the database and the videos collection
```
mongo
use nthu_distributed_system
db.videos.find({})
```
#### Result
![image](https://github.com/yaoyao0103/NTHU-Distributed-System/assets/76504560/c53c55cd-4b0f-41ec-b29d-82764d2fe8d4)

