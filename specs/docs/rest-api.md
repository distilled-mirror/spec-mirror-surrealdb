---
title: "Protocols and APIs"
description: "How clients reach SurrealDB: HTTP endpoints, RPC over WebSocket, HTTP and gRPC, the Postgres and MySQL wire protocols, the CBOR encoding and the error format that every protocol shares."
canonical_url: "https://surrealdb.com/docs/reference/protocols"
section: "Protocols and APIs"
surrealdb_version: "4.x"
last_modified: "2026-11-19T06:06:22Z"
---

> Full SurrealDB documentation index: https://surrealdb.com/docs/llms.txt

# Protocols and APIs

How clients reach SurrealDB: HTTP endpoints, RPC over WebSocket, HTTP and gRPC, the Postgres and MySQL wire protocols, the CBOR encoding and the error format that every protocol shares.

Any language or tool capable of making HTTP requests can interact with SurrealDB, and standard Postgres and MySQL clients can connect to it as well. This is useful when an official SDK is not available for your stack, or when you need to integrate SurrealDB with infrastructure tooling, scripts, or third-party platforms.

## Ways to connect

| Protocol | What it gives you |
| --- | --- |
| [HTTP](/docs/reference/protocols/http-protocol.md) | Query execution over plain endpoints with JSON results, sign in and sign up endpoints, create, read, update and delete operations using RESTful conventions, and health and status checks. |
| [RPC over WebSocket](/docs/reference/protocols/rpc-protocol.md) | Persistent connections with real-time capabilities, including live queries and [streaming query results](/docs/reference/protocols/rpc-protocol.md#query_stream) that arrive while the query runs. |
| [gRPC](/docs/reference/protocols/rpc-protocol.md#grpc-transport) | The same RPC protocol over HTTP/2, served on the same port with `grpc://` and `grpcs://` addresses, from 3.3.0. |
| [Postgres wire protocol](/docs/reference/protocols/postgres-protocol.md) | Connections from `psql`, JDBC and other Postgres clients, running SurrealQL, PostgreSQL SQL or ISO GQL with tabular typed results. |
| [MySQL wire protocol](/docs/reference/protocols/mysql-protocol.md) | From SurrealDB 4.0, connections from the `mysql` client and MySQL drivers, running MySQL SQL, SurrealQL or another dialect. |

## Encoding, errors and compatibility

- [CBOR protocol](/docs/reference/protocols/cbor-protocol.md) - the CBOR encoding SurrealDB uses, and its custom tags.
- [Errors](/docs/reference/protocols/errors.md) - the kind, wire code, structured details and cause that every error carries, in the same shape across every protocol and SDK.
- [Compatibility matrix](/docs/reference/protocols/sql-compatibility.md) - what the PostgreSQL and MySQL dialects run, feature by feature, and what they refuse.

## Official SDKs

If you prefer a richer client experience, the official SDKs are language-specific clients for [JavaScript](/docs/languages/javascript.md), [Python](/docs/languages/python.md), [Rust](/docs/languages/rust.md), [Go](/docs/languages/golang.md), [Java](/docs/languages/java.md), [.NET](/docs/languages/dotnet.md) and [PHP](/docs/languages/php.md).
