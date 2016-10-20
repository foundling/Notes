# REST / Representative State Transfer Notes

*Good Resources*:

+ http://www.vinaysahni.com/best-practices-for-a-pragmatic-restful-api
+ http://www.ics.uci.edu/~fielding/pubs/dissertation/rest_arch_style.htm

**My general Impression**: Trading efficiency for visibility, maintainability, flexibility. 

**design approach**: look at system as a whole and design components that suit its needs.
**null style**: start with empty set of constraints. 

## main characteristics:
+ **stateless**: session state is stored entirely on the client.
    ### Advantages of statelessness:
        - **visibility**: the information about a request is entirely located in the request itself.
        - **reliability**: recovering from partial failures is easier (look into this). 
        - **scalability**: backend doesn't have to manage resources between requests. can free resources quickly.

    ### Disadvantages:
        - **performance**: increases the request overhead.
        - **reliability**: server becomes dependent upon client's implementation of the protocol, since all request data is on client.

+ **cacheable**: server's response data is implicitly/explicity cacheable. client can use it later for 'equivalent requests'.
    ### Advantages of cacheing:
        - **efficiency**: client can reuse response data and improve perceived performance.
    ### Disadvantages:
        - **reliability**: cached data can conflict with server's data.
+ **uniform interface between components**: 
+ **layered**:

## What is a Resource?

The resource is the central abstraction of information. It's anything that can be named, any target of a hypertext reference, a mapping to a set of entities, but not the entities themselves *at any point in time*. 

**advantages:**

+ A resource can map to an entity before it exists. this late binding removes the need to change links when the resource changes. 
+ Reduces the cost of broken links by not specifying the resource they point to statically.

resource examples:

+ weather in LA
+ person
+ document
+ video
+ latest version of some software

## What is a Representation?

The complete description of the state of the request at that time.  A sequence of bytes and metadata to describe them. And sometimes, meta-metadata to ensure document integrity.

## Rest Components


