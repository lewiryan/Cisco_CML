# Requirements:  
CML 2.8+
Free-Tier

# In this Lab:
We are Using a three (3) IOL routers with eBGP and iBGP config. This is a simple lab to get you started into the world of BGP.

- Verify that BGP is **Established** 
- Which routers are using iBGP and which ones are using eBGP?
- Why don't we have any routes in our routing table besides directly connected routes if BGP is established?


### Helpful Commands:
```
show ip bgp neighbors | include BGP
show ip bgp summary

```

## History of BGP

The Border Gateway Protocol (BGP) has evolved significantly since its inception. Here are some key milestones in its history:

- **1989**: BGP was first introduced in RFC 1105 by Yakov Rekhter and Kirk Lougheed. This initial version, known as BGP-1, was designed to replace the Exterior Gateway Protocol (EGP) and provide a more robust and scalable routing protocol for the internet.
- **1990**: BGP-2 was introduced in RFC 1163, which included improvements and bug fixes from the initial version.
- **1991**: BGP-3 was specified in RFC 1267, further refining the protocol and addressing additional issues identified in earlier versions.
- **1994**: BGP-4, the current version of the protocol, was introduced in RFC 1654. BGP-4 added support for Classless Inter-Domain Routing (CIDR), which allowed for more efficient use of IP address space and improved scalability.
- **1995**: RFC 1771 replaced RFC 1654, providing further clarifications and updates to BGP-4.
- **2006**: RFC 4271 was published, which is the current standard for BGP-4. This RFC consolidated and updated previous BGP-4 specifications, providing a comprehensive and detailed description of the protocol.

Over the years, numerous extensions and enhancements have been proposed and implemented to address emerging requirements and challenges in internet routing. BGP continues to be a critical component of the internet's infrastructure, enabling efficient and reliable routing between Autonomous Systems.


## Key Features of BGP
- **Path Vector Protocol**: BGP uses a path vector mechanism to maintain the path information that gets updated dynamically as the network topology changes.
- **Scalability**: BGP is designed to handle a large number of routes, making it suitable for the global internet.
- **Policy-Based Routing**: BGP allows for complex routing policies based on various attributes like AS path, next-hop IP address, and more.
- **Loop Prevention**: BGP uses the AS path attribute to prevent routing loops.

## Types of BGP
- **External BGP (eBGP)**: Used for routing between different Autonomous Systems.
- **Internal BGP (iBGP)**: Used for routing within the same Autonomous System.

## BGP Attributes
- **AS Path**: Lists the ASes that routing information has passed through.
- **Next Hop**: Indicates the next hop IP address to reach a destination.
- **Local Preference**: Used to prefer an exit point from the AS.
- **MED (Multi-Exit Discriminator)**: Suggests the preferred route into an AS when multiple entry points exist.
- ... FYI there are more but theses are the most common.

## BGP Operations
- **Establishing BGP Sessions**: BGP peers establish a TCP connection on port 179 to exchange routing information.
- **Route Advertisement**: BGP routers advertise routes to their peers.
- **Route Selection**: BGP uses various attributes to select the best route to a destination.

## Common BGP Issues
- **Route Flapping**: Frequent changes in route availability can cause instability.
- **BGP Hijacking**: Malicious actors can advertise incorrect routes, leading to traffic misdirection.
- **Configuration Errors**: Misconfigurations can lead to routing issues and network outages.

## Conclusion
BGP is a critical protocol for the functioning of the internet, enabling efficient and scalable routing between different networks. Understanding its features, operations, and potential issues is essential for network engineers and administrators.

## Sources
- Rekhter, Y., & Lougheed, K. (1989). RFC 1105: A Border Gateway Protocol (BGP). Retrieved from https://tools.ietf.org/html/rfc1105
- Rekhter, Y., & Lougheed, K. (1990). RFC 1163: A Border Gateway Protocol (BGP-2). Retrieved from https://tools.ietf.org/html/rfc1163
- Rekhter, Y., & Lougheed, K. (1991). RFC 1267: A Border Gateway Protocol 3 (BGP-3). Retrieved from https://tools.ietf.org/html/rfc1267
- Rekhter, Y., & Li, T. (1994). RFC 1654: A Border Gateway Protocol 4 (BGP-4). Retrieved from https://tools.ietf.org/html/rfc1654
- Rekhter, Y., & Li, T. (1995). RFC 1771: A Border Gateway Protocol 4 (BGP-4). Retrieved from https://tools.ietf.org/html/rfc1771
- Rekhter, Y., Li, T., & Hares, S. (2006). RFC 4271: A Border Gateway Protocol 4 (BGP-4). Retrieved from https://tools.ietf.org/html/rfc4271

