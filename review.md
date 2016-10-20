Networks
========

## Architecture

1. What is a network?

1. What is the internet?

1. What are the different types/sizes of network? (List 3)

1. Describe the differences between a packet switched, and circuit switched network.

1. How do forwarding and routing differ?

1. What is the process used to forward packets from routers/switches? 
(This is one of the major causes of the "Best Effort" internet.)

1. How are different network providers organized? 
    - How do they interact?

1. Describe the layers in our architectural model used for the internet.
    - Why is this model considered the IP service model?

1. How many protocols do different layers define?
    - What are they and what do they provide?

1. 
## Information Theory

1. 

## Physical Layer

1. 

## Data Layer

1. 

## Network Layer (IP)

### Routers 

1. What is the primary task of routers?
    A: To route/forward packets from a source towards the destination network.

1. How does a router complete this task? (What do routers build?)
    A: By building forwarding tables and partipate in routing protocols.

1. Name two characteristics of the three levels of routers (Simple, Access/Distribution, Core).
    A: Simple: Cheap, little configuration availiable
    Access/Distribution: Common form factor, moderate configuration availiable
    Core: Custom hardware (ASICs), Multi-rack systems

1. What are the two major design goals of core routers?
    A: Performance and Power/Heat

1. What details need to be specified for internetworking? (There are 5)
    A: Moving packets from source towards destination networks
    IP packet format
    Fragmentation/Assembly details
    Error reporting
    Routing protocols - Intra/Inter/Multicast

1. Name 7 of 10 fields within the IP Header.
    A: IP version, header size, protocol, TTL (Time To Live), Flag/IPID/Offset, Src & Dst, Header cksum, options,

1. What is MTU, why does it matter/what is the reason it exists?
    A: MTU, or Max Transfer Unit, is the maximum size a packet can take across networks. It's defined
    as the max( minimum( max size ) ) of the networks, or the biggest packet that can fit through the network
    without being fragmented. The reason for this is fragmentation is expensive. Fragmentation occurs
    due to the allowance of different max sized packets allowed through a network to enable different hw designs.

1. What two popular network debugging programs use ICMP? How do they work? What is ICMP?
    A: Ping, Traceroute
    Traceroute works by incrementally increasing IP TTL (Time To Live) values recieving error messages from
    death messages to build a path of hosts. 
    Ping sends echo requests to hosts, waits for a reply.

1. What are two protocols for building router forwarding table entries? Explain each.
    A: Bellman-Ford Routing Information Board (RIB), Dijkstra Open Shortest Path First (OSPF)
    Relies on local computation by neighbors to establish rates/local forwarding info.

1. 
