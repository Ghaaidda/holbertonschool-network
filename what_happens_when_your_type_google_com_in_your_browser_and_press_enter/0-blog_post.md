# What Happens When You Type https://www.google.com in Your Browser?

When a user types `https://www.google.com` into their browser and presses Enter, several processes take place before the requested webpage appears.

## 1. Understanding the URL

First, the browser parses the URL to identify its components:

- **HTTPS:** The protocol used to securely communicate with the web server.
- **www.google.com:** The domain name, consisting of the top-level domain (`com`), second-level domain (`google`), and subdomain (`www`).
- **Port 443:** The default port used for HTTPS connections.

## 2. DNS Resolution

The browser needs to determine the IP address associated with `www.google.com`.

It first checks available DNS caches. If the address is not cached, a DNS lookup is performed through a DNS resolver to obtain the server's IP address.

Once the browser has the destination IP address, it can begin establishing a connection.

## 3. TCP/IP Connection

The browser uses TCP/IP to communicate with the destination server over the internet.

IP is responsible for addressing and routing packets toward their destination, while TCP provides reliable, ordered delivery of data.

For a typical HTTPS connection over TCP, a three-way handshake takes place between the client and server to establish the connection.

Modern browsers may also use HTTP/3, which runs over QUIC instead of TCP.

## 4. HTTPS and TLS Encryption

Before exchanging HTTP data over a new TCP connection, the browser and server perform a TLS handshake.

During this process, the server presents its TLS certificate, which the browser validates to verify the server's identity.

The browser and server then establish encryption keys to secure their communication.

HTTPS protects the exchanged data from being read or modified by unauthorized parties during transmission.

## 5. Firewall and Load Balancer

When the request reaches Google's infrastructure, it passes through network security controls that filter traffic based on configured rules.

A load balancer may then distribute the request to an available backend server.

Load balancing helps distribute traffic across multiple servers, improving performance, scalability, and availability.

## 6. Web Server and Application Server

The web server receives and processes the HTTP request.

Depending on the requested resource, it may serve static content directly or forward the request to an application server.

The application server executes the required logic and may communicate with a database if the request requires stored information.

## 7. HTTP Response and Page Rendering

After processing the request, the server sends an HTTP response containing a status code, headers, and potentially the requested content.

The response travels back to the browser through the established connection.

The browser then processes the received HTML, CSS, and JavaScript to render the webpage. It may also send additional requests for images, scripts, stylesheets, and other resources needed to display the complete page.

## Conclusion

Loading a webpage involves several technologies working together, from DNS resolution and network communication to encryption, request processing, and browser rendering.

Although the process appears almost instantaneous to the user, each component plays an important role in making web communication reliable, secure, and efficient.
