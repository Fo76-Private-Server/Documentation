# General
Source: net.ping-receiver, PingReceiver.cpp

# Example

```
Head: e16f80 Body: ffbedc000000010002
```

# Body Structure
0-3 Timestamp

Example: 0xff, 0xbe, 0xdc, 0x00

4-5 "bps"

Example: 0x00, 0x00

6-7 Unknown

Example: 0x01, 0x00

8 Unknown

Example: 0x02

Notes: Is read as 2 single bits and are checked if set inside the client. When set both will be set in the response.
