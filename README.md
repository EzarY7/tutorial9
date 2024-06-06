Mochammad Ezar Yudha 2206046746

<h1>Tutorial 9</h1>
<h3>What are the key differences between unary, server streaming, and bi-directional streaming RPC (Remote Procedure Call) methods, and in what scenarios would each be most suitable?</h3>
Unary RPC involves a single request from the client and a single response from the server. Bi-directional streaming RPC allows both sides to send and receive messages continuously.

<h3>What are the potential security considerations involved in implementing a gRPC service in Rust, particularly regarding authentication, authorization, and data encryption?</h3>
To secure a gRPC service in Rust, use TLS/SSL to encrypt data during transmission. Authenticate clients and servers using mutual TLS or tokens like JWT. Control access with roles or permissions to ensure only authorized users can perform certain actions. Validate inputs, limit request rates, log activities, and handle errors safely.

<h3>What are the potential challenges or issues that may arise when handling bidirectional streaming in Rust gRPC, especially in scenarios like chat applications?</h3>
Handling bidirectional streaming in Rust gRPC for chat applications requires managing concurrent streams, error handling, and resource allocation. Smooth communication relies on addressing backpressure, ensuring message order, and implementing scalability measures like load balancing.

<h3>What are the advantages and disadvantages of using the tokio_stream::wrappers::ReceiverStream for streaming responses in Rust gRPC services?</h3>
Using ReceiverStream for streaming responses in Rust gRPC services provides simplicity and compatibility with the Tokio asynchronous runtime. However, it may lack advanced features and optimizations found in specialized stream implementations and could introduce resource overhead, especially in high-throughput scenarios.

<h3>In what ways could the Rust gRPC code be structured to facilitate code reuse and modularity, promoting maintainability and extensibility over time?</h3>
Define gRPC service interfaces separately from their implementations, define service traits that abstract over concrete implementations, and use dependency injection or inversion of control patterns to decouple service implementations from their dependencies.

<h3>In the MyPaymentService implementation, what additional steps might be necessary to handle more complex payment processing logic?</h3>
To handle more complex payment processing logic in the MyPaymentService implementation, we need to consider steps such as input validation, error handling, and integration with external systems. Additionally, ensure secure handling of sensitive payment data, implement transaction logging, and design for scalability to handle high volumes of transactions efficiently.

<h3>What impact does the adoption of gRPC as a communication protocol have on the overall architecture and design of distributed systems, particularly in terms of interoperability with other technologies and platforms?</h3>
gRPC's adoption reshapes architecture by emphasizing performance, simplicity, and cross-platform compatibility. Integrating it may necessitate adjustments to existing patterns and tools to maximize benefits and ensure seamless interoperability.

<h3>What are the advantages and disadvantages of using HTTP/2, the underlying protocol for gRPC, compared to HTTP/1.1 or HTTP/1.1 with WebSocket for REST APIs?</h3>
HTTP/2 offers significant performance improvements over HTTP/1.1 and HTTP/1.1 with WebSocket. However, it introduces complexity and compatibility concerns.

<h3>How does the request-response model of REST APIs contrast with the bidirectional streaming capabilities of gRPC in terms of real-time communication and responsiveness?</h3>
The request-response model of REST APIs is suitable for stateless operations and data retrieval but lacks inherent support for real-time communication. In contrast, gRPC's bidirectional streaming capabilities enable more efficient and responsive real-time communication between clients and servers.

<h3>What are the implications of the schema-based approach of gRPC, using Protocol Buffers, compared to the more flexible, schema-less nature of JSON in REST API payloads?</h3>
gRPC's Protocol Buffers offer data validation, type safety, and efficient serialization with support for schema evolution. JSON in REST APIs provides flexibility but lacks strict validation and may lead to larger payloads and slower processing.