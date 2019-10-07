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
    
    To establish a connection, TCP uses a three-way [handshake](https://en.wikipedia.org/wiki/Handshaking). Before a client attempts to connect with a server, the server must first bind to and listen at a port to open it up for connections: this is called a passive open. Once the passive open is established, a client may initiate an active open. To establish a connection, the three-way (or 3-step) handshake occurs:
    
    1. **SYN**: The active open is performed by the client sending a SYN to the server. The client sets the segment's sequence number to a random value A.
    2. **SYN-ACK**: In response, the server replies with a SYN-ACK. The acknowledgment number is set to one more than the received sequence number i.e. A+1, and the sequence number that the server chooses for the packet is another random number, B.
    3. **ACK**: Finally, the client sends an ACK back to the server. The sequence number is set to the received acknowledgement value i.e. A+1, and the acknowledgement number is set to one more than the received sequence number i.e. B+1.
    
    At this point, both the client and server have received an acknowledgment of the connection. The steps 1, 2 establish the connection parameter (sequence number) for one direction and it is acknowledged. The steps 2, 3 establish the connection parameter (sequence number) for the other direction and it is acknowledged. With these, a full-duplex communication is established.
