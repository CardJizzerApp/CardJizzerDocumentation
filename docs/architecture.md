---
title: Architecture
permalink: /docs/architecture
---

# Architecture

The following depicts the way CardJizzer works and which endpoints are involved in the communication.

```
                            +---------------+
                            |               |
+-------------------------->+ Plugin Engine +---------------------------+
|                           |               |                           |
|                           +-----+---+-----+                           |
|                                 ^   |                                 |
|                                 |   v                                 |
|    +----------------+     +-----+---+-----+     +----------------+    |
|    |                +---->+               +---->+                |    |
|    |  CardCastGame  |     |    BACKEND    |     |  Google OAuth  |    |
|    |                +<----+               +<----+                |    |
|    +-------+--------+     +-----+---+-----+     +--------+-------+    |
|            ^                    |   ^                    ^            |
|            +----------------+   |   |   +----------------+            |
|                             |   v   |   |                             |
|                           +-+---+---+---+-+                           |
|                           |               |                           |
+---------------------------+   FRONTEND    +<--------------------------+
                            |               |
                            +---------------+
```
NOTE: Plugin engine is a feature that will be implemented soon.