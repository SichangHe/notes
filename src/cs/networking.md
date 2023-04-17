<!-- toc -->
# Networking

# encoding/decoding

- non-return to zero (NRZ)
    - baseline wander
    - synchronization problem
- non-return to zero inverted (NRZI): invert signal on 1
- Manchester encoding: xor clock and bit
    - only 50% efficiency
- 4b/5b encoding
    - 64b/66b
    - 128b/130b
- modulation

# framing

- sentinel-based framing
    - BISYNC, PPP
    - framing byte may appear in payload
        - escape byte
- count-based framing: body length before body
    - DDCMP
- bitwise sentinel framing
    - HDLC
    - bit stuffing: add extra 0 after 5 consecutive 1
- close-based framing
    - fixed size frame
    - need precise clock & synchronization phase
    - high efficiency

## error handling for framing

- parity bit: whether number of 1 is odd

    e.g. server RAM
    - fast, easy in hardware
    - miss many error
    - high overhead
- checksum: add up all sequence of certain length

    e.g. internet checksum
    - easy in software
    - miss many error
- cyclic redundancy check (CRC):
    divide message as a polynomial by generator polynomial

    e.g. BISYNC, DDCMP, HDLC, ethernet, Wi-Fi
    - easy in hardware with shift register
    - good implementation ensure catching
        - all single-bit error
        - double bit error
        - odd number of error
        - burst of error shorter than $k$ bit

# reliable transmission

- acknowledgement (ACK)
- timeout

## stop-and-wait transmission

if ACK arrive before timeout, send next frame, else, send same frame again

- timeout hard to choose
- need 1 bit for frame identifier and in ACK
- waste bandwidth

## continuous transmission: sliding window algorithm

sender

- send window size (SWS)
- last ACK received (LAR)
- last frame sent (LFS)

receiver

- receive window size (RWS)
- largest frame acceptable (LFA)
- last frame received (LFR)

### go-back-$n$

resend all frame since first lost frame

### duplicate ACK

- sender: resend on duplicate ACK
- receiver: resend ACK for the last in-order frame when frame out of order

### selective ACK

- sender: resend missing frame between last ACK and SACK
- receiver: send SACK for out-of-order frame

### sliding window performance

utilize bandwidth

frame size $f$,\
bandwidth $b$,\
transmission time $t$,\
round trip time $r$,\
time to first ACK $t_0$,\
number of packet $n$

$$
t=\frac{f}{b}\\[6pt]
t_0=t+r\\[6pt]
n=\left\lceil \frac{t_0}{t} \right\rceil
$$

### sliding window frame identifier count

- smaller is better since overhead
- ≥ SWS + RWS: prevent overlap of sequence

# Ethernet

- carrier sense: idle/busy
- multiple access: share medium and broadcast
- collision detection

## Ethernet switch

- usually point-to-point
- high collision

## Ethernet address

48 bit printed in hex separated per byte by colon

- unique
- manufacturer are allocated 3-byte OUI
- broadcast address FF:FF:FF:FF:FF:FF

# Wi-Fi

- carrier sense
- multiple access
- collision avoidance
    - request to send (RTS): inform future send
    - clear to send (CTS): reserve medium

## Wi-Fi distribution system

- access point connected to Ethernet
- automatic handover
    - support client mobility
    - new access point inform old one

# network switch

interconnect link of the same type

- many port
- can connect to each other

# forwarding

- require unique address

## packet forwarding (frame-based forwarding)

- each frame contain enough information of destination (overhead)
- no reachability information
- independent forwarding
- congestion
- network switch keep forwarding table
    - map destination to outgoing port

## circuit-based forwarding

- need establish circuit (stateful)
    - virtual circuit established on demand
    - circuit establishment request use frame forwarding
- network switch keep virtual circuit table
    - input port, input id, output port, output id

## source-based routing

- origin provide forwarding information
    - specify each output port in switch
        - intermediate switch shift array
    - address of each switch
- origin need global view
- frame header size undefined

usage

- establish virtual circuit
- go around failure
- hide origin of packet for attack
    - mostly disabled

# Ethernet switch device

multiple Ethernet interface

- build forwarding table
- broadcast if destination not on forwarding table
- remove old entry

## spanning tree algorithm

- disable some link to eliminate loop
- switch with lowest ID is the root
- each switch start with self as root and broadcast root and distance

reason

- broadcast storm: broadcast cycle

drawback

- waste bandwidth
- $O(d)$ where $d$ is diameter of network, slow to converge if $d$ large

## repeater

- increase collision

## virtual local area network (VLAN)

- additional field in frame header
- block invalid address
- scoped broadcast

# interconnect network

- failed attempt to convert packet

## internet protocol (IP)

- service model
    - no guarantee
    - most basic requirement on link layer, work everywhere
- packet header

### IP fragmentation

what to do when packet size exceed frame size

