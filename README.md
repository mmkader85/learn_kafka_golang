# Learn Kafka Golang

## Architecture diagram of this project

```text
+------------------------+           +---------------------+           +----------------------+
|                        |           |                     |           |                      |
|        HTTP API        |  ----->   |     Kafka Broker    |  ----->   |     Kafka Consumer   |
|   (Gin HTTP Server)    |           |                     |           |                      |
|                        |           +---------------------+           +----------------------+
|      Port: 8080        |                  |                               |
+------------------------+                  |                               |
|                                           |                               |
+------------------------+                  |                               |
|                        |                  |                               |
|      Zookeeper         | <--------------+ |                               |
|                        |                  |                               |
|      Port: 2181        |                  |                               |
+------------------------+                  |                               |
|                                           |                               |
+------------------------+                  |                               |
|                        |                  |                               |
|       Kafka CLI        | -----------------+                               |
|     Initialization     |                                                  |
|                        |                                                  |
+------------------------+                                                  |
|                                           |                               |
+------------------------+                                                  |
|                        |                                                  |
|       Application      | -------------------------------------------------+
|     (Golang Binary)    |
|                        |
|      Port: 8080        |
+------------------------+
```
