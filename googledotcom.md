# What Happens when you type Google.com and press enter?
When you type "google.com" into your browser’s address bar and hit enter, a series of complex processes are triggered behind the scenes, resulting in the webpage loading and you being able to start searching. While the entire process is highly optimized and happens in milliseconds, it involves several key steps.Let’s break down what happens in a bit of technical detail.

## 1.Domain Name System (DNS) Lookup
 When you type Google.com or any domain name in your browser on your computer or device what really happens is, a request is sent to the domain name system (DNS) server which serves as an address book for all domain names. This then sends back the exact IP address of the server which https://www.google.com points to. This address will be like 123.122.130.3 rendering these numbers for humans is not possible to remember, hence the need for servers known as Domain Name System Servers. The domain names are a way for humans to remember easily for e.g Google.com, twitter.com, etc.
 If you had accessed google.com or twitter.com earlier, the browser first checks its cache to see if it has a recent record of that domain name.
 If there is a recent copy of the DNS records for that domain, it will use the IP address in the cache to send a request to the server. This speeds up the process of resolving the domain name to an IP address because it avoids the need to send a request to the DNS server.
 If the browser cache does not find a copy of the recent record of the requested domain, or if the DNS record has changed since the last time it was cached, the browser will send a request to the DNS server to resolve the domain name to an IP address.

 ## 2.TCP/IP Connection
 Once the IP address is obtained, your browser establishes a connection to the Google servers using the Transmission Control Protocol (TCP) over Internet Protocol (IP).Once your computer has the IP address for www.google.com or the URL you are looking for, TCP is a protocol that ensures that the data sent between your computer and Google’s server or domain name you are looking for is delivered correctly, while IP is a protocol that ensures that the data is sent to the correct destination. This is like communication between the browser and server with the domain name you are looking for, and when the server receives the request it sends back a message acknowledging the request to establish a connection. This is like the handshake process.The server finally sends back the requested URL e.g Google.com with HTML code to the browser using TCP. The browser receives the HTML code and uses it to render the webpage on your screen. Any resources (such as images) that the webpage needs are also requested and received using TCP/IP.

 ## 3.Firewall
 To protect themselves from hackers and attacks, servers are often equipped with a firewall. A firewall is a software that sets rules about what can enter or leave a part of a network. In the case of our example, when the browser asks for the website at the address 54.172.4.191, that request has be processed by a firewall which will decide if it’s safe, or if it’s a threat to the server’s security. The browser itself can also be equipped with a firewall to detect if the IP given by the DNS request is a potential malicious agent.

 ## 4.HTTPS/SSL
 Now that the browser has the IP address, it is going to take care of the other part of the URL, the https:// part. HTTPS stands for HyperText Transfer Protocol Secure, and is a secure version of the regular HTTP. This transfer protocol defines different types of requests and responses served to clients and servers over a network. In other terms, it’s the main way to transfer data between a browser and a website. HTTP and HTTPS requests include GET, POST, PUT, and others. The HTTPS requests and responses are encrypted, which ensure the users that their data can’t be stolen or used by third-parties. For example, if we put our credit card information in a website that uses HTTPS, we are guaranteed that this info is not going to be stored in plain text somewhere accessible to anybody.

Another key component in securing websites is the SSL certificate. SSL stands for Secure Sockets Layer (also known as TSL, Transport Layer Security). The certificate needs be issued from a trusted Certificate Authority, like the famous Let’s Encrypt for example, which gives free SSL certificates. When a website has this certificate, we’re able to see a little lock icon next to the website name in the search bar. On some browsers and with certain types of SSL certificates, the bar turns green.

## 5.Load Balancer
 A load-balancer is a device that distributes incoming network traffic across multiple servers. For most website where the traffic is consequent, it would be impossible to be hosted on a single server. Plus, it would create a Single Point of Failure (SPOF), because it would only need one attack on said server to take the whole site down.As needs for higher availability and security rises, websites started augmenting the number of servers they have, organizing them in clusters, and using load-balancers.
 This is how a load balancer works in the case of a browser trying to access google.com, the load balancer would receive the incoming request from the browser and then forward it to one of the servers in the Google server network. This will also work the same way for any domain name you are trying to search for.

 ## 6.Web Server
 So Once the request is received by one of Google’s servers or the domain URL server you were looking for from the load balancer, it is passed to a web server. The web server is responsible for processing the request, generating the HTML, CSS, and JavaScript that make up the webpage, and sending it back to your browser for you to see it.

 ## 7.Application Server
 Most sites don’t just want a static page where no interaction is happening, and most websites are dynamic. That means that it’s possible to interact with the site, save information into it, log in with a user name and a password, etc.
This is made possible by the use of one or more application servers. These are software programs responsible for operating applications, communicate with databases and manage user information, among other things. they work behind web servers and will be able to serve a dynamic application using the static content from the web server.

## 8.Database
If the request requires data from a database, the request is passed to a database server. The database server is responsible for storing, organizing, and retrieving data. This allows websites to provide personalized content and store user data.

## Rendering
The HTTP response makes its way back through the channels, reaching your browser which then renders the HTML, CSS, and JavaScript to display the webpage we all know and love as Google.
This orchestrated sequence of events, though appearing instantaneous to us, embodies a marvel of engineering and a testament to the boundless possibilities within the realm of technology.
