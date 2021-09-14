# BGP - Border Gateway Protocol

* IETF RFC 4271

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

* **Idle** - Neighbor is not responding
* **Active** - Attempting to connect
* **Connect** - TCP session established
* **Open Sent** - Open message sent
* **Open Confirm** - Response received
* **Established** - Adjacency established

## BGP Terminology

* **Autonomous System (AS)** - Logical domain under a single administration.
  * 2-byte: 1 - 65535
    * 1 - 64511 Public AS numbers
    * 64512 - 65535 Private AS numbers
  * 4-byte: 65536 - 4294967295
* **External BGP (eBGP)** - BGP adjacency between ASs.
* **Internal BGP (iBGP)** - BGP adjacensy within an AS.
* **Path Attributes** - Different parameters used for path selection.
* **Route Reflector (RR)** - central device used to avoid full-mesh in iBGP.
* **BGP Confederations** - single AS, which is subdivided into a number of internal sub-AS's to reduce the number of BGP peerings within a single AS.

## BGP Path Attributes

Category | Attribute Name
-------- | --------------
Well-Known Mandatory |  AS Path, Origin, Next_Hop
Well-Known Discretionary | Local Preference, Atomic_Aggregate
Optional Transitive | Aggregator, Community
Optional Non-transitive | Multi_Exit_Discrimiantor (MED), Originator_ID, Cluster List


## BGP Best Path Selection

1. Weight - Administrative preference (Highest)
2. Local Preference - Communicated between peers within an AS (Highest)
3. Self-Originated - Prefer paths originated locally
4. AS Path - Minimize AS hops (Shortest)
5. Origin - Prefer IGP-learned routes over EGP, and EGP over unknown(IGP, EGP, ?)
6. MED - Used externally to enter an AS (Lowest)
7. External - Prefer eBGP routes over iBGP (eBGP, iBGP)
8. IGP Cost - Consider IGP metric (Lowest)
9. Multiple paths
10. eBGP Peering - Favor more stable routes (Oldest)
11. Router ID (Lowest)
12. Cluster List (Minimum)
13. Neighbor IP address (Lowest)

###### Links:
https://ipcisco.com/wp-content/uploads/Cheat-Sheets/bgp.pdf

https://packetlife.net/media/library/1/BGP.pdf
