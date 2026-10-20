# TCP text chat: university networking case study

A C/C++ client-server chat application developed for the University at Buffalo's CSE 489/589 Computer Networks course. This public repository contains a case study and screenshots; the course source code remains private under academic-integrity rules. Behavior and implementation details described below come from the earlier project README and cannot be rerun from this repository.

## Architecture

```text
Client A ?? TCP ???
Client B ?? TCP ????? Server event loop (select) ?? delivery / buffering
Client C ?? TCP ???
```

The project used TCP sockets for client-server communication and the Unix `select()` system call to monitor multiple connections. The server was responsible for routing direct and broadcast messages and maintaining state used by blocking and offline delivery. The public materials do not include a protocol specification, wire format, concurrency limits, or source-level error handling.

## Documented behavior

| Command or feature | Intended behavior |
| --- | --- |
| `SEND` | Deliver a message to one user. |
| `BROADCAST` | Deliver a message to eligible connected users. |
| `STATISTICS` | Show user or traffic statistics. |
| `BLOCK`, `BLOCKED`, `UNBLOCK` | Manage and inspect sender blocking. |
| Offline buffering | Queue eligible messages while a recipient is offline for later delivery. |
| `LOGOUT` | End a client session. |

The previous README also listed handlers for invalid send, block, blocked, and unblock requests. Exact command syntax, delivery guarantees, queue persistence, and edge cases are not documented in the public repository.

## Screenshots

- [Direct message example](https://github.com/user-attachments/assets/5d18584f-1d94-42f2-b4f5-865d9b181cb1)
- [Broadcast example](https://github.com/user-attachments/assets/9a040561-75cd-48b6-a091-6693e937418b)

These screenshots illustrate a course demo; they do not establish load capacity or reliability.

## Contributions and limits

The earlier README credits Manish Malepati and Srijan Sareen with work across messaging, statistics, blocking, buffering, and logout. It specifically listed Manish on exception handling for send and blocking commands. The private source history is needed to attribute individual functions more precisely.

There is no runnable build, test suite, or public protocol specification in this repository. This was an academic exercise, not a hosted chat service. Questions about the work can be sent to [Manish Malepati](mailto:manish.malepati@gmail.com).
