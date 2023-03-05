# Example of documentation

This is an example of documentation

```kroki-mermaid
flowchart TD
    S1["Service One"]
    S2["Service Two"]
    Q1>"Kafka"]
    Q2>"RabbitMQ"]
    
    S1<--prv.gaming.queue-->Q1
    S1<--prv.gaming.queue-->Q2
    S1--Consume-->S2
    
    classDef service fill:green;
    classDef external fill:blue;
    classDef kafka fill:red,fill-opacity:0.35,color:#FFFFFF,stroke-opacity:0.2;
    classDef rabbitMQ fill:red,fill-opacity:0.35,color:#FFFFFF,stroke-opacity:0.2
    class S1 service
    class S2 external
    class Q1 kafka
    class Q2 rabbitMQ
```