Networks
========

## Architecture

1. What is a network?
<!---
A connection of multiple hosts.
-->

1. What is the internet?
<!---
A network of networks. An interconnection between networks.
-->

1. What are the different types/sizes of network? (List 3)
<!--- 
Host-to-Host: A direct connection between two hosts.
Multiple Access Network: All hosts are connected either via a single 
    connection or through a switch.
-->

1. Describe the differences between a packet switched, and circuit switched network.
<!---
A circuit switched network requires a direct and dedicated connection between hosts to communicate
whereas a packet switched network uses known sized "packets" of data which can forwarded between hops
of routers to reach the target destination.
-->

1. How do forwarding and routing differ?
<!---
Forwarding is the action of moving a packet towards a target destination. Routing is the process of 
both building forwarding tables (LUTs) to be used to forward packets towards a target destination.
-->

1. What is the process used to forward packets from routers/switches? 
(This is one of the major causes of the "Best Effort" internet.)
<!---
Statistically Multiplexed - Best Effort: Routers can't necessarily handle all the packets that are being
sent to them, buffers of incoming packets might not be serviced in time which implies that there will
be cases where packets are completely lost, hence best effort.
-->

1. How are different network providers organized? 
    - How do they interact?
<!---
A tiered hierarchy: ~ Three levels of providers. 
Providers can interact in a peer manner (Same level).
Or a service type interaction (One level to another level).
Both of these are business type relationships.
-->

1. Describe the layers in our architectural model used for the internet.
    - Why is this model considered the IP service model?
    - How many/what protocols does each layer define?
<!---
Physical: NRZ[I], Manchester, Ethernet
Data Link: Ethernet
Network/IP: IPv4/6
Transport: TCP, UDP
Application: Telnet, SSH, FTP, etc.

IP Service model since it is "slim waisted" IP acts as a service to all upper level 
layers. Also service model implies that levels offer services to the level above them 
abstracting away details of implementation.
-->

## Physical Layer

### Information Theory

1. Write out the waveforms of each NRZ, NRZ-I, and Manchester for
0x59ab.
<!---
<Note the waveform is doubled to accommodate Manchester ddr>
WAVEFORM    : 110011110000111100110011001111
NRZ         : 110011110000111100110011001111
NRZ-I       : 111100111111001111000011110011
MANCHESTER  : 100110100101101001100110011010
-->

## Data Layer

1. 
<!---
-->

## Network Layer (IP)

### Routers 

1. What is the primary task of routers?
<!---
To route/forward packets from a source towards the destination network.
-->

1. How does a router complete this task? (What do routers build?)
<!---   
By building forwarding tables and partipate in routing protocols.
-->

1. Name two characteristics of the three levels of routers (Simple, Access/Distribution, Core).
<!---
Simple: Cheap, little configuration availiable
Access/Distribution: Common form factor, moderate configuration availiable
Core: Custom hardware (ASICs), Multi-rack systems
-->

1. What are the two major design goals of core routers?
<!---
Performance and Power/Heat
-->

1. What details need to be specified for internetworking? (There are 5)
<!--- 
Moving packets from source towards destination networks
IP packet format
Fragmentation/Assembly details
Error reporting
Routing protocols - Intra/Inter/Multicast
-->

1. Name 7 of 10 fields within the IP Header.
<!---
IP version, header size, protocol, TTL (Time To Live), Flag/IPID/Offset, Src & Dst, Header cksum, options,
-->

1. What is MTU, why does it matter/what is the reason it exists?
<!---
MTU, or Max Transfer Unit, is the maximum size a packet can take across networks. It's defined
as the max( minimum( max size ) ) of the networks, or the biggest packet that can fit through the network
without being fragmented. The reason for this is fragmentation is expensive. Fragmentation occurs
due to the allowance of different max sized packets allowed through a network to enable different hw designs.
-->

1. What two popular network debugging programs use ICMP? How do they work? What is ICMP?
<!---
A: Ping, Traceroute
Traceroute works by incrementally increasing IP TTL (Time To Live) values recieving error messages from
death messages to build a path of hosts. 
Ping sends echo requests to hosts, waits for a reply.
-->

1. What are two protocols for building router forwarding table entries? Explain each.
<!---
Bellman-Ford Routing Information Board (RIB), Dijkstra Open Shortest Path First (OSPF)
Relies on local computation by neighbors to establish rates/local forwarding info.
-->
