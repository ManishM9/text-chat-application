# text-chat-application

# Text Chat Application (Client-Server Architecture)

> The source code for this project is private due to academic integrity guidelines.  
> Please feel free to [reach out](mailto:manishma@buffalo.edu) if you’d like access for review purposes.

## Overview

This is a networked text chat application developed in C/C++ as part of the **CSE 489/589: Computer Networks** course at the University at Buffalo. It implements a TCP-based client-server architecture, supporting multiple commands and robust message handling across clients.

## Features

- **Point-to-point messaging** (`SEND`)
- **Broadcast messaging** (`BROADCAST`)
- **User statistics tracking** (`STATISTICS`)
- **Blocking functionality** (`BLOCK`, `BLOCKED`, `UNBLOCK`)
- **Buffered message delivery** when clients are offline
- **Robust exception handling** for all commands
- **Graceful client logout**

## Technologies Used

- C/C++
- TCP Sockets
- `select()` system call for I/O multiplexing
- Linux/Unix-based development environment

## Team Contributions

### 🧑‍💻 Manish Malepati (manishma)
- Implemented: `send`, `broadcast`, `statistics`, `block`, `blocked`, `unblock`, `buffer`, `logout`
- Handled: `exception_send`, `exception_block`, `exception_blocked`, `exception_unblock`

### 🧑‍💻 Srijan Sareen (srijansa)
- Implemented: `send`, `broadcast`, `statistics`, `block`, `blocked`, `unblock`, `buffer`, `logout`

## 🖼️ Sample Screenshots

Sent one message and received one message:
![image](https://github.com/user-attachments/assets/5d18584f-1d94-42f2-b4f5-865d9b181cb1)

Broadcast message received:
![image](https://github.com/user-attachments/assets/9a040561-75cd-48b6-a091-6693e937418b)



## 🔒 Access Policy

Due to university guidelines, the full source code is not publicly available.  
To request access, please contact **Manish Malepati** at [manishma@buffalo.edu or manish.malepati@gmail.com].

---

