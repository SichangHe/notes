<!-- toc -->
# Networking

## encoding/decoding

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

## framing

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
