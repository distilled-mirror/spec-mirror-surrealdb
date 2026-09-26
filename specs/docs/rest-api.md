> Full SurrealDB documentation index: https://surrealdb.com/docs/llms.txt

# REST API

The SurrealDB REST API: executing queries over HTTP. Manage authentication and perform CRUD operations.

Any language or tool capable of making HTTP requests can interact with SurrealDB through this API. This is useful when an official SDK is not available for your stack, or when you need to integrate SurrealDB with infrastructure tooling, scripts, or third-party platforms.

## What the API provides

- **Query execution** - send SurrealQL statements over HTTP and receive results as JSON.
- **Authentication** - sign in, sign up, and manage tokens via dedicated endpoints.
- **CRUD operations** - create, read, update, and delete records using RESTful conventions.
- **Health and status** - check whether the server is running and accepting connections.

## Protocol details

The full HTTP protocol reference, including request and response formats, authentication headers, and endpoint specifications, is available in the [HTTP protocol](/docs/reference/rest-api/http-protocol.md) page.

## Alternative access methods

If you prefer a richer client experience, SurrealDB also supports:

- **[WebSocket protocol](/docs/reference/rest-api/rpc-protocol.md)** - persistent connections with real-time capabilities, including live queries and [streaming query results](/docs/reference/rest-api/rpc-protocol.md#query_stream) that arrive while the query runs.
- **[gRPC](/docs/reference/rest-api/rpc-protocol.md#grpc-transport)** - the same RPC protocol over HTTP/2, served on the same port with `grpc://` and `grpcs://` addresses, from 3.3.0.
- **[Postgres wire protocol](/docs/reference/rest-api/postgres-protocol.md)** - connect with `psql`, JDBC, and other Postgres clients, then run SurrealQL or ISO GQL (Cypher Query Language) with tabular typed results.
- **Official SDKs** - language-specific clients for [JavaScript](/docs/languages/javascript.md), [Python](/docs/languages/python.md), [Rust](/docs/languages/rust.md), [Go](/docs/languages/golang.md), [Java](/docs/languages/java.md), [.NET](/docs/languages/dotnet.md), and [PHP](/docs/languages/php.md).
