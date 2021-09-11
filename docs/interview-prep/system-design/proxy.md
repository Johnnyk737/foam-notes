# Proxy

## Forward Proxy
A forward proxy is a server that sits between a client and servers and acts on behalf of the client. The client does a request that goes to the forward proxy. Then the proxy forwards it on to the server. When the server response, it gives the response to the forward proxy. Then the proxy forwards the response to the server. The forward proxy is made to attempt to hide the IP addresses of the client from the server. This is how VPNs work in a simpler example.

## Reverse Proxy
The reverse proxy acts on behalf of the server. In this set up, the client can make a call to the reverse proxy, but the client won't know this. Then the reverse proxy forwards the request to the server. The server then sends a response to the reverse proxy, then the reverse proxy forwards that to the client. In an example, when a client searches for a URL, the DNS server retrieves the IP address of the reverse proxy, if it's set up properly. This maintains that the client doesn't know that it is actually talking to the reverse proxy.

### Benefits
 - You can filter out requests that you want to ignore.
 - You can take care of logging for your system.
 - You want to cache things like HTML pages.
 - You can use it as a load balancer.

## Key Terms
 - [Forward Proxy](glossary.md#forward-proxy) - A server that sits between a client and servers and acts on behalf of the client, typically used to mask the client's identity (IP address). Note that forward proxies are often referred to as just proxies.
 - [Reverse Proxy](glossary.md#reverse-proxy) - A server that sits between clients and servers and acts on behalf of the servers, typically used for loggins, load balancing or caching.
 - [Nginx](glossary.md#nginx) - Pronounced "engine X" --not "N jinx", Nginx is a very populat webserver that's often used as a **reverse proxy** and **load balancer**.
