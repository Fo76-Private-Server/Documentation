Table of Contents
=================

* [General Structure](#general-structure)
* [Types](#types)

# General Structure

Example Ping Request Packet

```
e16f80ffbedc000000010002
```

Byte 0-1 Session. 

Example: 0xE1, 0x6F

When the wrong session is send to the client, the packet will be dropped.



Byte 2 Type

Example: 0x80

Most significant bit seems to be only set when the client send the token to the server.

Byte 3-N Body

Example: 0xff, 0xbe, 0xdc, 0x00, 0x00, 0x00, 0x01, 0x00, 0x02

# Types

[Token - 0x00](/Packets/Token.md)

[Ping Request - 0x80](/Packets/Ping-Request.md)

[Ping Response - 0x81](/Packets/Ping-Response.md)

[Data - 0x82](/Packets/Data.md)
