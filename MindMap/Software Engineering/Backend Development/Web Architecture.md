# History
- In December of 1990, Tim Berners-Lee started a non-profit software project that he called “World Wide Web.”
-  Berners-Lee had invented and implemented:
	- The [[URI|Uniform Resource Identifier]] ([[URI]]), a syntax that assigns each web document a unique address.
	- The [[HyperText Transfer Protocol]] ([[HTTP]]), a message-based language that computers could use to communicate over the Internet.
	- The [[HyperText Mark-up Language]] ([[HTML]]), to represent informative documents that contain links to related documents.
	- The first [[web server]].
	- The first web browser, which Berners-Lee also named “World Wide Web” and later renamed “Nexus” to avoid confusion with the Web itself.
	- The first WYSIWYG [[HTML]] editor, which was built right into the browser.
- The World Wide Web (W3) is a wide-area hypermedia information retrieval initiative aiming to give universal access to a large universe of documents.
- From that moment, the Web began to grow, at times exponentially.
- The Web’s traffic was outgrowing the capacity of the Internet infrastructure.
- In late 1993, Roy Fielding, co-founder of the [[Apache]] [[HTTP]] Server Project, became concerned by the Web’s scalability problem.
- Upon analysis, Fielding recognized that the Web’s scalability was governed by a set of key constraints.
- Fielding worked alongside Tim Berners-Lee and others to increase the Web’s scalability. 
- To standardize their designs, they wrote a specification for the new version of the [[HTTP|HyperText Transfer Protocol]], [[HTTP]]/1.1.* They also formalized the syntax of [[URI|Uniform Resource Identifier]]s ([[URI]]) in RFC 3986.
- In the year 2000, after the Web’s scalability crisis was averted.
- Fielding named and described the Web’s architectural style in his Ph.D. dissertation.
- “[[REST API|Representational State Transfer]]” ([[REST API|REST]]) is the name that Fielding gave to his description of the Web’s architectural style, which is composed of the constraints outlined above.
# Web API Architectural Style Constraints
- The constraints, which Fielding grouped into six categories and collectively referred to
as the Web’s architectural style.
## Client-Server
- The web is a client-server based system, they have different roles, implementation and deployment, thy must conform to the Web's Uniform Interface. 
## Uniform Interface
- Interactions between web components depend on uniformity, which decouples the architecture, allowing each part to evolve independently, it has 4 guiding principles.
	- **Identification of resources**: resources are distinct web-based concepts that can be addressed by *unique identifiers*, such as [[URI]]s.
	- **Manipulation of resources through representations**: There are no direct interaction with the resource itself, but with a representation of it (like [[HTML]], [[JSON]], ... etc), allowing same resource to be represented in different ways without changing its identifier.
	- **Self-descriptive messages**: The messages must hold all data and metadata about the desired resource state (for the client) and current resource state (from the server), for [[HTTP]], this is provided through headers.
	- **Hypermedia as the engine of application state**: Resources are linked and connected together through hyperlinks, these links presence or absence is an important part of resource's state.
## Layered System
- Enabling network-based intermediaries (proxies, gateways, .... etc) to be *transparently* deployed between client and server using the Web’s **uniform interface**.
- Network-based intermediaries are commonly used for enforcement of **security**, **response caching**, and **load balancing**.
## Cache
- The [[web server]] is declaring the cache-ability of of each response data.
- Caching response data can help to **reduce client-perceived latency**, **increase the overall availability and reliability of an application**, and **control a web server’s load**.
- A cache may exist anywhere along the network path between the client and server. They can be in an organization’s [[web server]] network, within specialized [[content delivery network]]s (CDNs), or inside a client itself.
## Stateless
- The [[web server]] is not required to memorize the state client application.
- Disadvantage: client must include all contextual information with each interaction.
- Advantage: The server can serve a larger number of clients.
- This trade-off is the key contributor to scalability of Web's Architectural Style. 
## Code-On-Demand
- The [[web server]] is enabled to *temporarily* transfer executable programs such as scripts and plug-ins.
- Drawback: Technology coupling is created between client and server, since client will need to understand and execute the code.
- Conclusion: Code-On-Demand is the only **optional** constraint in Web's architectural style.