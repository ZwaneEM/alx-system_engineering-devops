<h1> 0. Simple web stack </h1>

<h2> Specifics </h2>

<h3> What is a server </h3><br>

-> A server is a computer or software that provides functionality or service
to other computers, known as clients over a network.

<h3>What is the role of the domain name? </h3><br>

-> A domain name serves as a human-readable label for identifying websites
of the internet

<h3> What type of DNS record is "www" in "www.foobar.com"</h3><br>

-> 'www' typically represents a subdomain in a domain name. It represents
as a CNAME (Canonical Name) record pointing to the main domain

<h3> What is the role of the web server ? </h3><br>

-> A web server is a software responsible for serving web pages to user in
response to their requests sent via HTTP (Hypertext Transfer Protocol)

<h3> What is the role of the application server ? </h3><br>

-> An application server is responsible for handling the logic and processing
required to provide dynamic content or perform specific tasks for the web
application.


<h3> What is the role of the database ? </h3><br>

-> A database is a structured collection of data that is organized in a way
that facilitates efficient storage, retrival, and management of information.

<h3> What is the server using to communicate with the computer 
of the user requsting the website ? </h3><br>

-> The server communicates with the user's computer over the internet using
HTTP or its secure variant HTTPS.

-> HTTPS  adds a layer of encryption using SSL/TLS (Secure Socket Layer/
Transport Later Security) to ensure secure communication.

<br>
<h2> Issues with the structure </h2><br>

<h3>SPOF</h3><br>

Having only one server means that if any componet of the system fails, 
the entire service becomes inaccessible.

<h3> Downtime During Maintenance </h3><br>

When maintenance is required, such as deploying new code that necessitates restarting the web server, the website will experience downtime. Since there's only one server handling both the web server and the application server, any maintenance operation affecting the server will result in service interruption for users accessing the website.

<h3>Inability to scale with increased Traffic </h3><br>

With only one server in place, the infrastructure lacks scalability. If there's a sudden surge in incoming traffic, the single server may struggle to handle the increased load effectively.
