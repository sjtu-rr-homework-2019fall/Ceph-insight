# A technical report about  computer network

- ### Definition

  A **computer network** is a [digital](https://en.wikipedia.org/wiki/Digital_signal) [telecommunications network](https://en.wikipedia.org/wiki/Telecommunications_network) which allows [nodes](https://en.wikipedia.org/wiki/Node_(networking)) to share resources. In computer networks, [computing devices](https://en.wikipedia.org/wiki/Computing_device) [exchange data](https://en.wikipedia.org/wiki/Data_transmission) with each other using connections ([data links](https://en.wikipedia.org/wiki/Data_link)) between nodes. These data links are established over [cable media](https://en.wikipedia.org/wiki/Networking_cables) such as wires or optic cables, or [wireless media](https://en.wikipedia.org/wiki/Wireless_network) such as [Wi-Fi](https://en.wikipedia.org/wiki/Wi-Fi).

- ### Network packet

  A **network packet** is a formatted unit of [data](https://en.wikipedia.org/wiki/Data) carried by a [packet-switched network](https://en.wikipedia.org/wiki/Packet-switched_network). A packet consists of control information and user data,[[1\]](https://en.wikipedia.org/wiki/Network_packet#cite_note-1) which is also known as the [payload](https://en.wikipedia.org/wiki/Payload_(computing)). Control information provides data for delivering the payload, for example: source and destination [network addresses](https://en.wikipedia.org/wiki/Network_address), [error detection](https://en.wikipedia.org/wiki/Error_detection) codes, and sequencing information. Typically, control information is found in packet [headers](https://en.wikipedia.org/wiki/Header_(computing)) and [trailers](https://en.wikipedia.org/wiki/Trailer_(computing)).

  In packet switching, the [bandwidth](https://en.wikipedia.org/wiki/Bandwidth_(computing)) of the communication medium is shared between multiple communication sessions, in contrast to [circuit switching](https://en.wikipedia.org/wiki/Circuit_switching), in which circuits are preallocated for the duration of one session and data is typically transmitted as a continuous [bit stream](https://en.wikipedia.org/wiki/Bit_stream).

  There is no denying that packet switching, which we are using today, is far better than the circuit switching because of better fault handling. Suppose we lost or broke a package on the road, we can use error detecting codes to find the broken package, and resend the package. In my humble opinion, it is much harder for bit stream to achieve this effect.

  In the seven-layer [OSI model](https://en.wikipedia.org/wiki/OSI_model) of [computer networking](https://en.wikipedia.org/wiki/Computer_networking), *packet* strictly refers to a [protocol data unit](https://en.wikipedia.org/wiki/Protocol_data_unit) at layer 3, the [network layer](https://en.wikipedia.org/wiki/Network_layer). The correct term for a data unit at layer 2, the [data link layer](https://en.wikipedia.org/wiki/Data_link_layer), is a *frame*, and at Layer 4, the [transport layer](https://en.wikipedia.org/wiki/Transport_layer), the correct term is *segment* or *datagram*. For TCP/IP communication over [Ethernet](https://en.wikipedia.org/wiki/Ethernet), a [TCP segment](https://en.wikipedia.org/wiki/TCP_segment) is carried in one or more [IP packets](https://en.wikipedia.org/wiki/IP_packet_(disambiguation)), which are each carried in one or more [Ethernet frames](https://en.wikipedia.org/wiki/Ethernet_frame).

- ### OSI model

  - #### Definition

    The **Open Systems Interconnection model** (**OSI model**) is a [conceptual model](https://en.wikipedia.org/wiki/Conceptual_model) that characterizes and standardizes the communication functions of a [telecommunication](https://en.wikipedia.org/wiki/Telecommunication) or computing system without regard to its underlying internal structure and technology. Its goal is the interoperability of diverse communication systems with standard [communication protocols](https://en.wikipedia.org/wiki/Communication_protocols). The model partitions a communication system into [abstraction layers](https://en.wikipedia.org/wiki/Abstraction_layer). The original version of the model had seven layers.

  - #### Chart

    [![Capture.png](https://i.postimg.cc/HsT9L72Q/Capture.png)](https://postimg.cc/Z0Dd7nXR)

  - #### Layer 1: Physical Layer

    This layer may be implemented by a [PHY chip](https://en.wikipedia.org/wiki/PHY_(chip)).

    The physical layer consists of the [electronic circuit](https://en.wikipedia.org/wiki/Electronic_circuit) transmission technologies of a network.[[2\]](https://en.wikipedia.org/wiki/Physical_layer#cite_note-Fundamentals_of_Sensor_Network_Programming-2) It is a fundamental layer underlying the higher level functions in a network, and can be implemented through a great number of different hardware technologies with widely varying characteristics.[[3\]](https://en.wikipedia.org/wiki/Physical_layer#cite_note-3)

    The physical layer defines the means of transmitting raw [bits](https://en.wikipedia.org/wiki/Bit)[[4\]](https://en.wikipedia.org/wiki/Physical_layer#cite_note-4) rather than logical [data packets](https://en.wikipedia.org/wiki/Network_packet) over a physical [data link](https://en.wikipedia.org/wiki/Data_link) connecting network [nodes](https://en.wikipedia.org/wiki/Node_(networking)). The [bitstream](https://en.wikipedia.org/wiki/Bitstream) may be grouped into code words or symbols and converted to a physical [signal](https://en.wikipedia.org/wiki/Signal) that is transmitted over a [transmission medium](https://en.wikipedia.org/wiki/Transmission_medium). The physical layer provides an electrical, mechanical, and procedural interface to the transmission medium. The shapes and properties of the [electrical connectors](https://en.wikipedia.org/wiki/Electrical_connector), the frequencies to broadcast on, the [line code](https://en.wikipedia.org/wiki/Line_code) to use and similar low-level parameters, are specified here.

  - #### Layer 2: Data Link Layer

    The **data layer**, or **layer 2**, is the second layer of the seven-layer [OSI model](https://en.wikipedia.org/wiki/OSI_model) of [computer networking](https://en.wikipedia.org/wiki/Computer_network). This layer is the protocol layer that transfers data between adjacent network nodes in a [wide area network](https://en.wikipedia.org/wiki/Wide_area_network) (WAN) or between nodes on the same [local area network](https://en.wikipedia.org/wiki/Local_area_network) (LAN) [segment](https://en.wikipedia.org/wiki/Network_segment).

    The data link layer has two sublayers: *logical link control* (LLC) and *media access control* (MAC).

    A MAC address is intended as a unique serial number. MAC addresses are typically assigned to network interface hardware at the time of manufacture. The most significant part of the address identifies the manufacturer, who assigns the remainder of the address, thus provide a potentially unique address. This makes it possible for frames to be delivered on a network link that interconnects hosts by some combination of [repeaters](https://en.wikipedia.org/wiki/Repeater), [hubs](https://en.wikipedia.org/wiki/Ethernet_hub), [bridges](https://en.wikipedia.org/wiki/Network_bridge) and [switches](https://en.wikipedia.org/wiki/Network_switch), but not by [network layer](https://en.wikipedia.org/wiki/Network_layer) [routers](https://en.wikipedia.org/wiki/Router_(computing)). Thus, for example, when an [IP](https://en.wikipedia.org/wiki/Internet_Protocol) packet reaches its destination (sub)network, the destination IP address (a layer 3 or network layer concept) is resolved with the [Address Resolution Protocol](https://en.wikipedia.org/wiki/Address_Resolution_Protocol) for [IPv4](https://en.wikipedia.org/wiki/IPv4), or by [Neighbor Discovery Protocol](https://en.wikipedia.org/wiki/Neighbor_Discovery_Protocol) (IPv6) into the MAC address (a layer 2 concept) of the destination host.

    

  - #### Layer 3: Network Layer

    The [network layer](https://en.wikipedia.org/wiki/Network_layer) provides the functional and procedural means of transferring variable length [data](https://en.wikipedia.org/wiki/Data) sequences (called [packets](https://en.wikipedia.org/wiki/Network_packet)) from one node to another connected in "different networks". A network is a medium to which many nodes can be connected, on which every node has an *address* and which permits nodes connected to it to transfer messages to other nodes connected to it by merely providing the content of a message and the address of the destination node and letting the network find the way to deliver the message to the destination node, possibly [routing](https://en.wikipedia.org/wiki/Routing) it through intermediate nodes. If the message is too large to be transmitted from one node to another on the data link layer between those nodes, the network may implement message delivery by splitting the message into several fragments at one node, sending the fragments independently, and reassembling the fragments at another node. It may, but does not need to, report delivery errors.

  - #### Layer 4: Transport Layer

    In [computer networking](https://en.wikipedia.org/wiki/Computer_network), the **transport layer** is a conceptual division of methods in the [layered architecture](https://en.wikipedia.org/wiki/Abstraction_layer) of protocols in the network stack in the [Internet protocol suite](https://en.wikipedia.org/wiki/Internet_protocol_suite) and the [OSI model](https://en.wikipedia.org/wiki/OSI_model). The protocols of this layer provide host-to-host communication services for applications.[[1\]](https://en.wikipedia.org/wiki/Transport_layer#cite_note-1) It provides services such as [connection-oriented communication](https://en.wikipedia.org/wiki/Connection-oriented_communication), [reliability](https://en.wikipedia.org/wiki/Reliability_(computer_networking)), [flow control](https://en.wikipedia.org/wiki/Flow_control_(data)), and [multiplexing](https://en.wikipedia.org/wiki/Multiplexing).

    The best-known transport protocol of TCP/IP is the [Transmission Control Protocol](https://en.wikipedia.org/wiki/Transmission_Control_Protocol) (TCP), and lent its name to the title of the entire suite. It is used for connection-oriented transmissions, whereas the connectionless [User Datagram Protocol](https://en.wikipedia.org/wiki/User_Datagram_Protocol) (UDP) is used for simpler messaging transmissions. TCP is the more complex protocol, due to its [stateful design](https://en.wikipedia.org/wiki/Stateful_design) incorporating reliable transmission and data stream services.

  - #### Layer 5: Session Layer

    In the seven-layer [OSI model](https://en.wikipedia.org/wiki/OSI_model) of [computer networking](https://en.wikipedia.org/wiki/Computer_network), the **session layer** is **layer 5**.

    The session layer provides the mechanism for opening, closing and managing a [session](https://en.wikipedia.org/wiki/Session_(computer_science)) between end-user application processes, i.e., a semi-permanent dialogue. Communication sessions consist of requests and responses that occur between applications. Session-layer services are commonly used in application environments that make use of [remote procedure calls](https://en.wikipedia.org/wiki/Remote_procedure_call) (RPCs).

    Other examples of session layer implementations include [Zone Information Protocol](https://en.wikipedia.org/wiki/Zone_Information_Protocol) (ZIP) – the [AppleTalk](https://en.wikipedia.org/wiki/AppleTalk) protocol that coordinates the name binding process, and Session Control Protocol (SCP) – the [DECnet](https://en.wikipedia.org/wiki/DECnet) Phase IV session-layer protocol.

  - #### Layer 6: Presentation Layer

    The presentation layer is responsible for the formatting and delivery of information to the application layer for further processing or display.[[4\]](https://en.wikipedia.org/wiki/Presentation_layer#cite_note-4) It relieves the application layer of concern regarding syntactical differences in [data](https://en.wikipedia.org/wiki/Data) representation within the end-[user](https://en.wikipedia.org/wiki/User_(computing)) systems. An example of a presentation service would be the conversion of an [EBCDIC](https://en.wikipedia.org/wiki/EBCDIC)-coded text [computer file](https://en.wikipedia.org/wiki/Computer_file) to an [ASCII](https://en.wikipedia.org/wiki/ASCII)-coded file.

    [Serialization](https://en.wikipedia.org/wiki/Serialization) of complex data structures into flat byte-strings (using mechanisms such as [TLV](https://en.wikipedia.org/wiki/Type-length-value) or [XML](https://en.wikipedia.org/wiki/XML)) can be thought of as the key functionality of the presentation layer.

    [Encryption](https://en.wikipedia.org/wiki/Encryption) is typically done at this level too, although it can be done on the [application](https://en.wikipedia.org/wiki/Application_layer), [session](https://en.wikipedia.org/wiki/Session_layer), [transport](https://en.wikipedia.org/wiki/Transport_layer), or [network layers](https://en.wikipedia.org/wiki/Network_layer), each having its own advantages and disadvantages.[[1\]](https://en.wikipedia.org/wiki/Presentation_layer#cite_note-Network+_Guide_to_Networks-1) [Decryption](https://en.wikipedia.org/wiki/Decryption) is also handled at the presentation layer. For example, when logging on to bank account sites the presentation layer will decrypt the data as it is received.[[1\]](https://en.wikipedia.org/wiki/Presentation_layer#cite_note-Network+_Guide_to_Networks-1) Another example is representing structure, which is normally standardized at this level, often by using [XML](https://en.wikipedia.org/wiki/XML). As well as simple pieces of data, like strings, more complicated things are standardized in this layer. Two common examples are 'objects' in [object-oriented programming](https://en.wikipedia.org/wiki/Object-oriented_programming), and the exact way that streaming [video](https://en.wikipedia.org/wiki/Video) is transmitted.

  - #### Layer 7: Application Layer

    In the OSI model, the definition of the application layer is narrower in scope. The OSI model defines the application layer as the user interface responsible for displaying received information to the user. In contrast, the Internet Protocol Suite does not concern itself with such detail. OSI also explicitly distinguishes additional functionality below the application layer, but above the transport layer at two additional levels: the [session layer](https://en.wikipedia.org/wiki/Session_layer), and the [presentation layer](https://en.wikipedia.org/wiki/Presentation_layer). OSI specifies a strict modular separation of functionality at these layers and provides [protocol implementations](https://en.wikipedia.org/wiki/OSI_protocols) for each layer.

- ### **Transmission Control Protocol** (**TCP**)

  - ####   Definition

    The **Transmission Control Protocol** (**TCP**) is one of the main [protocols](https://en.wikipedia.org/wiki/Communications_protocol) of the [Internet protocol suite](https://en.wikipedia.org/wiki/Internet_protocol_suite). It originated in the initial network implementation in which it complemented the [Internet Protocol](https://en.wikipedia.org/wiki/Internet_Protocol) (IP). Therefore, the entire suite is commonly referred to as *TCP/IP*. TCP provides [reliable](https://en.wikipedia.org/wiki/Reliability_(computer_networking)), ordered, and [error-checked](https://en.wikipedia.org/wiki/Error_detection_and_correction) delivery of a stream of [octets](https://en.wikipedia.org/wiki/Octet_(computing)) (bytes) between applications running on hosts communicating via an IP network. Major internet applications such as the [World Wide Web](https://en.wikipedia.org/wiki/World_Wide_Web), [email](https://en.wikipedia.org/wiki/Email), [remote administration](https://en.wikipedia.org/wiki/Remote_administration), and [file transfer](https://en.wikipedia.org/wiki/File_transfer) rely on TCP. Applications that do not require reliable data stream service may use the [User Datagram Protocol](https://en.wikipedia.org/wiki/User_Datagram_Protocol) (UDP), which provides a [connectionless](https://en.wikipedia.org/wiki/Connectionless_communication) [datagram](https://en.wikipedia.org/wiki/Datagram) service that emphasizes reduced [latency](https://en.wikipedia.org/wiki/Latency_(engineering)) over reliability.

  - ####  Structure

    Processes transmit data by calling on the TCP and passing buffers of data as arguments. The TCP packages the data from these buffers into segments and calls on the internet module [e.g. IP] to transmit each segment to the destination TCP.

    A TCP segment consists of a segment *header* and a *data* section. The segment header contains 10 mandatory fields, and an optional extension field (*Options*, pink background in table). The data section follows the header and is the payload data carried for the application. 

    [![Capture.png](https://i.postimg.cc/qMpHB8yL/Capture.png)](https://postimg.cc/JtY2PHTD)
    
    [![1280px-Tcp-state-diagram-fixed-new-svg.png](https://i.postimg.cc/dQHz2DfR/1280px-Tcp-state-diagram-fixed-new-svg.png)](https://postimg.cc/QV74sNhV)
    
    [![1024px-TCP-CLOSE-svg.png](https://i.postimg.cc/7hXN1C9F/1024px-TCP-CLOSE-svg.png)](https://postimg.cc/wRyJgjS2)
    
    To establish a connection, TCP uses a three-way [handshake](https://en.wikipedia.org/wiki/Handshaking). Before a client attempts to connect with a server, the server must first bind to and listen at a port to open it up for connections: this is called a passive open. Once the passive open is established, a client may initiate an active open. To establish a connection, the three-way (or 3-step) handshake occurs:
    
    1. **SYN**: The active open is performed by the client sending a SYN to the server. The client sets the segment's sequence number to a random value A.
    2. **SYN-ACK**: In response, the server replies with a SYN-ACK. The acknowledgment number is set to one more than the received sequence number i.e. A+1, and the sequence number that the server chooses for the packet is another random number, B.
    3. **ACK**: Finally, the client sends an ACK back to the server. The sequence number is set to the received acknowledgement value i.e. A+1, and the acknowledgement number is set to one more than the received sequence number i.e. B+1.
    
    At this point, both the client and server have received an acknowledgment of the connection. The steps 1, 2 establish the connection parameter (sequence number) for one direction and it is acknowledged. The steps 2, 3 establish the connection parameter (sequence number) for the other direction and it is acknowledged. With these, a full-duplex communication is established.
    
    The connection termination phase uses a four-way handshake, with each side of the connection terminating independently. When an endpoint wishes to stop its half of the connection, it transmits a FIN packet, which the other end acknowledges with an ACK. Therefore, a typical tear-down requires a pair of FIN and ACK segments from each TCP endpoint. After the side that sent the first FIN has responded with the final ACK, it waits for a timeout before finally closing the connection, during which time the local port is unavailable for new connections; this prevents confusion due to delayed packets being delivered during subsequent connections.
    
  - #### Resource usage
  
    Most implementations allocate an entry in a table that maps a session to a running operating system process. Because TCP packets do not include a session identifier, both endpoints identify the session using the client's address and port. Whenever a packet is received, the TCP implementation must perform a lookup on this table to find the destination process. Each entry in the table is known as a Transmission Control Block or TCB. It contains information about the endpoints (IP and port), status of the connection, running data about the packets that are being exchanged and buffers for sending and receiving data.
  
    The number of sessions in the server side is limited only by memory and can grow as new connections arrive, but the client must allocate a random port before sending the first SYN to the server. This port remains allocated during the whole conversation, and effectively limits the number of outgoing connections from each of the client's IP addresses. If an application fails to properly close unrequired connections, a client can run out of resources and become unable to establish new TCP connections, even from other applications.
  
    Comment: This approach (table entry) allows communication between processes on different machines and prevent them from affecting each other. But one thing we should remember is that port is also a kind of resource, which needs to be closed if it is not in use.
  
  - #### Reliable transmission
  
    TCP uses a *sequence number* to identify each byte of data. The sequence number identifies the order of the bytes sent from each computer so that the data can be reconstructed in order, regardless of any [packet reordering](https://en.wikipedia.org/wiki/Packet_reordering), or [packet loss](https://en.wikipedia.org/wiki/Packet_loss) that may occur during transmission. The sequence number of the first byte is chosen by the transmitter for the first packet, which is flagged SYN. This number can be arbitrary, and should, in fact, be unpredictable to defend against [TCP sequence prediction attacks](https://en.wikipedia.org/wiki/TCP_sequence_prediction_attack).
  
    Acknowledgements (ACKs) are sent with a sequence number by the receiver of data to tell the sender that data has been received to the specified byte. ACKs do not imply that the data has been delivered to the application. They merely signify that it is now the receiver's responsibility to deliver the data.
  
    Reliability is achieved by the sender detecting lost data and retransmitting it. TCP uses two primary techniques to identify loss. Retransmission timeout (abbreviated as RTO) and duplicate cumulative acknowledgements (DupAcks).
  
    Comment: It is very important for packages to have an identifier for ordering because they may be transmitted out of order. This is also important when a package is lost on the way. When it comes to security, the first number should be arbitrary.
  
  - #### Dupack-based retransmission
  
    If a single packet (say packet 100) in a stream is lost, then the receiver cannot acknowledge packets above 100 because it uses cumulative ACKs. Hence the receiver acknowledges packet 99 again on the receipt of another data packet. This duplicate acknowledgement is used as a signal for packet loss. That is, if the sender receives three duplicate acknowledgements, it retransmits the last unacknowledged packet. A threshold of three is used because the network may reorder packets causing duplicate acknowledgements. This threshold has been demonstrated to avoid spurious retransmissions due to reordering.
  
    Comment: This approach is suitable for most of the situation. But if we want to retransmit all the lost packages in the end rather than at once, maybe we should find another way.
  
  - #### Timeout-based retransmission
  
    Whenever a packet is sent, the sender sets a timer that is a conservative estimate of when that packet will be acked. If the sender does not receive an ACK by then, it transmits that packet again. The timer is reset every time the sender receives an acknowledgement. This means that the retransmit timer fires only when the sender has received *no* acknowledgement for a long time.  Further, in case a retransmit timer has fired and still no acknowledgement is received, the next timer is set to twice the previous value (up to a certain threshold). Among other things, this helps defend against a [man-in-the-middle](https://en.wikipedia.org/wiki/Man-in-the-middle_attack) [denial of service attack](https://en.wikipedia.org/wiki/Denial_of_service_attack) that tries to fool the sender into making so many retransmissions that the receiver is overwhelmed.
  
    Comment: This approach is important in making the retransmissions in an rational scale and attack-proof.
  
  - #### Error detection
  
    Sequence numbers allow receivers to discard duplicate packets and properly sequence reordered packets. Acknowledgments allow senders to determine when to retransmit lost packets.
  
    To assure correctness a checksum field is included
  
  - #### Flow control
  
    TCP uses a [sliding window](https://en.wikipedia.org/wiki/Sliding_Window_Protocol) flow control protocol. In each TCP segment, the receiver specifies in the *receive window* field the amount of additionally received data (in bytes) that it is willing to buffer for the connection. The sending host can send only up to that amount of data before it must wait for an acknowledgement and window update from the receiving host.
  
    Comment: This is quite interesting that your download speed is growing from zero to the highest pitch due to the sliding window flow control.
  
  - #### Congestion control
  
    Acknowledgments for data sent, or lack of acknowledgments, are used by senders to infer network conditions between the TCP sender and receiver. Coupled with timers, TCP senders and receivers can alter the behavior of the flow of data. This is more generally referred to as congestion control and/or network congestion avoidance.
  
    In TCP, the **congestion window** is one of the factors that determines the number of bytes that can be outstanding at any time. The congestion window is maintained by the sender. Note that this is not to be confused with the sliding window size which is maintained by the receiver. The congestion window is a means of stopping a link between the sender and the receiver from becoming overloaded with too much traffic. It is calculated by estimating how much congestion there is on the link.
  
    The flow of data over a TCP connection is also controlled by the use of the *receive window* advertised by the receiver. By comparing its own congestion window with the *receive window*, a sender can determine how much data it may send at any given time.
  
  - #### Vulnerabilities
  
    - ##### Denial of service
  
      By using a [spoofed IP](https://en.wikipedia.org/wiki/IP_address_spoofing) address and repeatedly sending [purposely assembled](https://en.wikipedia.org/wiki/Mangled_packet) SYN packets, followed by many ACK packets, attackers can cause the server to consume large amounts of resources keeping track of the bogus connections. 
  
    - ##### Connection hijacking
  
      An attacker who is able to eavesdrop a TCP session and redirect packets can hijack a TCP connection. To do so, the attacker learns the sequence number from the ongoing communication and forges a false segment that looks like the next segment in the stream. Such a simple hijack can result in one packet being erroneously accepted at one end. 
  
    - ##### TCP veto
  
      An attacker who can eavesdrop and predict the size of the next packet to be sent can cause the receiver to accept a malicious payload without disrupting the existing connection. The attacker injects a malicious packet with the sequence number and a payload size of the next expected packet.
  
- ### User Datagram Protocol (UDP)

  - #### Definition
  
    With UDP, computer applications can send messages, in this case referred to as *datagrams*, to other hosts on an [Internet Protocol](https://en.wikipedia.org/wiki/Internet_Protocol) (IP) network. Prior communications are not required in order to set up [communication channels](https://en.wikipedia.org/wiki/Communication_channel) or data paths.
  
  - #### Characteristic
  
    - It is *transaction-oriented*, suitable for simple query-response protocols such as the [Domain Name System](https://en.wikipedia.org/wiki/Domain_Name_System) or the [Network Time Protocol](https://en.wikipedia.org/wiki/Network_Time_Protocol).
    - It provides *datagrams*, suitable for modeling other protocols such as [IP tunneling](https://en.wikipedia.org/wiki/IP_tunneling) or [remote procedure call](https://en.wikipedia.org/wiki/Remote_procedure_call) and the [Network File System](https://en.wikipedia.org/wiki/Network_File_System).
    - It is *simple*, suitable for [bootstrapping](https://en.wikipedia.org/wiki/Bootstrapping) or other purposes without a full [protocol stack](https://en.wikipedia.org/wiki/Protocol_stack), such as the [DHCP](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol) and [Trivial File Transfer Protocol](https://en.wikipedia.org/wiki/Trivial_File_Transfer_Protocol).
    - It is *stateless*, suitable for very large numbers of clients, such as in [streaming media](https://en.wikipedia.org/wiki/Streaming_media) applications such as [IPTV](https://en.wikipedia.org/wiki/IPTV).
    - The *lack of retransmission delays* makes it suitable for real-time applications such as [Voice over IP](https://en.wikipedia.org/wiki/Voice_over_IP), [online games](https://en.wikipedia.org/wiki/Online_games), and many protocols using [Real Time Streaming Protocol](https://en.wikipedia.org/wiki/Real_Time_Streaming_Protocol).
    - Because it supports [multicast](https://en.wikipedia.org/wiki/Multicast), it is suitable for broadcast information such as in many kinds of [service discovery](https://en.wikipedia.org/wiki/Service_discovery) and shared information such as [Precision Time Protocol](https://en.wikipedia.org/wiki/Precision_Time_Protocol) and [Routing Information Protocol](https://en.wikipedia.org/wiki/Routing_Information_Protocol).
  
  - #### Structure
  
    [![Capture.png](https://i.postimg.cc/Y9cpJMKy/Capture.png)](https://postimg.cc/WDnLZR4M)
  
  - #### Reliability and congestion control
  
    Lacking reliability, UDP applications must be willing to accept some packet loss, reordering, errors or duplication. 
  
    Most often, UDP applications do not employ reliability mechanisms and may even be hindered by them
  
    Comment ：It is  quite clear that UDP is suitable for Streaming media, in that kind of situation, the latency and the speed is the major concern, package loss does not bring fatal fault.
  
- ### Comparison of UDP and TCP

  The major difference between UDP and TCP is that UDP is stateless, not ordered and unreliable. But at the same time, it is lightweight and can be sent to multiple device at once.

- ### Wired technologies

  - #### Coaxial cable

    Coaxial cable conducts electrical signal using an inner conductor (usually a solid copper, stranded copper or copper plated steel wire) surrounded by an insulating layer and all enclosed by a shield, typically one to four layers of woven metallic braid and metallic tape. The cable is protected by an outer insulating jacket. Short coaxial cables are commonly used to connect home [video](https://en.wikipedia.org/wiki/Video) equipment

    [![RG-6-coaxial-cable.png](https://i.postimg.cc/D07Q2V37/RG-6-coaxial-cable.png)](https://postimg.cc/mz61w5rn)

    Long distance coaxial cable was used in the 20th century to connect [radio networks](https://en.wikipedia.org/wiki/Radio_network), [television networks](https://en.wikipedia.org/wiki/Television_network), and [Long Distance telephone](https://en.wikipedia.org/wiki/L-carrier) networks though this has largely been superseded by later methods

  - #### Twisted pair

    It typically consists of 4 pairs of copper cabling that can be utilized for both voice and data transmission. The use of two wires twisted together helps to reduce [crosstalk](https://en.wikipedia.org/wiki/Crosstalk_(electronics)) and [electromagnetic induction](https://en.wikipedia.org/wiki/Electromagnetic_induction).

    A twisted pair can be used as a [balanced line](https://en.wikipedia.org/wiki/Balanced_line), which as part of a [balanced circuit](https://en.wikipedia.org/wiki/Balanced_circuit) can greatly reduce the effect of noise currents induced on the line by coupling of electric or magnetic fields. 

    [![FTP-cable3.jpg](https://i.postimg.cc/tJ3zGhSn/FTP-cable3.jpg)](https://postimg.cc/1VzFpNZy)

    Comment: The advantage is that it can minimize the noise on the line, and it is a cheap solution for this problem.

  - #### Optical fiber

    An **optical fiber** is a flexible, [transparent](https://en.wikipedia.org/wiki/Transparency_and_translucency) [fiber](https://en.wikipedia.org/wiki/Fiber) made by [drawing](https://en.wikipedia.org/wiki/Drawing_(manufacturing)) [glass](https://en.wikipedia.org/wiki/Glass) ([silica](https://en.wikipedia.org/wiki/Silica)) or plastic to a diameter slightly thicker than that of a [human hair](https://en.wikipedia.org/wiki/Hair's_breadth).[[1\]](https://en.wikipedia.org/wiki/Optical_fiber#cite_note-1) Optical fibers are used most often as a means to transmit light between the two ends of the fiber and find wide usage in [fiber-optic communications](https://en.wikipedia.org/wiki/Fiber-optic_communication), where they permit transmission over longer distances and at higher [bandwidths](https://en.wikipedia.org/wiki/Bandwidth_(computing)) (data rates) than electrical cables.

    [![Fibreoptic.jpg](https://i.postimg.cc/3JRfsqjg/Fibreoptic.jpg)](https://postimg.cc/jCphNZF5)

    

  - 

  

  

  

  
