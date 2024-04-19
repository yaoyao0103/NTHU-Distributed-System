## Test
### Test your implementation in the otelkit package.
```
make dc.pkg.test
```
### Verify your implementation of the interceptor with the following steps.
First, build your image.
```
make dc.image
```
Then, start comment-server, comment-gateway and prometheus server.
```
docker-compose up -d comment-api comment-gateway prometheus
```
Make some requests to the comment server.
For example:
```
curl -X GET "http://localhost:10081"
```

## Result
![image](https://github.com/yaoyao0103/NTHU-Distributed-System/assets/76504560/1a9149dd-cd0f-4a97-af71-bacc22749ab1)
![image](https://github.com/yaoyao0103/NTHU-Distributed-System/assets/76504560/a5fb994d-29db-4365-b2ee-680c7f5efb8f)
![image](https://github.com/yaoyao0103/NTHU-Distributed-System/assets/76504560/3637519b-6b91-432d-bb63-5fe536327b8c)
