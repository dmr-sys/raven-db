# Raven Database
Raven is a database written in Rust. The earlier version started as an attempt to learn Rust, this
version builds on that to be production-grade.

## Overall Architecture:
___________________________________________________________________________________________________
|           |               | Frontend  | Execution Engine | Storage Engine |                      |
|-----------|---------------|-----------|------------------|----------------|----------------------|
| Client => | Network Layer | Lexer     | Query executor   | Disk manager   | OS                   |
|           |               | Parser    | Cache manager    | Buffer manager | filesystem interface |
|           |               | Optimizer | Utility services | Index manager  |                      |
___________________________________________________________________________________________________

