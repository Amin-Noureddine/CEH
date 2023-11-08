# dig Command in Linux with Examples

**dig**  command stands for  _**Domain Information Groper**_. It is used for retrieving information about DNS name servers. It is basically used by network administrators. It is used for verifying and troubleshooting DNS problems and to perform DNS lookups. Dig command replaces older tools such as  [nslooku](https://www.geeksforgeeks.org/nslookup-command-in-linux-with-examples/)p and the  [host](https://www.geeksforgeeks.org/host-command-in-linux-with-examples/).

### Installing Dig command

**In case of Debian/Ubuntu**

$sudo apt-get install dnsutils

**In case of CentOS/RedHat**

$sudo yum install bind-utils

**Syntax:**

dig [server] [name] [type]

### Working with Dig Command

**1.**  To query domain “A” record

dig geeksforgeeks.org

![To-query-domain-A-record](https://media.geeksforgeeks.org/wp-content/uploads/20200517230023/To-query-domain-A-record.png)This command causes dig to look up the “A” record for the domain name “geeksforgeeks.org”.

A record refers to IPV4 IP.  
Similarly, if record type is set as “AAAA”, this would return IPV6 IP.

**2.**  To query domain “A” record with  **+short**

dig geeksforgeeks.org +short

![To-query-domain-A-record-with-short](https://media.geeksforgeeks.org/wp-content/uploads/20200517230153/To-query-domain-A-record-with-short.png)By default dig is verbose and by using “+short” option we can reduce the output drastically as shown.  **3.**  To remove comment lines.

dig geeksforgeeks.org +nocomments

![To-remove-comment-lines](https://media.geeksforgeeks.org/wp-content/uploads/20200517230259/To-remove-comment-lines-.png)This command makes a request and excludes the comment lines.  **4.**  To set or clear all display flags.

dig geeksforgeeks.org +noall

![To-set-or-clear-all-display-flags](https://media.geeksforgeeks.org/wp-content/uploads/20200517230751/To-set-or-clear-all-display-flags.png)We use the “noall” query option, when we want to set or clear all display flags.  **5.**  To query detailed answers.

dig geeksforgeeks.org +noall +answer

![to-query-detailed-answers](https://media.geeksforgeeks.org/wp-content/uploads/20200517230948/to-query-detailed-answers.png)If we want to view the answers section information in detail, we first stop the display of all section using “+noall” option and then query the answers section only by using “+answer” option with the dig command.  **6.**  To query all DNS record types.

dig geeksforgeeks.org ANY

![to-query-all-dns-record-types](https://media.geeksforgeeks.org/wp-content/uploads/20200517231129/to-query-all-dns-record-types.png)We use “ANY” option to query all the available DNS record types associated with a domain. It will include all the available record types in the output.  **7.**  To query MX record for the domain.

dig geeksforgeeks.org MX

![to-query-ms-record-of-the-domain](https://media.geeksforgeeks.org/wp-content/uploads/20200517231236/to-query-ms-record-of-the-domain.png)If we want only the mail exchange – MX – answer section associated with a domain we use this command.  **8.**  To trace DNS path

dig geeksforgeeks.org +trace

![to-trace-dns-path](https://media.geeksforgeeks.org/wp-content/uploads/20200517231349/to-trace-dns-path.png)“+trace” command is used for tracing the DNS lookup path. This option makes iterative queries to resolve the name lookup. It will query the name servers starting from the root and subsequently traverses down the namespace tree using iterative queries following referrals along the way.  **9.**  For specifying name servers

dig geeksforgeeks.org @8.8.8.8

![for-specifying-name-servers](https://media.geeksforgeeks.org/wp-content/uploads/20200517231600/for-specifying-name-servers.png)By default, dig command will query the name servers listed in “/etc/resolv.conf” to perform a DNS lookup. We can change it by using @ symbol followed by a hostname or IP address of the name server.  **10.**  To query the statistics section

dig geeksforgeeks.org +noall +answer +stats

![TO-QUERY-STATISTICS-SECTION](https://media.geeksforgeeks.org/wp-content/uploads/20200517231709/TO-QUERY-STATISTICS-SECTION.png)We use “+stats” option with dig command, to see the statistics section.

**Reverse DNS Lookup:**

Reverse DNS lookup can be used to fetch domain name or the host name from the IP address.  
“-x” option is used to perform reverse DNS lookup.

ex:

[xxxxxx ~]# dig +noall +answer -x 8.8.8.8  
8.8.8.8.in-addr.arpa. 18208 IN PTR dns.google.

Note: DNS reverse look up will work only if the entry is present PTR.  
PTR contents can be viewed using the command “dig -x xx.yy.zz.aa”  

**Batch Queries:**

Instead performing dig query for each domain at a time, a list of domains can be queried at once.

To do so, enter the domain names in a file, only 1 domain name in each line and perform the dig query on file.  
ex: let’s say, file.txt has the list of domain names to be queried then,

dig -f file.txt +shortwill perform DNS queries and return all the resolved IPs.
