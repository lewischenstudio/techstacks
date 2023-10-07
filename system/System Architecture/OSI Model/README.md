# The OSI Model

#### Table of Contents

- [What is the OSI Model](#what-is-the-osi-model)
- [The OSI Model Explained: The OSI 7 Layers](#the-osi-model-explained-the-osi-7-layers)
- [Why you need to know the 7 OSI layers](#why-you-need-to-know-the-7-osi-layers)
- [Advantages of the OSI Model](#advantages-of-the-osi-model)
- [OSI vs. TCP/IP Model](#osi-vs-tcpip-model)

### What is the OSI Model

The Open Systems Interconnection (OSI) model describes seven layers that
computer systems use to communicate over a network. It was the first standard
model for network communications, adopted by all major computer and
telecommunication companies in the early 1980s

The modern Internet is not based on OSI, but on the simpler TCP/IP model.
However, the OSI 7-layer model is still widely used, as it helps visualize and
communicate how networks operate, and helps isolate and troubleshoot networking
problems.

OSI was introduced in 1983 by representatives of the major computer and telecom
companies, and was adopted by ISO as an international standard in 1984.

### The OSI Model Explained: The OSI 7 Layers

| **No.** | **Layer**          | **Description**                                                                      |
| :-----: | ------------------ | ------------------------------------------------------------------------------------ |
|    7    | Application Layer  | Human-computer interaction layer, where applications can access the network services |
|    6    | Presentation Layer | Ensures that data is in a usable format and is where data encryption occurs          |
|    5    | Session Layer      | Maintains connections and is responsible for controlling ports and sessions          |
|    4    | Transport Layer    | Transmits data using transmission protocols including TCP and UDP                    |
|    3    | Network Layer      | Decides which physical path the data will take                                       |
|    2    | Data Link Layer    | Declines the format of data on the network                                           |
|    1    | Physical Layer     | Transmits raw bit stream over the physical medium                                    |

We'll describe OSI layers “top down” from the application layer that directly
serves the end user, down to the physical layer.

#### 7. Application Layer

The application layer is used by end-user software such as web browsers and
email clients. It provides protocols that allow software to send and receive
information and present meaningful data to users. A few examples of application
layer protocols are the Hypertext Transfer Protocol (HTTP), File Transfer
Protocol (FTP), Post Office Protocol (POP), Simple Mail Transfer Protocol
(SMTP), and Domain Name System (DNS).

The Application Layer in the OSI model is the layer that is the “closest to the
end user”. It receives information directly from users and displays incoming
data to the user. Oddly enough, applications themselves do not reside at the
application layer. Instead the layer facilitates communication through lower
layers in order to establish connections with applications at the other end. Web
browsers (Google Chrome, Firefox, Safari, etc.) TelNet, and FTP, are examples of
communications that rely on Layer 7.

#### 6. Presentation Layer

The presentation layer prepares data for the application layer. It defines how
two devices should encode, encrypt, and compress data so it is received
correctly on the other end. The presentation layer takes any data transmitted by
the application layer and prepares it for transmission over the session layer.

The Presentation Layer represents the area that is independent of data
representation at the application layer. In general, it represents the
preparation or translation of application format to network format, or from
network formatting to application format. In other words, the layer “presents”
data for the application or the network. A good example of this is encryption
and decryption of data for secure transmission; this happens at Layer 6.

#### 5. Session Layer

The session layer creates communication channels, called sessions, between
devices. It is responsible for opening sessions, ensuring they remain open and
functional while data is being transferred, and closing them when communication
ends. The session layer can also set checkpoints during a data transfer—if the
session is interrupted, devices can resume data transfer from the last
checkpoint.

When two computers or other networked devices need to speak with one another, a
session needs to be created, and this is done at the Session Layer. Functions at
this layer involve setup, coordination (how long should a system wait for a
response, for example) and termination between the applications at each end of
the session.

#### 4. Transport Layer

The transport layer takes data transferred in the session layer and breaks it
into “segments” on the transmitting end. It is responsible for reassembling the
segments on the receiving end, turning it back into data that can be used by the
session layer. The transport layer carries out flow control, sending data at a
rate that matches the connection speed of the receiving device, and error
control, checking if data was received incorrectly and if not, requesting it
again.

The Transport Layer deals with the coordination of the data transfer between end
systems and hosts. How much data to send, at what rate, where it goes, etc. The
best known example of the Transport Layer is the Transmission Control Protocol
(TCP), which is built on top of the Internet Protocol (IP), commonly known as
TCP/IP. TCP and UDP port numbers work at Layer 4, while IP addresses work at
Layer 3, the Network Layer.

#### 3. Network Layer

The network layer has two main functions. One is breaking up segments into
network packets, and reassembling the packets on the receiving end. The other is
routing packets by discovering the best path across a physical network. The
network layer uses network addresses (typically Internet Protocol addresses) to
route packets to a destination node.

Here at the Network Layer is where you’ll find most of the router functionality
that most networking professionals care about and love. In its most basic sense,
this layer is responsible for packet forwarding, including routing through
different routers. You might know that your Boston computer wants to connect to
a server in California, but there are millions of different paths to take.
Routers at this layer help do this efficiently.

#### 2. Data Link Layer

The data link layer establishes and terminates a connection between two
physically-connected nodes on a network. It breaks up packets into frames and
sends them from source to destination. This layer is composed of two
parts—Logical Link Control (LLC), which identifies network protocols, performs
error checking and synchronizes frames, and Media Access Control (MAC) which
uses MAC addresses to connect devices and define permissions to transmit and
receive data.

The Data Link Layer provides node-to-node data transfer (between two directly
connected nodes), and also handles error correction from the physical layer. Two
sublayers exist here as well--the Media Access Control (MAC) layer and the
Logical Link Control (LLC) layer. In the networking world, most switches operate
at Layer 2. But it’s not that simple. Some switches also operate at Layer 3 in
order to support virtual LANs that may span more than one switch subnet, which
requires routing capabilities.

#### 1. Physical Layer

The physical layer is responsible for the physical cable or wireless connection
between network nodes. It defines the connector, the electrical cable or
wireless technology connecting the devices, and is responsible for transmission
of the raw data, which is simply a series of 0s and 1s, while taking care of bit
rate control.

At the bottom of our OSI model we have the Physical Layer, which represents the
electrical and physical representation of the system. This can include
everything from the cable type, radio frequency link (as in a Wi-Fi network), as
well as the layout of pins, voltages, and other physical requirements. When a
networking problem occurs, many networking pros go right to the physical layer
to check that all of the cables are properly connected and that the power plug
hasn’t been pulled from the router, switch or computer, for example.

### Why you need to know the 7 OSI layers

Most people in IT will likely need to know about the different layers when
they’re going for their certifications, much like a civics student needs to
learn about the three branches of the US government. After that, you hear about
the OSI model when vendors are making pitches about which layers their products
work with.

In a Quora post asking about the purpose of the OSI model, Vikram Kumar answered
this way:

“The purpose of the OSI reference model is to guide vendors and developers so
the digital communication products and software programs they create will
interoperate, and to facilitate clear comparisons among communications tools.”

While some people may argue that the OSI model is obsolete (due to its
conceptual nature) and less important than the four layers of the TCP/IP model,
Kumar says that “it is difficult to read about networking technology today
without seeing references to the OSI model and its layers, because the model’s
structure helps to frame discussions of protocols and contrast various
technologies.”

If you can understand the OSI model and its layers, you can also then understand
which protocols and devices can interoperate with each other when new
technologies are developed and explained.

### Advantages of the OSI Model

#### The OSI model helps users and operators of computer networks:

- Determine the required hardware and software to build their network.
- Understand and communicate the process followed by components communicating
  across a network.
- Perform troubleshooting, by identifying which network layer is causing an
  issue and focusing efforts on that layer.

#### The OSI model helps network device manufacturers and networking software vendors:

- Create devices and software that can communicate with products from any other
  vendor, allowing open interoperability
- Define which parts of the network their products should work with.
- Communicate to users at which network layers their product operates – for
  example, only at the application layer, or across the stack.

### OSI vs. TCP/IP Model

<div style='text-align:center'>
<table>
<thead>
<tr>
<th style='text-align:center'>OSI Model</th>
<th style='text-align:center'>TCP/IP Model</th>
<th style='text-align:center'>TCP/IP Protocol Suite</th>
</tr>
</thead>
<tbody>
<tr>
<td>Application Layer</td>
<td rowspan=3>Application Layer</td>
<td rowspan=3>HTTP, SMTP, Telnet, FTP, DNS, RIP, SNMP</td>
</tr>
<tr>
<td>Presentation Layer</td>
</tr>
<tr>
<td>Session Layer</td>
</tr>
<tr>
<td>Transport Layer</td>
<td>Transport Layer</td>
<td>TCP UDP</td>
</tr>
<tr>
<td>Network Layer</td>
<td>Internet Layer</td>
<td>ARP, IP, IGMP, ICMP</td>
</tr>
<tr>
<td>Data Link Layer</td>
<td rowspan=2>Network Access<br/>Layer</td>
<td rowspan=2>Ethernet, Token Ring, ATM, Frame Relay</td>
</tr>
<tr>
<td>Physical Layer</td>
</tr>
</tbody>
</table>
</div>

The Transfer Control Protocol/Internet Protocol (TCP/IP) is older than the OSI
model and was created by the US Department of Defense (DoD). A key difference
between the models is that TCP/IP is simpler, collapsing several OSI layers into
one:

- OSI layers 5, 6, 7 are combined into one Application Layer in TCP/IP
- OSI layers 1, 2 are combined into one Network Access Layer in TCP/IP – however
  TCP/IP does not take responsibility for sequencing and acknowledgement
  functions, leaving these to the underlying transport layer.

Other important differences:

- TCP/IP is a functional model designed to solve specific communication
  problems, and which is based on specific, standard protocols. OSI is a
  generic, protocol-independent model intended to describe all forms of network
  communication.
- In TCP/IP, most applications use all the layers, while in OSI simple
  applications do not use all seven layers. Only layers 1, 2 and 3 are mandatory
  to enable any data communication.

[Content Sourece](https://www.imperva.com/learn/application-security/osi-model/)
[Content Source](https://www.networkworld.com/article/3239677/the-osi-model-explained-and-how-to-easily-remember-its-7-layers.html)