- reassemble packet at destination
- in frame header
    - use same identifier
    - indicate following fragment with flags
    - help reassemble with offset
- alternative: drop packet
    - default in IPv6
    - tell sender maximum valid size

## IP address

- hierarchical
- network identifier
- node identifier

### network information center (NIC)

### IPv4

- class A: big network, first byte < 128, 1 byte reserved
- class B: smaller, first byte 129 ~ 191, 2 byte reserved
- class C: small, first byte ≥ 192, 3 byte reserved

### IPv6

- 16 byte
- written in hex, 2 byte between each colon, $0$s omitted

### subnet/CIDR

split address

- length `x.y.z.w/l`
    - bit not masked determine subnet size
    - network smaller than `/24` usually not allowed in routing table
- netmask: same as length, $1$s followed by $0$s
- can split large subnet/ aggregate small subnet and advertise big network
- routing table can have overlapping entry, specific one used

## IP forwarding by router

- if interface is connected to destination network,
    translate to link-layer address (e.g. MAC) and deliver over local network
- else, find a router nearer to destination and do the above to it

### address translation

- build link-layer address from IP
    - does not work, e.g. IPv4 address (4 byte) to MAC (6 byte)
    - privacy leak, e.g. IPv6 EUI-64 deprecated
- address resolution protocol (ARP)
    - source broadcast ARP request
    - matching node send ARP response with link-layer address to requester
- neighbor discovery protocol (NDP) for IPv6

### default route

just deliver to this route if not in my routing table

## routing table

- can configure manually but usually automatically by routing protocol
- distilled into forwarding table
- map destination to potentially many next port
- additional information than forwarding table

### distance vector protocol

- used by routing information protocol (RIPv2)
- each router periodically broadcast all its best route to each neighbor
- count to infinity problem
    - solution: limit maximum distance to 15
    - split horizon optimization: do not send route back to where it is from

### link-state protocol

- used by open shortest path first (OSPF)
- each router globally broadcast all its link at change
- reliable flooding
    - costly
    - send link-state packet (LSP)
        - list of neighbor and metric (cost) of link
        - sequence number: increasing
        - guaranteed delivery via ACK
        - time-to-live
    - receiver discard LSP with lower sequence number than seen
    - receiver forward LSP
    - receiver optimization: wait for other LSP for a while
- metric
    - usually fixed
    - dynamic metric cause route oscillation and unpredictable performance

## node configuration

- manual configuration: maintain IP allocation table
- autoconfiguration: DHCP

### dynamic host configuration protocol (DHCP)

- client without IP address broadcast DHCP discover message
- DHCP server respond with configuration
    - IP address
    - DNS server
    - default gateway
    - lease duration
- DHCP server reserve IP prefix and give new device unallocated IP address
- DHCP relay allow multiple network to use 1 DHCP server

## internet control message protocol (ICMP)

- report error, transmit metadata
- for troubleshoot

message type

- 0: echo reply
- 3: destination unreachable
    - 0/1/2/3: network/host/protocol/port unreachable
    - 4 fragmentation needed, for maximum transmission unit (MTU) discovery

- 8: echo request

# interdomain routing

## autonomous system (AS)

a.k.a domain

- distinct operator
- transit traffic: traffic across two AS
- stub AS: on the border, no transit trafic
    - transit AS: opposite
- multihoming: network with multiple provider
- peering point: host network equipment

## border gateway protocol (BGP)

- de facto standard
- policy-based routing
    - oblivious to performance
    - goal: find loop-free policy-compliant path
    - no obligation to accept or propagate route
    - can withdraw route
- focus on scalability
    - only propagate most preferred route
- only need to run on router that connect two AS
- configure BGP session manually
    - sometimes require contract and service agreement
    - small/regional network pay larger network for transit

## routing relationship and policy

- whatever make them money
- provider-client/client-provider: client pay for transit
    - provider export all route to client
    - client export only its route to provider
- peer-to-peer: exchange route for free
    - peer export client route to peer

# user datagram protocol (UDP)

multiplex packet for different application

- demultiplexing key (network port) in packet
- add packet to queue for socket. packet stay until application call `recv()`
- datagram: packet

## network port

- 2 byte, local to each node
- which port
    - in the spec
    - portmap
    - well-know port: SSH: 22, DNS: 53, HTTP: 80, HTTPS: 443

# transport control protocol (TCP)

- demultiplexing
- guaranteed delivery
    - dynamic retransmission timer
- in-order delivery
    - dynamic sliding window
- bidirection transmission
- flow control
    - accommodate for slowest endpoint
- congestion control
    - coordinate across nodes

## end-to-end principle

functionality should be provided at a layer only if it can be complete there

- guarantee on each link does not guarantee end-to-end
- TCP/IP push reliable delivery to transport layer

## TCP header

- number each byte: SequenceNum
- ACK for each byte: Acknowledgment
- control sliding window: AdvertisedWindow

## TCP connection establishment

- three-way handshake
