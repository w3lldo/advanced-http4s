advanced-http4s
===============

Code samples of advanced features of [Http4s](http://http4s.org/) in combination with some features of [Fs2](https://functional-streams-for-scala.github.io/fs2/) not often seen.

Streaming end to end
--------------------

- **Server**: Streaming responses end to end, from the `FileService` reading all the directories in your `$HOME` directory to the `FileHttpEndpoint`.
- **Client**: Parsing chunks of the response body produced by the server in a streaming fashion way.

> You'll need two sbt sessions. Run the server in one and after the client in the other to try it out.

Middleware Composition
----------------------

- **GZip**: For compressed responses. Client must set the `Accept Encoding` header to `gzip`.
- **AutoSlash**: To make endpoints work with and without the slash `/` at the end.

> Response compression is verified by `HexNameHttpEndpointSpec`. You can also try it out from Postman or similar.

Authentication
--------------

- **OAuth**: Using Twitter and GitHub APIs.

Media Type negotiation
----------------------

- **XML**
- **Json**

Form Multipart
--------------

- **Uploading a file**

