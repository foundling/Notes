# REST / Representative State Transfer Notes

*My general Impression*: Trading efficiency for visibility, maintainability, flexibility. 

*design approach*: look at system as a whole and design components that suit its needs.
*null style*: start with empty set of constraints. 

## main characteristics:
+ *stateless*: session state is stored entirely on the client.
    ### Advantages of statelessness:
        + *visibility*: the information about a request is entirely located in the request itself.
        + *reliability*: recovering from partial failures is easier (look into this). 
        + *scalability*: backend doesn't have to manage resources between requests. can free resources quickly.

    ### Disadvantages:
        + *performance*: increases the request overhead.
        + *reliability*: server becomes dependent upon client's implementation of the protocol, since all request data is on client.

+ *cacheable*: server's response data is implicitly/explicity cacheable. client can use it later for 'equivalent requests'.
    ### Advantages of cacheing:
        + *efficiency*: client can reuse response data and improve perceived performance.
    ### Disadvantages:
        + *reliability*: cached data can conflict with server's data.
+ *uniform interface between components*: 
+ *layered*:
