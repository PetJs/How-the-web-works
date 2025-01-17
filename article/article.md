# How the Web Works and Web Protocols: How Popular Services are Implemented

## Architecture of the Web
The Web is a system of digital content and resources accessible through the internet. Web architecture refers to the design, creation, and implementation of internet-based programs. These programs often include websites containing information for users. Some of them also include web apps, progressive web apps (PWAs), and more. Despite their varying forms, they all serve the fundamental goal of delivering information tailored to users' needs.

---

## A Brief Flashback to the Origin of the Web
The World Wide Web (WWW) was conceptualized as a solution to communication challenges.

In 1989, **Tim Berners-Lee** introduced the web as a platform for sharing information and fostering collaboration. By 1990, he developed the first web server and browser at CERN. The Web was initially built using **Hypertext Markup Language (HTML)**, a language also invented by Berners-Lee.

This innovation sparked a revolution in technology, leading to the development of tools like **CSS** and **JavaScript**, which enhanced the web's capabilities over time.

---

## Web Architecture
Initially, the web operated on a simple two-tier architecture consisting of **clients** and **servers**. These two components worked together to fulfill user requests:

- **Clients**: Typically, users' devices (e.g., browsers) that request services or resources.
- **Servers**: Systems that respond to these requests by delivering the requested content or service.

This basic architecture laid the foundation for more complex and scalable systems that support the modern web.

![Web Architecture ](https://github.com/PetJs/How-the-web-works/blob/main/research/web-archi.jpg)

# Web Protocols: The Basis of the World Wide Web

The Web is guided by protocols that form the foundation of the World Wide Web (WWW). These protocols are primarily based on the **TCP (Transmission Control Protocol) / IP (Internet Protocol)** reference model. Below are some key protocols and standards:

- **Communication Formats**: Machines communicate using formats such as HTML, CSS, or XML.  
- **Data Transfer Protocols**: The Web uses HTTP (Hypertext Transfer Protocol) or HTTPS (Hypertext Transfer Protocol Secure) for transferring data.  
- **Standardized Addressing**: Web resources are identified using URLs (Uniform Resource Locators).  

---

## Understanding Key Protocols
Now you might wonder: what exactly do these protocols do? Let’s dive into the details of some of them.

---

### HTTP and HTTPS
Every time we access a URL, it is prefixed with either **HTTP** or **HTTPS**. Have you ever wondered why? While both are communication protocols, they serve slightly different purposes.

---

### HTTP (Hypertext Transfer Protocol)
**HTTP** stands for **Hypertext Transfer Protocol**, where hypertext refers to text encoded with HTML. HTTP establishes a standard for communication between a web browser (client) and a web server.

- **How it works**:  
  1. The client sends an HTTP request to the server.  
  2. The server responds with an HTTP response, often containing the requested content.  

- **Significance**:  
  HTTP defines rules for transferring data between computers, making it the backbone of web communication.

---

### HTTPS (Hypertext Transfer Protocol Secure)
**HTTPS** stands for **Hypertext Transfer Protocol Secure**. The key difference lies in the "S," which stands for **Secure**.

- **Key Features**:  
  - HTTPS adds an additional layer of security to HTTP by encrypting the data exchanged between the client and the server.  
  - This encryption is achieved using **SSL (Secure Sockets Layer)** or **TLS (Transport Layer Security)** protocols.  

- **Importance**:  
  - HTTPS is critical for transmitting sensitive and confidential information, such as personal details, passwords, or financial data.  

In essence, **HTTPS** is a combination of **HTTP** with encryption conventions (**SSL/TLS**) to ensure secure communication.

![HTTP/HTTPS](https://github.com/PetJs/How-the-web-works/blob/main/research/http-https.jpg)

# HTML

**HTML** stands for **HyperText Markup Language**. It is the standard language used to create and structure content on the web. As the most fundamental building block of the web, HTML instructs browsers on how to display text, links, images, and other forms of multimedia on a webpage.

![Bubble Text](https://github.com/PetJs/How-the-web-works/blob/main/research/bubble%20text.png)

---

## How HTML Works

HTML uses “markup” to annotate text, images, and other content for display in a Web browser. This markup includes special elements known as **tags**, such as:

- `<head>`  
- `<body>`  
- `<header>`  
- `<section>`  
- `<h1>`  
- `<p>`  
- `<div>`  
- `<nav>`  

---

## Sample HTML Code

Below is a sample code that demonstrates the basics of HTML:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Welcome to the Web!</title>
  </head>

  <body>
    <style type="text/css" media="all">
      h1 {
        color: blue;
      }
    </style>
    <h1>Hello World!</h1>
    <p>Welcome to a preview of how the first web looks like!</p>
    <a href="http://info.cern.ch/hypertext/WWW/TheProject.html">Link to the first webpage</a>
  </body>
</html>
```

![HTML preview](https://github.com/PetJs/How-the-web-works/blob/main/research/html%20source%20code%20preview.png)


# DNS

**DNS (Domain Name System)** is a hierarchical and decentralized naming system for internet-connected resources. DNS maintains a list of domain names along with the resources, such as IP addresses, that are associated with them.  
What this protocol does is that it takes a domain name (such as `www.risevest/academy`) to a numeric IP address (such as `172.67.166.2`).

---

# How Web Protocols Work Together: The Case of Netflix

![Netflix](https://github.com/PetJs/How-the-web-works/blob/main/research/netflix.jpg)

If you’re wondering how web protocols work together to create a simple web service, let’s examine Netflix as an example.  
Netflix is a streaming platform where users can stream, watch, and download movies. Here’s how it all comes together:

The interface you see—featuring movies, the search button, and the cards displaying all the available content—is built using HTML and CSS.  
- Netflix uses React, a JavaScript framework, for building dynamic and interactive components.  
- However, when the final interface is rendered in your browser, it is displayed in HTML form.

When you sign up, click the play button, or search for a movie, this interaction involves a web server:  
1. **HTTPS Requests**:  
   - When you take an action, such as searching for a movie, an HTTPS request is sent from your browser to Netflix's web server.  
   - The server processes the request and sends back an HTTPS response containing the required data (e.g., search results).  
2. **Client-Side Display**:  
   - The browser uses the response to display the information or perform the requested action, like playing a movie.

The **DNS (Domain Name System)** ensures your request is routed correctly:  
- When you enter `www.netflix.com`, the DNS translates the domain name into an IP address.  
- This directs your request to the nearest Content Delivery Network (CDN) or server.  
- By splitting traffic among multiple servers, DNS reduces the load on individual servers and ensures fast, reliable access.

Despite its scale, Netflix still follows the same basic protocols established in traditional web architecture. These include:  
- **HTML and CSS** for content display.  
- **HTTPS** for secure data transfer.  
- **DNS** for routing and load distribution.  

This same architecture applies to smaller web services, like JAMB or similar platforms, demonstrating the timeless effectiveness of these foundational protocols.

![A Sketch](https://github.com/PetJs/How-the-web-works/blob/main/research/sketch%20of%20netflix%20web%20architecture.PNG)
