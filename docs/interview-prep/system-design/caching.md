# Caching

## Overview
Caching is used to improve time complexity of algorithms. Caching is used to speed up a system. It is used to improve the latency of a system. It will be storing data in a different location than the main store such that it will be faster to retrieve.

## Examples
- You are doing a lot of network requests and you want to stop needing to do so.
- Speed up a computationally expensive operation
- You have an operation that needs to happen numerous times, so you cache it so it can be easily retrieved.

## Types of Caching
- Write-through - Allows you to write to the cache and the main source of truth (database) at the same time. This allows the cache and the database to be in sync. The downside of this is that you still need to call to the database.
- Write-back - Only updates the cache. This means that your cache will be out of date with the database. An async operation is what takes the cache and writes to the database. This can be done in many ways (every 5 minutes, when cache is filled up, etc.)



## Key Terms
 - [Cache](glossary.md#cache) - A piece of hardware or software that stores data, typically meant to retrieve that data faster than otherwise. Caches are often used to store responses to network requests as well as results of computationally long operations. Note that data in a cache can become stale if the main source of truth for that data (i.e. the main database behind the cache) gets updated and the cache doesn't.
 - [Cache Hit](glossary.md#cache-hit) - When requested data is found in a cache.
 - [Cache Miss](glossary.md#cache-miss) - When requested data could have been found in a cache but isn't. This is typically used to refer to a negative consequence of a system failure or of a poor design choice. For example, If a server goes down our load balancer will have to forward requests to a new server, which will result in cache misses.
 - [Cache Eviction Policy](glossary.md#cache-eviction-policy) - The policy by which values get evicted or removed from a cache. Popular cache eviction policies include **LRU** (least-recently used), **FIFO** (first in, first out), and **LFU** (least-frequently used).
 - [Content Delivery Network](glossary.md#content-delivery-network) - A **CDN** is a third-party service that acts like a cache for your servers. Sometimes, web applications can be slow for users in a particular region if your servers are located only in another region. a CDN has servers all around the world, meaning that the latency to a CDN's servers will almost always be far better than the latency to your servers. A CDN's servers are often referred to as **PoPs** (Points of Presence). Two of the most popular CDNs are **Cloudflare** and **Google Cloud CDN**.
