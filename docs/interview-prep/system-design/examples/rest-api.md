# REST API

## Constraints
### Uniform Interface
1. Identifiers for each resource
2. Manipulates them through representation
3. Messages composed of hypermedia
### Client-server
1. Encapsulation
### Stateless
Shouldn't be storing information on the server
### Cacheable
1. resources must declare themselves as Cacheable.
2. High performance and reduces server payload
### Layered system
1. Each component should only know what the next layer is.
### Executable code

## Why?
1. Can be a companies greatest asset
2. permanence
3. Scalability
4. generality
5. Encapsulation
6. simple (Than soap)
7. Faster  (Than soap)

## Conventions
### resources
1. Collections and instances
2. Use nouns, not verbs
3. coarse grained

#### Good
/albums
/albums/123
/songs

#### Bad
/getAlbums

### Behavior
HTTP verbs do not have 1:1 relationship with CRUD

### Documentation
1. easy to find, publicly Available
2. Show examples of complete request/response cycles

### Versioning
1. want to ensure backwards compatibility
2. Use either head or URL

### Other Conventions
1. result filtering, ordering and searching
2. allow limits
3. pagination
