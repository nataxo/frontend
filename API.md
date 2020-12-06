# APIs

## JSON-RPC
JSON-RPC is a stateless, light-weight remote procedure call (RPC) protocol.

### JSON-RPC Advantages
1. It is not necessary to match http code to errors codes. App likely can have more error codes than there is a number of http codes
2. All response/requests data are inside body of response/request  and response is standardized
3. Easy to create rpc over web socket
4. Easy to batch requests
5. Easy to make notifications to server (when client didn't await a reply)
6. RPC is more suitable for: projects with small quantity of entities, with complex business logic, gamedev, messengers and other realtime stuff.

### JSON-RPC Trade-offs
1. Doesn't fit for HTTP-caching
2. Each request is the same in access logs -> have to mark each request
3. Temptation to keep state on the server between requests (violate stateless )
4. Humble documentation tools (no analogues of swagger.io)

### Examples
- <details><summary>rpc call with named parameters</summary>
    <pre>
    --> {"jsonrpc": "2.0", "method": "subtract", "params": {"subtrahend": 23, "minuend": 42}, "id": 3}
    <-- {"jsonrpc": "2.0", "result": 19, "id": 3}

    --> {"jsonrpc": "2.0", "method": "subtract", "params": {"minuend": 42, "subtrahend": 23}, "id": 4}
    <-- {"jsonrpc": "2.0", "result": 19, "id": 4}
    </pre>
    </details>

- <details><summary>rpc call of non-existent method</summary>
    <pre>
    --> {"jsonrpc": "2.0", "method": "foobar", "id": "1"}
    <-- {"jsonrpc": "2.0", "error": {"code": -32601, "message": "Method not found"}, "id": "1"}
    </pre>
</details>

- <details><summary>rpc call with invalid Request object</summary>
    <pre>
    --> {"jsonrpc": "2.0", "method": 1, "params": "bar"}
    <-- {"jsonrpc": "2.0", "error": {"code": -32600, "message": "Invalid Request"}, "id": null}
    </pre>
    </details>

## GraphQL
1. https://www.moesif.com/blog/technical/graphql/REST-vs-GraphQL-APIs-the-good-the-bad-the-ugly/ 
2. https://lwhorton.github.io/2019/08/24/graphql-tradeoffs.html  
In other words, RESTful API calls are chained on the client before the final representation can be formed for display.
GraphQL can reduce this by enabling the server to aggregate the data for the client in a single query.

### GraphQL Advantages
1. The spec requires everything to have a schema. This is great. It enables powerful tooling such as playground and graphiql.
2. It’s very easy to optimize payload size. No overfetching.
3. Reduce a Number of requests: fetch data from multiple resources from client with one request
4. Better and easier documentation
5. allows you to represent this query in a cleaner way

### GraphQL Trade-offs
1. Change backends to follow specification
2. Optimizations: by exposing any node or edge to a client, you may have unleashed unlimited-complexity queries
3. Caching: GraphQL pushes caching out of the network layer and into the application layer. We lose the long lever of intermediaries (CDNs, reverse proxies, gateways, etc.) and features like Etag, Is-Modified-Since, Last-Modified, or Cache-Control. Each application has to develop a custom caching strategy, which is no small feat.

## RESTful API
https://mlsdev.com/blog/81-a-beginner-s-tutorial-for-understanding-restful-api 

### Advantages
1. Easy read requests 
2. Large amount of tooling 
3. Swagger for documentation
4. Cache over http
5. Stateless 
6. Versioning 
7. Easier to read access logs.
8. Easy to build monitoring system to notify about 500 errors and etc.

### RESTful Trade-offs
1. You have to deal with a lot of http response codes 
2. Overfetching
3. Large number of requests

## JSON:API
A specification for building apis in json.
`json:api` provides a specification that covers both serialization formats and expected HTTP behaviors.


## Stateless rule
Each client request to the server have to contain all the necessary information for that request execution without keeping any context on the server side. The entire session state is stored on the client.
