# How to use the whois command on Ubuntu Linux
### Installing Whois Command on Ubuntu

Follow the below number of steps to install the Whois command on Ubuntu.

**Step 1:** Firstly, update the system using the below command. Execute the below command in the terminal to update the system.

sudo [apt](https://www.geeksforgeeks.org/apt-command-in-linux-with-examples/) update

![Updating System](https://media.geeksforgeeks.org/wp-content/uploads/20230403200525/Step-1-min-min.png)

**Step 2:** Now, by using the apt manager, install the whois command utility, so that we can retrieve the information about domains, IP Addresses, etc.

sudo apt install whois

![Installing Whois command utility](https://media.geeksforgeeks.org/wp-content/uploads/20230403200526/Step-2.png)

### Usage of Whois Command on Ubuntu

#### **Example 1: Getting Information on Domain Name (geeksforgeeks.org).**

In this example, we will extract the information about the domain (geeksforgeeks.org). In the below screenshot, you can see that we have information like Registry Domain ID, WHOIS Server, Updated Date, etc.

whois geeksforgeeks.org

![Getting info about domain name](https://media.geeksforgeeks.org/wp-content/uploads/20230403200529/Usage-1-1-min.png)

Some information is kept private due to security issues. As you can see in the below screenshot, information like Phone, Fax, Postal Code, etc information is kept private.

![Private Data](https://media.geeksforgeeks.org/wp-content/uploads/20230403200530/Usage-1-2-min.png)

#### **Example 2: Getting Information about IP Address.**

In this example, we will be extracting information by giving the IP Address as input to the whois command. In the below screenshot, we have got the information about the IP Address such as NetRange,  [CIDR](https://www.geeksforgeeks.org/cidr-full-form/), etc.

whois 8.8.8.8

![Getting info about IP address](https://media.geeksforgeeks.org/wp-content/uploads/20230403200532/Usage-2.png)

In the below screenshot, detailed information is shown such as OrgTechName, OrgTechPhone, OrgTechEmail, etc. This information can be helpful to diagnose the network connections and also to troubleshoot the network.

![Data retrived about IP Address](https://media.geeksforgeeks.org/wp-content/uploads/20230403200533/Usage-2-2.png)

#### Example 3: Getting Information about some specific WHOIS server set up by an ICANN.

WHOIS command is not limited to standard domain or IP address, even we can extract the information of some specific WHOIS server set up by an ICANN. In the below screenshot, we have given the input of the WHOIS Server along with the domain name. We have got the detailed information for this.

whois -h whois.verisign-grs.com google.com

![Getting Information about some specific WHOIS server set up by an ICANN](https://media.geeksforgeeks.org/wp-content/uploads/20230403200534/Usage-3-min.png)

#### Example 4: Getting Information about a domain name from a specific registrar.

In this example, we will fetch the information about a domain name from a specific registrar. We have given the domain name (**whois.iana.org**) and the registrar (**com**).

whois -h whois.iana.org com

![Getting  Information about a domain name from a specific registrar](https://media.geeksforgeeks.org/wp-content/uploads/20230403200536/Usage-4.png)

### Uninstalling Whois Command on Ubuntu

After usage, we can remove the command by uninstalling it. Execute the below command in the terminal to remove the whois command from Ubuntu.

sudo [apt remove](https://www.geeksforgeeks.org/how-to-uninstall-packages-with-apt-package-manager-in-linux/) whois

![Removing Whois command using apt manager](https://media.geeksforgeeks.org/wp-content/uploads/20230403200528/Uninstall.png)

### Conclusion

In conclusion, the whois command is a useful tool for obtaining information about domain names, IP Addresses, and network devices registered with ICANN. Whois command is a simple and powerful tool that can be useful for network administration, web development, and security tasks, and every Linux user should be familiar with its usage. In this article, we have gone through the installation of the whois command and its usage in the form of examples.
