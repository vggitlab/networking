# BGP - Border Gateway Protocol

* IETF RFC 4271, 1771, 2858

* Routing Protocol of global Internet

* Routing between Autonomous System

* Path Vector Protocol

* TCP destinaton port 179


## BGP Message Types

* Open
* Update
* Keepalive
* Notification

## BGP Neighbor States

* Idle - Neighbor is not responding
* Active - Attempting to connect
* Connect - TCP session established
* Open Sent - Open message sent
* Open Confirm - Response received
* Established - Adjacency established

## BGP Terminology

* Autonomous System (AS) - Logical domain under a single administration.
  * 2-byte: 1 - 65535
    * 1 - 64511 Public AS numbers
    * 64512 - 65535 Private AS numbers
  * 4-byte: 65536 - 4294967295
* External BGP (eBGP) - BGP adjacency between AS's.
* Internal BGP (iBGP) - BGP adjacensy within an AS.




https://ipcisco.com/wp-content/uploads/Cheat-Sheets/bgp.pdf

https://packetlife.net/media/library/1/BGP.pdf



