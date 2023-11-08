# Identification of Web Application Firewall using WAFW00F in Kali Linux

A firewall is a security device that monitors incoming and outgoing traffic just like IPS and IDS. A firewall can be hardware and it can also be software. The firewall is a security mechanism that monitors and filters incoming traffic and also blocks outsiders from gaining unauthorized access to the internal systems of your company or organization. The firewall not only blocks unauthorized incoming traffic but also helps to block malicious software and malicious files that can infect the system. Sometimes it behaves like an antivirus. But it’s not an antivirus. The tool WAF protects against any type of attack such as SQLi & XSS. This is a free and open-source tool that can identify whether the firewall is present on a website or not. Even this tool will give you all the information about which firewall is present on the website. The WAFW00F can filter out requests just like a normal firewall.

![](https://media.geeksforgeeks.org/wp-content/uploads/20210614164219/0.PNG)

### Installation

**Step 1:**  Open your kali Linux operating system and install the tool using the following command.

https://github.com/EnableSecurity/wafw00f.git
cd wafw00f

![](https://media.geeksforgeeks.org/wp-content/uploads/20210614163842/14.PNG)

**Step 2:** The tool has been downloaded. Now give the permission of execution to the tool.

chmod +x setup.py

![](https://media.geeksforgeeks.org/wp-content/uploads/20210614164020/15.PNG)

**Step 3:** Use the following command to run the tool.

./setup.py --help

![](https://media.geeksforgeeks.org/wp-content/uploads/20210614164125/16.PNG)

The tool is running successfully now. We will see examples of using the tool.

### Usage

**Example 1:** Use the wafw00f tool to find whether firewall security is behind a domain or not.

wafw00f www.amazon.com

![](https://media.geeksforgeeks.org/wp-content/uploads/20210614164500/17.PNG)

Sometimes, most security researchers, when they start researching or start finding bugs in websites and web applications. Most of the sites are protected by unknown firewalls.

**Example 2:**  Use the wafw00f tool to find whether firewall security is behind a domain or not.

wafw00f -a www.amazon.com

![](https://media.geeksforgeeks.org/wp-content/uploads/20210614165034/18.PNG)

WAF protects against any type of attack such as SQLi & XSS. This is a free and open-source tool that can identify whether the firewall is present on the website or not. Even this tool will give you all the information about which firewall is present on the website. The WAFW00F can filter out requests just like a normal firewall and tells which firewall is present behind the website. In this example, we have checked the firewall on the domain www.amazon.com. The result we got is that the Cloudfront firewall is present behind this domain.

**Example 3:** Use the wafw00f tool to scan a target with Nmap Scripts.

nmap -p 80,443 --script=http-waf-detect equifaxsecurity2017.com

![](https://media.geeksforgeeks.org/wp-content/uploads/20210618132920/4.PNG)

We can use Nmap with wafw00f tool to find out the open and closed ports on the website. However, we can do the same thing using normal scanning, but in this example, you can see that if we use the wafw00f tool with Nmap it will show us the firewall also, as it’s showing IPS and IDS, which are intrusion detection systems and Intrusion prevention systemn, this way you can use the tool with Nmap.

**Example 4:** Use the wafw00f tool to scan a target with Nmap Scripts.

nmap -p 80,443 --script=http-waf-fingerprint noodle.com

![](https://media.geeksforgeeks.org/wp-content/uploads/20210618133136/5.PNG)

The Nmap scripts will give you information about the ports of websites. In this example, we scanned a normal port scanning using the -p flag of the Nmap tool inside the wafw00f directory. This tool allows IP scanning also, as we have scanned in this example. Similarly, you can perform scanning in our target domain to perform reconnaissance.
