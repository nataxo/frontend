# http 2.0

## http1.1 restrictions
1. amount of simultaneous TCP connections is limited to 6
2. Uncompressed headers in requests
3. Sending all headers in every request which increases requests time particularly ones with the large coockies.

## http2 features
* data compression of http headers (HPACK compression)
* http2 Server Push  - allows http2 server to send resources to a http2 client before the client requests them. It is, for the most part, a performance technique that can be helpful in loading resources preemptively. http2 Server Push is not a notification mechanism from server to client. 
* pipelining of requests - http2 addresses this issue through request multiplexing, which eliminates HOL blocking at the application layer, but HOL still exists at the transport (TCP) layer
* fixing the head-of-line blocking problem in http1.x
* multiplexing streams - multiple requests over a single TCP connection. Use single connection to simultaneously delivery several response and requests. It reduces a page load time.
* Prioritizing requests

## Sources
https://developers.google.com/web/fundamentals/performance/http2/

https://habr.com/ru/post/221427