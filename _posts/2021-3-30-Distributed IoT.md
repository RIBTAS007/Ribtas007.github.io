---
layout: post
title: "Distributed IoT"
description: In this article we will deep dive into distributed IoT
image: /files/blogs/Iot/Iot7.jpg
date: 2021-3-30
categories: post
tags: [IoT, Blockchain]
---

The Internet of Things (IoT) is a term that describes the connected devices and sensor technology that uses secure network access and cloud infrastructure to reliably turn data into sound knowledge for individuals, companies, and organizations. Modern IoT architectures needed a combination of clustered and distributed systems, with parallel computing clustered resources deployed as network nodes. At the edge interacting with a heterogeneous mesh topology of devices, to achieve distributed computation and storage over a vast area network. 


<img src="{{ site.url }}/files/blogs/Iot/Iot1.jpg" width="100%">

In general, the IoT refers to an environment that captures data from a variety of devices (computers, cars, smartphones, traffic lights, and applications (who might span from a social networking app like Twitter to an e-commerce platform, from a job shop to a traffic control system). Nonetheless, data alone is ineffective. It isn't significant unless it can be interpreted and transformed into information. This data is commonly required to be exchanged with other devices or applications to produce business value. Consequently, we need to trust in the massive amount of data generated and exchanged between systems.  Blockchain-defined technologies like distributed ledgers and smart contracts can help with distributed computing and storage.  Blockchain and its potential for building confidence in distributed environments without authorities' need is a technological innovation with the potential to transform many industries, including the Internet of Things.


<img src="{{ site.url }}/files/blogs/Iot/Iot2.jpg" width="100%">

Innovative, connected products' compelling features not only reshape industry profitability, but they can often expand the definition of the industry itself. An industry's overall boundaries widen to provide a group of related products that, because once combined, meet a broader underlying requirement. The function of one product is enhanced with the addition of other related products. Integrating intelligent, connected farm equipment, such as tractors, tillers, and planters, can improve overall equipment performance. As a result, the basis of competition shifts from the functionality of a discrete product to the more extensive product system's performance, in which the firm is only one actor. The manufacturer can now provide a package of connected equipment and related services that improve overall results.

## Problem with Non-Distributed IOT systems

There are numerous obstacles to widespread IoT adoption. These are primarily due to the current internet's design and the intermittent connectivity of today's networks. The factors listed apply to IoT systems and also have a consequence on their architecture and implementation:

1.	**Scalability**: The scale for IoT systems applies in terms of the number of sensors and actuators connected to the system, the networks that attach them, the amount of data related to the design and its speed of movement, and the proportion of processing power required.

2.	**Big Data**: Some of the more advanced IoT systems rely on massive amounts of data analysis. For example, there is a need to extract patterns from historical data to guide future actions. Another example of research that necessitates extensive processing is the extraction of useful information from complex data, such as video.

3.	**Cloud computing**: The use of cloud computing platforms in IoT systems is widespread. Cloud computing systems enable vast quantities of resources to be used, both in terms of data storage and the ability to bring versatile and scalable processing resources to data analysis. IoT systems would almost certainly need a variety of processing software. Cloud providers' adaptability is required to cope with new specifications, firmware or device upgrades, and new features over time.

4.	**Real time**: IoT systems often run in real-time; data about current events is continuously streamed in and may need prompt responses to the stream of events. This includes stream processing, which involves acting on event data as it arrives, comparing it to previous events, and static data to respond appropriately. There is also a need to ensure that compromised data is detected and not used — whether due to faulty sensors or malicious intent — because the use of corrupted data could damage people, equipment, and the environment.

5.	**Highly distributed**: Internet of Things (IoT) systems can span entire houses, entire cities, and even the entire globe. Data that can be stored at the network's edge or centralized can also be spread widely. Processing may also be distributed — some processing is done centrally (in cloud services). Still, processing can also be done at the network's edge, in IoT gateways, or even inside (more capable types of) sensors and actuators. There are now reportedly more mobile devices on the planet than humans. One of the most well-known IoT devices and systems are mobile devices and networks.

6.	**Heterogeneous systems**: IoT systems are often constructed from a diverse collection of components. This is true not only for the sensors and actuators but also for the various networks and processing components involved. Low-power sensors are popular, and these devices often communicate via specialized local networks. An IoT gateway is used to provide internet-scale connectivity to such applications.

7.	**Security and Privacy**: The security and trustworthiness of distributed heterogeneous IoT systems is a complex problem with solutions that must scale and develop along with the systems. Data security is essential, and there are serious privacy issues about data that relate to individuals. It's challenging to assure that these systems are safe, stable, and resilient and meet their stakeholders' privacy expectations. 

8.	**Compliance**: Providing trust in the operation of these IoT systems is needed due to industry, sector, and vertical regulations, as well as the norms and expectations of the IoT systems' stakeholders.

9.	**Integration**: IoT systems do not operate in isolation; they must link to existing operational technology systems, such as intelligent automation, building control systems, and other forms of physical management systems, as well as business systems, such as enterprise applications and databases.

## Types of IoT Architecture

There are mainly three types of IoT Architectures: 

**Centralized systems**: The most popular model for software applications right now is centralized systems. From a single location, centralized structures monitor the operation of individual units and the flow of information. To send and receive information and be ordered, everyone is utterly reliant on the central power. For knowledge exchange, the central network owner acts as a single point of contact. The most significant disadvantage of a centralized network is that it becomes a single point of failure because there is only one central owner. Furthermore, with only one copy stored with the owner, any access to the resource results in an access problem over time.


<img src="{{ site.url }}/files/blogs/Iot/Iot3.jpg" width="100%">

**Decentralized Systems**: All of the components of a decentralized, non-distributed (or co-located) system are physically located in the exact location. There are many central owners who have copies of the capital. With a centralized network, this removes the most severe issue of a single point of failure. When there are many owners, they can still access the other nodes' information if one of the central nodes fails. Furthermore, having several owners increases the speed at which they can access data. Decentralized systems are the backbone of parallel and cluster computing. Multiple processors on a network will execute the same instruction set on different parts of the same (shards) or other datasets.
Thus, a decentralized system is basically a communication network of collection of mostly autonomous processors (nodes) and having the following features:
*	**Individual objectives**: The nodes are working on individual goals that may or may not need to be organized in order to achieve the desired outcome (e.g., map-reduce)
*	**Loosely coupled nodes**: the network's nodes should be loosely coupled.
*	**Direct synchronization with other network nodes**: all network nodes should be synchronized using the same clock.
*	**Shared memory**: The network's nodes can store intermediate state and data in shared memory space.
*	**Geographical distribution**: If data redundancy is needed, the network nodes should be collocated with a minimum geographical distribution.
*	**Homogeneity**: The network's nodes should preferably be self-contained and heterogeneous.

**Distributed Systems**: The nodes in a distributed network are not only geographically distributed but also collocated. It prevents centralization. The fundamental principle of the distributed network is that everyone has access, and everyone has fair access. If any active device is connected to the internet and has an IP address, any active such as a laptop, phone, or printer, can serve as a node Binary trees are made up of nodes that are arranged in a tree structure. These transactions will necessitate a significant amount of computing and processing capacity, which means that the average computer's capabilities are insufficient. Every node on the network is given importance, but some nodes perform different functions in terms of network support.


<img src="{{ site.url }}/files/blogs/Iot/Iot4.jpg" width="100%">
 
## Distributed IoT

A distributed system where nodes are communicating over a communication network and are a collection of mostly autonomous processors (nodes). Then they can have the following characteristics: 


<img src="{{ site.url }}/files/blogs/Iot/Iot5.jpg" width="100%">

*	**Usual goal**: the nodes are working to achieve a usual goal that can be achieved using only multiple processor
* **Loosely coupled**: the nodes on the network should be able to communicate using a standard protocol via a messaging system and should be loosely coupled 
*	**No direct synchronization with other network nodes**: the network nodes should not be synchronized via a common clock
*	**Distributed memory**: if possible, the network nodes should not have a shared memory space, but shared distributed memory space for the entire system can be provided as an abstraction
*	**Geographical distribution**: the network nodes should avoid any centralization and should be geographically distributed
*	**Autonomy and heterogeneity**: the network of nodes should be heterogeneous in nature and should be autonomous


<img src="{{ site.url }}/files/blogs/Iot/Iot6.jpg" width="100%">

The majority of today's IoT architectures depend on centralized cloud computing. A distributed approach's attractive property is that it can run software in parallel among the nodes and close to where the computing is required, minimizing data transmission between the individual nodes. This approach broadens the definition of "the cloud" beyond data centres to include all computing resources, from massive data centres to consumer devices at the network's edge. In effect, this computing method produces a cloud fabric that is millions of times larger than the current central cloud infrastructure. The result is an emerging swarm of services that use computing resources as required, from edge nodes in clusters to large server nodes in data centres, which provides the protection, privacy, convergence, and enforcement that IoT architectures demand.

Distributed computing, like other computer science fields, is not accessible; it covers various topics from the practical to the theoretical. On the hypothetical hand, distributed computing provides a plethora of mathematically intriguing problems in which an algorithm is pitted against an opponent who portrays the system's unpredictability. Since executions include a complex relationship between the algorithm's actions and the system's responses, the study of distributed algorithms often has a robust game-theoretic flavour. A synchronous framework, in which all nodes work in lockstep, is the most basic form of distributed computing. This model is commonly known as the LOCAL model.

For each communication round, all nodes in parallel
1.	receive the most recent messages from their neighbours
2.	perform arbitrary local computation, and
3.	electing a leader
4.	and then sending new messages to their neighbours.

The number of communication rounds needed to complete the task is a crucial complexity measure in such systems. This is the execution of state machines in a distributed system where each node performs an arbitrary local computation and then communicates the results to other nodes to be organized in the appropriate order for the next round of calculations. The practical issue of distributed computing is that such a system cannot be inherently scalable or real-time, nor can it provide real-time analytics of data streams that may be required to cause subsequent computations. There's also a need for historical l data analysis that can be used to guide potential artificial intelligence decisions, and this decision-making can take place as close to the computing node as possible to minimize latency.

## Conclusion


<img src="{{ site.url }}/files/blogs/Iot/Iot7.jpg" width="100%">

Modern IoT architectures needed a combination of clustered and distributed systems in which clusters of parallel computing resources deployed at the edge interact with a collection of network nodes as a mesh topology of heterogeneous devices deployed as to achieve distributed computation and storage over a vast area network. Blockchain-defined technologies like distributed ledgers and smart contracts can help with distributed computing and storage. The Distributed IoT can help to optimize the overall system by removing the cons of centralized system and adding new features that provide flexibility to the overall system.

## References

*	https://medium.com/@prashunjaveri/rethinking-iot-architecture-the-need-for-distributed-systems-architecture-for-the-internet-of-ad967d19eae
*	Images taken from google Images
*	https://www.researchgate.net/publication/327674199_Distributed_IoT_and_Applications_A_Survey
