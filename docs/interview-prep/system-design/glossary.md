# Glossary

### Client
A machine or process that requests data or service from a server
   > A single machine or piece of software can be both a client and a server at the same time. For instance, a single machine could act as a server for end users and as a client for a database.
### Client-Server model
The paradigm by which modern systems are designed, which consists of clients requesting data or service from servers and servers providing data or service to clients. 
### Databases
Databases are programs that either use disk or memory to do 2 core things: **record** data and **query** data. In general, they are themselves servers that are long lived and interact with the rest of your application through netowrk calls, with protocols on to pof TCP or even HTTP.  Some databases only keep record in memory, and the users of such databases are aware of the fact that those record may be lost forever if the machine or process dies. For the most part though, databases need persistence of those records, and thus cannot use memory. This means that you have to write your data to disk. Anything written to disk will remain through power loss or network partitions, so that's what is used to keep permanent records. Since machines die often in a large scale system, special disk partitions or volumes are used by the database process, and thos volumes can get recovered even if the machine were to go down permanently.
### Disk
Usually refers to either **HDD (Hard-Disk Drive)** or **SSD (Solid-State Drive)**. Data written to disk will persist through power failures and general machine crashes. Disk is also referred to as **non-volatile storage**. SSD is far faster than HDD but also far more expensive from a financial point of view. Because of that, HDD will typically be used for data that's rarely accessed or updated, but that's stored for a long time, and SSD will be used for data that's frequently accessed and updated.
### DNS
Short for Domain Name System, it describes the entities and protocols involved in the translation from domain names to IP addresses. Typically, machines make a DNS query to a well known entity which is responsible for returning the IP address (or multiple ones) of the requested domain name in the response.
### HTTP
The HyperText Transfer Protocol is a very common network protocol implemented on top of TCP. Clients make HTTP requests and servers respond with a response. Requests typically have the following schema:
   ```
   host: string (example: google.com)
   port: integer (example: 80 or 443)
   method: string (example: GET, PUT, POST, DELETE, OPTIONS or PATCH)
   headers: pair list (example: "Content-Type" => "application/json")
   body: opaque sequence of bytes
   ```
   Responses typically have the following schema:
   ```
   status code: integer (example: 200, 401, 404)
   headers: pair list (example: "Content-Length" => 1238)
   body: opaque sequence of bytes
   ```
### IP
Stands for **Internet Protocol**. This network protocol outlines how almost all machine-to-machine communications should happen in the world. Other protocols like **TCP**, **UDP** and **HTTP** are built on top of IP.
### IP Address
An address given to each machine connected to the public internet. IPv4 addresses consist of four numbers separated by dots (eg. a.b.c.d) where all four numbers are between 0 and 255. Special values include: 
   - **127.0.0.1**: Your own local machine, also referred to as **localhost**
   - **192.168.x.y**: Your private network. For instance, your machine and all machines on your private wifi network will usually have the 192.168 prefix.
### IP Packet
Sometimes more boradly referred to as just a network packet, an IP packet is effectively the smallest unit used to describe data being sent over IP, aside from bytes. An IP packet consists of:
   - an **IP header**, which contains the source and destination **IP addresses** as well as other information related to the network.
   - a **payload**, which is just the data being sent over the network.
### Latency
The time it takes for a certain operation to complete in a system. Most often this measure is a time duration, like milliseconds or seconds. You should know these orders of magnitude:
   - Reading 1 MB from RAM: 250 microseconds (.25ms)
   - Reading 2 MB from SSD: 1000 microseconds (1ms)
   - Transfer 1 MB over network: 10000 microseconds (10ms)
   - Reading 1 MB from HDD: 20000 microseconds (20ms)
   - Inter-continental round trip: 150000 microseconds (150ms)
### Memory
Short for **Random Access Memory (RAM)**. Data stored in memory will be lost when the process that has written that data dies.
### Persistent Storage
Usually refers to disk, but in general it is any form of storage that persists if the process in charge of managing it dies.
### Port
In order for multiple programs to listen for new network connections on the same machine without colliding, they pick a **port** to listen on. A port is an integer between 0 and 65,535 (2<sup>16</sup> ports total). Typically, ports 0 - 1023 are reserved for *system ports* (also called *well-known* ports) and shouldn't be used by user-level processes. Certain ports have pre-defined uses, and although you usually won't be required to have the memorized, they can sometimes come in handy. Some examples are: 
   - 22: Secure Shell
   - 53: DNS lookup
   - 80: HTTP
   - 443: HTTPS
### Server
A machine or process that provides data or service for a client, usually by listening for incoming network calls.
   > A single machine or piece of software can be both a client and a server at the same time. For instance, a single machine could act as a server for end users and as a client for a database.
### TCP
Network protocol built on top of IP. Allows for ordered, reliable data delivery between machines over the public internet by creating a **connection**. TCP is usually implemented in the kernel which exposes **sockets** to applications that they can use to stream data through an open connection.
### Throughput
The number of operations that a system can handle properly per time unit. For instance the throughput of a server can often be measured in requests per second (RPS or QPS)
