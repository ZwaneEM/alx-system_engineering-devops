<h1> 1. Distributed web infrastructure </h1>

<h3> Specifics: </h3>

<b>Every additional element, Why we added it?</b>

adding a new server to provide redundancy and fault tolerance. If one server fails
the second server can continue to serve the requests.

<b>What distribution algorithm your load balancer is configured with and how it works?</b>

Its using round-robin distribution algorithm. The algorithm is going to distribute
the requests Sequentially, Meaning the request are going to be divided evenly 
between the servers.

<b> Active-Active or Active-Passive setup:</b>

The servers are using a Active-Active setup where all the servers are actively serving
traffic. The difference is that in a Active-Passive setup the other servers remain
idle until the active server fails then the idle server takes over.

<b> Primary-Replica (Master-Slave) Database cluster work: </b>

In a Primary replica the primary node(master) accepts write operations and 
replicates data changes to replica node (slave)

<b> What is the difference between the Primary node and the Replica node in regards to the application?</b>

The primary node is responsible for handling the write operations and managing
the data changes. while the replica node replicates the data in the primary node
and handles the read only operations.

<h3> Issues with the Infrastructure </h3>

<b> SPOF (single point of failure):</b>

The main single point of failure is not having redundancy of components to 
cover when the main components fail (having only one load balancer).

<b>Security issues (no firewall, no HTTPS):</b>

Because of a lack of a firewall and any other security components the infrastructure
remains vulnerable to attacks and unauthorised access.

<b> No Monitoring:</b>

Without Monitoring, it makes it challenging to detect and address performance
issues
