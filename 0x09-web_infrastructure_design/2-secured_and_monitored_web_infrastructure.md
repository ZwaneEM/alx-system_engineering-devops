<h1> 2. Secured and monitored web infrastructure </h1>

<h3> Specifics </h3>

<h2> For every additional element, why you adding it </h2><br>

we have added a firewale for each server to protect them from being
attacked and exploited, 1 SSL certificate to serve the site over HTTPS and
threee monitoring clients that will collect logs and send them to the data
collector Sumlogic.

<br>
<h2> What are firewalls for </h2><br>

Is a network security system that monitors and controls incoming and
outgoing network traffic based on predetermined security rules.

<br>
<h2> Why is the traffic served over HTTPS: </h2><br>

Becaused previously the traffic was passed over HTTP which transfers data in
plain text while HTTPS is secure where the data is encrypted using SSL

<br>
<h2> What monitoring is used for </h2><br>

It provides the capability to detect and diagnose any web application
performance issues proactively.

<br>
<h2> How the monitoring tool is collecting data: </h2><br>

It collects logs of the application server, MYSQL database and the web server.

<br>
<h2> Explain what to do if you want to monitor your web server QPS: </h2><br>

One web server handles 1K queries per second, i would basically nonitor it 
from the network and application level.

<hr><br>

<h3> Issues </h3><br>

<h2> Why terminating SSL at the load balancer level is an issue </h2><br>

It is an issue because decryption is resource and CPU intensive. Placing the
decryption burden on the load balancer enables the server to spend processing
power on application tasks

<br>
<h2> Why having only one MySQL server capable of accepting write is an issue</h2><br>

Because once it goes down it means data wont be able to be recorded in the
entire infrastructure

<br>
<h2> Why having servers with all the same componets(database, webserver and
application server) might be a problem </h2><br>

This is because once you have a bug in one of the components in one of the
servers then the bug will be valid in the other servers.
