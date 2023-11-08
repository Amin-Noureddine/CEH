# Information Gathering Using TheHarvester In Kali Linux

**Let’s get started,**

If you are using Kali Linux, open the terminal and type  **theharvester**

If not then it can be easily downloaded from here:  [https://github.com/laramies/theHarvester](https://github.com/laramies/theHarvester)

Simply Download and extract it

Provide execute permission to:  **theHarvester.py by [chmod 755 theHavester.py]**

Then simply run **./theharvester**

You will see similar to this:

![Information Gathering using theHarvester in Kali Linux](https://do5p5je931nb0.cloudfront.net/wp-content/uploads/2015/09/theharvester1.jpg)

Here I am using kali linux.

**Method:1**

You can simply use the command  **theHarvester -d [url] -l 300 -b [search engine name]**

For example:  **theHarvester -d sixthstartech.com -l 300 -b google**

Which will result as in the screenshot below:

![Information Gathering using theHarvester in Kali Linux](https://do5p5je931nb0.cloudfront.net/wp-content/uploads/2015/09/theharvester2.jpg)

**Method:2**

To get all the information about the website u can use the command as:

**theHarvester -d sixthstartech.com -l 300 -b all**

Which will result as:

![Information Gathering using theHarvester in Kali Linux](https://do5p5je931nb0.cloudfront.net/wp-content/uploads/2015/09/theharvester3.jpg)

**Method:3**

To save the result in HTML file you can use  **–f** option followed by a file name,

Example:

**theHarvester.py -d sixthstartech.com -l 300 -b all -f test**

![Information Gathering using theHarvester in Kali Linux](https://do5p5je931nb0.cloudfront.net/wp-content/uploads/2015/09/theharvester4.jpg)

The result in HTML File:

![Information Gathering using theHarvester in Kali Linux](https://do5p5je931nb0.cloudfront.net/wp-content/uploads/2015/09/theharvester5.jpg)

That’s it and hoped this helped you!!
