# Nslookup Command in Linux with Examples
**Nslookup** (stands for “Name Server Lookup”) is a useful command for getting information from the DNS server. It is a network administration tool for querying the Domain Name System (DNS) to obtain domain name or IP address mapping or any other specific DNS record. It is also used to troubleshoot DNS-related problems.

## **Syntax of the `nslookup` command in Linux System**
nslookup [option] [hosts]

**Options of nslookup command:**


**-domain=[domain-name]**

allows you to change the default DNS name.

**-debug**

enables the display of debugging information.

**-port=[port-number]**

Use the -port option to specify the port number for queries. By default, nslookup uses port 53 for DNS queries

**-timeout=[seconds]**

you can specify the time allowed for the DNS server to respond. By default, the timeout is set to a few seconds

**-type=a**

Lookup for a record  
We can also view all the available DNS records for a particular record using  the  _-type=a_ option

**-type=any**

Lookup for any record  
We can also view all the available DNS records using the  _-type=any_  option.

**-type=hinfo**

displays hardware-related information about the host. It provides details about the operating system and hardware platform

**-type=mx**

Lookup for an mx record  
MX (Mail Exchange) maps a domain name to a list of mail exchange servers for that domain. The MX record says that all the mails sent to “google.com” should be routed to the Mail server in that domain.

**-type=ns**

Lookup for an ns record  
NS (Name Server) record maps a domain name to a list of DNS servers authoritative for that domain. It will output the name serves which are associated with the given domain.

**-type=ptr**

used in reverse DNS lookups. It retrieves the Pointer (PTR) records, which map IP addresses to domain names.

**-type=soa**

Lookup for a soa record  
SOA record (start of authority), provides the authoritative information about the domain, the e-mail address of the domain admin, the domain serial number, etc…

## Examples of Some Most Command Options of `nslookup` in Linux.

### Performing a basic DNS lookup

**Syntax:**

nslookup example.com

**Example:**

nslookup google.com

nslookup followed by the domain name will display the “A Record” (IP Address) of the domain. Use this command to find the address record for a domain. It queries domain name servers and gets the details.

![nslookup google.com](https://media.geeksforgeeks.org/wp-content/uploads/1final-1.png)

nslookup google.com

### Performing a reverse DNS lookup

**Syntax:**

nslookup [IP Address]

**Example:**

nslookup 192.168.0.10

You can also do the reverse DNS look-up by providing the IP Address as an argument to nslookup.

![nslookup 192.168.0.10](https://media.geeksforgeeks.org/wp-content/uploads/2-282.png)

nslookup 192.168.0.10

### Using `-type=any` option

**Syntax:**

nslookup -type=any google.com

Lookup for any record We can also view all the available DNS records using the  _-type=any_  option.

![nslookup -type=any google.com](https://media.geeksforgeeks.org/wp-content/uploads/3-202.png)

nslookup -type=any google.com

### Using  **`-type=soa`**  option

**Syntax:**

nslookup -type=soa redhat.com

Lookup for a soa record SOA record (start of authority), provides the authoritative information about the domain, the e-mail address of the domain admin, the domain serial number, etc…

![nslookup -type=soa redhat.com](https://media.geeksforgeeks.org/wp-content/uploads/4-130.png)

nslookup -type=soa redhat.com

### Using  **`-type=ns`**  option

**Syntax:**

nslookup -type=ns google.com

Lookup for an ns record. NS (Name Server) record maps a domain name to a list of DNS servers authoritative for that domain. It will output the name serves which are associated with the given domain.

![nslookup -type=ns google.com](https://media.geeksforgeeks.org/wp-content/uploads/5-99.png)

nslookup -type=ns google.com

### Using  **`-type=a`**  option

**Syntax:**

nslookup -type=a google.com

Lookup for a record. We can also view all the available DNS records for a particular record using  the  _-type=a_ option.

![](https://media.geeksforgeeks.org/wp-content/uploads/6-74.png)

nslookup -type=a google.com

### Using  **`-type=mx`**  option

**Syntax:**

nslookup -type=mx google.com

Lookup for an mx record. MX (Mail Exchange) maps a domain name to a list of mail exchange servers for that domain. The MX record says that all the mails sent to “google.com” should be routed to the Mail server in that domain.

![nslookup -type=mx google.com](https://media.geeksforgeeks.org/wp-content/uploads/7-57.png)

nslookup -type=mx google.com

### Using  **`-type=txt`**  option

**Syntax:**

nslookup -type=txt google.com

Lookup for a txt record. TXT records are useful for multiple types of records like DKIM, SPF, etc. You can find all TXT records configured for any domain using the command below.

![nslookup -type=txt google.com](https://media.geeksforgeeks.org/wp-content/uploads/9-31.png)

nslookup -type=txt google.com

## Conclusion

In this article we have discussed the `nslookup` command which is a variable tool for querying the DNS server and obtaining information about domain name or IP address mapping. We have studied that it is very useful for troubleshooting DNS-related issues. We have also discussed options like -type=a, -type=any, -type=mx, -type=ns, -type=ptr, and -type=soa. Overall, we can say that by using nslookup information, administrators can gain insights into the DNS infrastructure and resolve DNS-related problems efficiently.


