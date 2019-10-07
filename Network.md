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

    The [physical layer](https://en.wikipedia.org/wiki/Physical_layer) is responsible for the transmission and reception of unstructured raw data between a device and a physical [transmission medium](https://en.wikipedia.org/wiki/Transmission_medium). It converts the digital bits into electrical, radio, or optical signals. Layer specifications define characteristics such as voltage levels, the timing of voltage changes, physical data rates, maximum transmission distances, modulation scheme, channel access method and physical connectors. This includes the layout of [pins](https://en.wikipedia.org/wiki/Lead_(electronics)), [voltages](https://en.wikipedia.org/wiki/Voltage), line [impedance](https://en.wikipedia.org/wiki/Characteristic_impedance), cable specifications, signal timing and frequency for wireless devices. Bit rate control is done at the physical layer and may define transmission mode as [simplex](https://en.wikipedia.org/wiki/Simplex_communication), [half duplex](https://en.wikipedia.org/wiki/Duplex_(telecommunications)#Half-duplex), and [full duplex](https://en.wikipedia.org/wiki/Duplex_(telecommunications)#Full-duplex). The components of a physical layer can be described in terms of a [network topology](https://en.wikipedia.org/wiki/Network_topology). [Bluetooth](https://en.wikipedia.org/wiki/Bluetooth), [Ethernet](https://en.wikipedia.org/wiki/Ethernet_physical_layer), and [USB](https://en.wikipedia.org/wiki/USB) all have specifications for a physical layer.

  - 