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
    - use same identifier, indicate following fragment with flag
- alternative: drop packet
    - default in IPv6
    - tell sender maximum valid size
