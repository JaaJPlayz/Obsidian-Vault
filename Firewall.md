### **Firewalls: Key Concepts & Information**

A **firewall** is a network security device that monitors and controls incoming and outgoing network traffic based on predetermined security rules. It acts as a barrier between a trusted internal network and untrusted external networks, such as the internet.

---

### **Types of Firewalls**

1. **Packet-Filtering Firewalls**
    
    - **Function**: Inspects packets at the network layer (Layer 3) and the transport layer (Layer 4) to determine whether they should be allowed or blocked based on predefined rules (e.g., source IP, destination IP, ports, and protocols).
    - **Strengths**: Simple, fast, and lightweight.
    - **Weaknesses**: Limited security; cannot inspect the content of the packet (e.g., payload).
2. **Stateful Inspection Firewalls**
    
    - **Function**: Monitors the state of active connections and makes decisions based on the context of traffic (i.e., whether a packet is part of an established connection or not).
    - **Strengths**: More secure than packet-filtering because it tracks the state of connections.
    - **Weaknesses**: Requires more resources and configuration compared to packet filtering.
3. **Proxy Firewalls (Application-Level Gateways)**
    
    - **Function**: Acts as an intermediary between users and the services they access. It can inspect the entire packet, including the data (payload), and can enforce security policies based on the application layer (Layer 7).
    - **Strengths**: Offers deep packet inspection, provides control over application-layer traffic, and hides internal network addresses.
    - **Weaknesses**: Can introduce latency, and requires more processing power.
4. **Next-Generation Firewalls (NGFW)**
    
    - **Function**: Combines traditional firewall capabilities with advanced features like application awareness, intrusion prevention, user identity management, and deep packet inspection.
    - **Strengths**: Comprehensive security, including protection against sophisticated attacks like malware and intrusions.
    - **Weaknesses**: More complex and can be more expensive than traditional firewalls.
5. **Web Application Firewalls (WAF)**
    
    - **Function**: Focuses specifically on securing web applications by filtering and monitoring HTTP traffic to protect against application-level attacks such as SQL injection, cross-site scripting (XSS), and others.
    - **Strengths**: Effective for web-specific attacks.
    - **Weaknesses**: Doesn't protect network-level traffic as a whole; focused mainly on web applications.

---

### **Firewall Rules**

Firewall rules are configurations that define what traffic is allowed or denied based on criteria such as IP addresses, ports, protocols, and other parameters. Here are some of the key rule types and best practices:

1. **Allow Rules**
    
    - **Description**: These rules permit traffic based on specific conditions (e.g., allow all HTTP traffic from a certain IP range).
    - **Example**: Allow incoming HTTP traffic (port 80) from any IP address to your web server.
2. **Deny Rules**
    
    - **Description**: These rules block traffic based on specific criteria (e.g., block all incoming traffic from a certain IP address).
    - **Example**: Deny all traffic from a known malicious IP address.
3. **Reject Rules**
    
    - **Description**: Similar to deny rules, but they send a response back to the sender, informing them that the traffic was explicitly rejected.
    - **Example**: Reject traffic on port 23 (Telnet) to prevent unauthorized access.
4. **Implicit Deny**
    
    - **Description**: Many firewalls have an implicit "deny all" rule, meaning any traffic not explicitly allowed by a rule is automatically blocked.
    - **Best Practice**: It’s generally recommended to have a "deny all" rule at the end of your firewall rule set to ensure that all unspecified traffic is blocked.
5. **Stateful Rules**
    
    - **Description**: Stateful firewalls maintain a connection state table and ensure that only traffic that is part of a valid session is allowed. For instance, if you initiate a connection to a web server, a stateful firewall will allow the return traffic associated with that session.
    - **Example**: Allow inbound traffic on port 443 (HTTPS) for an established connection.

---

### **Common Ports and Associated Rules**

When configuring a firewall, it's common to create rules based on well-known ports for specific services. Below are examples of ports you might configure rules for:

| **Service** | **Port** | **Direction**    | **Common Rule**                                                              |
| ----------- | -------- | ---------------- | ---------------------------------------------------------------------------- |
| **SSH**     | 22       | Inbound          | Allow SSH traffic only from trusted IP addresses for admin access.           |
| **HTTP**    | 80       | Inbound          | Allow incoming traffic on port 80 for web servers.                           |
| **HTTPS**   | 443      | Inbound          | Allow incoming traffic on port 443 for secure web servers.                   |
| **FTP**     | 21       | Inbound/Outbound | Block inbound FTP traffic, allow outbound if required.                       |
| **SMTP**    | 25       | Outbound         | Allow outbound SMTP for email servers but block inbound to prevent spamming. |
| **DNS**     | 53       | Inbound/Outbound | Allow DNS queries (UDP 53) to external servers.                              |
| **MySQL**   | 3306     | Inbound          | Block all external access to MySQL databases except from specific IPs.       |

---

### **Firewall Security Best Practices**

1. **Principle of Least Privilege**
    
    - Only allow the traffic that is necessary for the operation of your system and deny everything else by default. This minimizes your attack surface.
2. **Log and Monitor Traffic**
    
    - Enable logging to keep track of blocked and allowed traffic. Regularly review these logs for signs of suspicious activity.
3. **Regular Rule Review**
    
    - Firewalls should be regularly audited, and rules should be updated as your network changes. Outdated rules can create unnecessary vulnerabilities.
4. **Use VPNs for Remote Access**
    
    - Instead of opening ports like RDP (port 3389) directly to the internet, use VPNs to create a secure tunnel for remote access.
5. **Limit Inbound Connections**
    
    - Only allow specific IPs or ranges that require access to your system (e.g., for administrative tasks or certain services).
6. **Segmentation and Network Zones**
    
    - Use firewalls to create network zones (e.g., DMZ for web servers, private network for internal systems) to limit exposure and contain breaches.
7. **Test Firewall Configuration**
    
    - Regularly test the firewall’s effectiveness by attempting to access restricted services and ensuring it blocks unauthorized connections.

---

### **Firewall Deployment Architectures**

1. **Perimeter Firewalls**
    
    - Positioned at the boundary between a trusted internal network and untrusted external networks (e.g., internet). These firewalls inspect all incoming and outgoing traffic.
2. **Internal Firewalls**
    
    - Placed inside the network to segment different internal zones (e.g., between departments, databases, and user workstations) to provide additional security layers.
3. **Cloud Firewalls**
    
    - Designed for cloud environments, cloud firewalls provide protection for cloud resources and can scale to handle high traffic volumes.
4. **Web Application Firewalls (WAF)**
    
    - Specifically focused on protecting web applications from common vulnerabilities like SQL injection and cross-site scripting (XSS). Often used alongside other firewalls.

---

### Conclusion

A well-configured firewall is a crucial component of network security. It helps prevent unauthorized access to your network and ensures that only legitimate traffic can pass through. In your Obsidian vault, you can create detailed notes for each type of firewall and its configuration, as well as specific rules and best practices. Let me know if you’d like more details on any specific firewall topic or configuration!