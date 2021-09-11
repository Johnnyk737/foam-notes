# Latency and Throughput

## Latency
How long it takes data to traverse a system and specifically, how long it takes data to get from one point in a system to another. For network latency, this means how long does it take one request from a client to a server, then a server back to the client. This total round trip time is the latency. The most important aspect to know is that different parts of the system have different latency. 

### Examples for latency
- If you are reading 1mb sequentially from memory - 250 microseconds
- If you are reading 1mb sequentially from SSD - 1000 microseconds
- Sending 1mb data over 1gbps network (assuming no real distance) - 10000 microseconds
- Reading 1md from HDD - 20000 microseconds
- Sending packet over network from CA to Netherlands and back - 150000 microseconds ~ 150 ms

## Throughput
How much work a machine can perform in a period of time. How much data can be transferred from one point in a system to another in given amount of time. Usually measured in Gigabits per second, or Kilobits per second. Throughput is normally determined by your cloud provider. Just increasing throughput does not necessary fix any issues with your program.

## Key Terms
1. [Latency](glossary.md#latency) - The time it takes for a certain operation to complete in a system. Most often this measure is a time duration, like milliseconds or seconds. You should know these orders of magnitude:
   - Reading 1 MB from RAM: 250 microseconds (.25ms)
   - Reading 2 MB from SSD: 1000 microseconds (1ms)
   - Transfer 1 MB over network: 10000 microseconds (10ms)
   - Reading 1 MB from HDD: 20000 microseconds (20ms)
   - Inter-continental round trip: 150000 microseconds (150ms)
2. [Throughput](glossary.md#throughput) - The number of operations that a system can handle properly per time unit. For instance the throughput of a server can often be measured in requests per second (RPS or QPS)
