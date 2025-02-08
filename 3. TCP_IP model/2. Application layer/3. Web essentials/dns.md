# DNS and Levels of Domain

## What is DNS (Domain Name System)?
**DNS (Domain Name System)** is like the phonebook of the internet. It translates human-readable domain names (like `google.com`) into machine-readable IP addresses (like `172.217.9.14`) so that computers can find each other and communicate over the internet.

### Example:
When you type `google.com` in your browser, DNS converts it to an IP address so that your browser can find Google's server and load the page.

---

# Levels of Domain

Domains have a hierarchical structure, and they are organized into different levels:

1. **Top-Level Domain (TLD)**:
   - This is the highest level in the domain hierarchy. Examples include:
     - `.com`, `.org`, `.net`, `.edu` (Generic TLDs)
     - `.gov`, `.mil` (Sponsored TLDs)
     - Country codes like `.us`, `.in`, `.uk` (Country Code TLDs)

   - **Example**: In `www.example.com`, `.com` is the TLD.

2. **Second-Level Domain (SLD)**:
   - This is the part of the domain that comes right before the TLD and usually represents the organization or business name.

   - **Example**: In `www.example.com`, `example` is the SLD.

3. **Subdomain**:
   - This is an optional part of the domain and is used to create more specific addresses under the main domain.

   - **Example**: In `blog.example.com`, `blog` is the subdomain.


---

# How Domain Lookup Works

Domain lookup is the process of finding the IP address associated with a domain name. Here's how it works:

1. **User Enters Domain in Browser**:
   - When you type a domain name (e.g., `www.example.com`) into your browser, the browser needs to find the corresponding IP address to connect to the website.

2. **DNS Query**:
   - The browser sends a DNS query to a **DNS resolver** (usually provided by your internet service provider or a public DNS service like Google DNS).

3. **Recursive Query Process**:
  - If the resolver doesn't have the domain cached, it first checks its local cache or queries its **ISP's DNS server** to see if the domain's IP address is already known.
  - If the ISP's DNS server doesn't have the information, it then queries the **root DNS server**.
  - The **root DNS server** directs the query to the appropriate **TLD (Top-Level Domain) nameserver** for the domain's TLD (e.g., `.com`, `.org`, etc.).
  - The TLD nameserver points the query to the **authoritative nameserver** for the specific domain (e.g., `example.com`).
  - The **authoritative nameserver** holds the actual DNS records and responds with the correct IP address for the domain (e.g., `www.example.com`).
  - Finally, the resolver returns the IP address to your browser, which can now establish a connection to the server hosting the website.


4. **Browser Connects to Server**:
   - Now that the browser has the IP address, it can send an HTTP request to the server hosting the website (using the IP address).
   - The server responds, and your browser displays the website.

### Example:
1. You type `www.example.com` into the browser.
2. The browser queries a DNS resolver to find the IP address of `www.example.com`.
3. The DNS resolver first checks its cache or asks its **ISP's DNS server** to find the IP address.
4. If the ISP’s DNS server doesn't have the IP address, the resolver queries the **root DNS server**.
5. The root DNS server directs the query to the **TLD (Top-Level Domain) nameserver** (e.g., for `.com`, `.org`, etc.).
6. The TLD nameserver then directs the query to the **authoritative nameserver** for the domain `example.com`.
7. The **authoritative nameserver** responds with the IP address (e.g., `192.0.2.1`).
8. The resolver returns the IP address to the browser, which then connects to the server at that IP address and loads the website.

---

# Summary
- **DNS** helps translate domain names (like `google.com`) into IP addresses so devices can connect.
- Domains have different levels: **TLD**, **SLD**, and **Subdomain**.
- To rent a domain, you register it through a domain registrar.
- **Domain lookup** involves querying a series of DNS servers to find the IP address of a domain.
- **Clients** connect to a domain by first finding its IP address via DNS and then establishing a connection to the server using that address.
