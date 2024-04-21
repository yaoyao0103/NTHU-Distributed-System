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
### Result
![image](https://github.com/yaoyao0103/NTHU-Distributed-System/assets/76504560/07aec27a-e582-4646-a316-685abde67a55)
![image](https://github.com/yaoyao0103/NTHU-Distributed-System/assets/76504560/78a162fc-ba27-49ba-a3c3-deb9f317a905)
![image](https://github.com/yaoyao0103/NTHU-Distributed-System/assets/76504560/d367ac47-3e9f-4726-a98a-4ba22cf18d17)
![image](https://github.com/yaoyao0103/NTHU-Distributed-System/assets/76504560/2e4c2380-91ac-4d1a-a887-be184d3fce48)
![image](https://github.com/yaoyao0103/NTHU-Distributed-System/assets/76504560/69f4f203-6771-40a9-93ea-1b9ed33c4358)


