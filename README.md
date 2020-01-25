Table of Contents
=================

* [Project Status](#project-status)
* [Requirements](#requirements)
* [Getting Started](#getting-started)
* [General and Reverse Engineering](#general-and-reverse-engineering)
* [Contributing](#contributing)

# Project Status
Not usable. Currently only connects to the UDP Server

# Requirements
https://github.com/Fo76-Private-Server/WinHttpWrapper

https://github.com/Fo76-Private-Server/BnetAPI

https://github.com/Fo76-Private-Server/Fo76_UDPServer

WolfSSL and the WolfSSL csharp wrapper compiled with the correct settings. Alternatively you can use the precompiled binaries
from the Fo76_UDPServer repository.

# Getting Started
Download the [requirements](#requirements).

Configure the Projects in case you dont want to use localhost

Compile the WinHttpWrapper for x64 and copy it to your game folder

Start the BnetAPI Server

Start the Fo76_UDPServer

Login with any credentials

Press Start

# General and Reverse Engineering
The procedure to connect and play on a server of Fo76 works this way:
1. Login and receiving of Characters and Account Information 
2. The Game connects to a websocket (/bps/pub/wsa) which handles the matchmaking and selection of the server which will be joined
3. The Game receives from the WebSocket the Server IP, Port and PSK which will be used for the DTLS communication
4. The Game connects to the Server and expects the hint "PROJECT_76" and the previous key to be used as PSK 

# Contributing
Im currently not focussed on a specific game version. This repository was created and is working with game version 1.2.6.3
The next steps are to reverse engineer the messages the game sends. If you did reverse engineer binaries before and want to help
join the [discord](https://discord.gg/p8FXc9k) .

Current Points of interest are (v1.2.6.3):

Structure of the Snapshots and the structure of the data inside the compressed message head
