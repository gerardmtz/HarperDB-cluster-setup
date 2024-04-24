# Memory processes and threads on HarperDB

**Memory Processes:** HarperDB is built on top of the Lightning Memory-Mapped Database (LMDB), a key-value store offering industry-leading performance and functionality.

This allows HarperDB’s storage algorithm to store data in tables as rows/objects.

HarperDB operations are atomic, consistent, and isolated per instance. This means that any query will provide an isolated consistent snapshot view of the database.

**Threads:** Starting from version 4.1, HarperDB introduced the ability to use worker threads for concurrently handling HTTP requests. This was a shift from the previous model where processes handled these requests. The use of threads provides several benefits:

- Better control of traffic delegation with support for optimized load tracking and session affinity.
- Improved debuggability.
- Support for alternate storage models.
- Better memory/resource utilization.

In terms of resource usage, threads require less resources than processes. Every aspect of the Node.js runtime must be duplicated in every extra process. However, worker threads are able to reuse important parts of the runtime including the JS runtime core functions, lmdb-js’s core instance, and perhaps most importantly, the worker pool for async tasks.

Each HarperDB table has a single writer process, avoiding deadlocks and assuring that writes are executed in the order in which they were received. HarperDB tables can have multiple reader processes operating at the same time for consistent, high scale reads.