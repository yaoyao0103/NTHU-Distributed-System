## Test
### To generate gRPC client and server interface (make sure your Docker is running)
```
make dc.generate
```
Or if you only want to generate codes in certain module:
```
# comment
make dc.comment.generate
# video
make dc.video.generate
```
### To test the implementation
```
make dc.test
```
Or if you only want to test certain module:
```
# comment
make dc.comment.test
# video
make dc.video.test
```

## Result
![image](https://github.com/yaoyao0103/NTHU-Distributed-System/assets/76504560/52e1cdd1-6800-4325-9498-57dcb9aedbf8)
![image](https://github.com/yaoyao0103/NTHU-Distributed-System/assets/76504560/2bfd54cf-8951-43bf-be00-eed3bad27141)
![image](https://github.com/yaoyao0103/NTHU-Distributed-System/assets/76504560/cf289283-9ea1-4dba-b8ff-76d1d21d7dc2)
