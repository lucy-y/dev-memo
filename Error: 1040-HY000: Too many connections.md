- mysql에 연결된 클라이언트의 수가 일정수치 이상인 경우 발생

  
```
show variables like "max_connections";
set global max_connections = 200;
```
