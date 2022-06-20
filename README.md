# Top 10 Hacker Tools and Techniques

By understanding how hackers gain access to systems, organizations can stay a step ahead and ensure information availability, integrity, and confidentiality. Listed below is Altius IT's list of the Top 10 Hacker Tools and Techniques:

1) Reconnaissance

Reconnaissance, also known as the preparatory phase, is where the hacker gathers information about a target before launching an attack and is completed in phases prior to exploiting system vulnerabilities. One of the first phases of Reconnaissance is dumpster diving. It is during this phase that the hacker finds valuable information such as old passwords, names of important employees (such as the head of the network department), and performs an active reconnaissance to know how the organization functions. As a next step, the hacker completes a process called footprinting to collect data on the security posture, reduces the focus area such as finding out specific IP addresses, identifies vulnerabilities within the target system, and finally draws a network map to know exactly how the network infrastructure works to break into it easily. Footprinting provides important information such as the domain name, TCP and UDP services, system names, and passwords. There are also other ways to do footprinting, including impersonating a website by mirroring it, using search engines to find information about the organization, and even using the information of current employees for impersonation. 


# Top 10 Tools for Reconnaissance

1) Google

For every penetration tester, Google should be the first tool to use for continuous cyber recon. Google and other search engines like Bing are vital during reconnaissance because it provides vital data about individuals, companies, and data including leaked content. The obtained information is free and can help to determine the direction a penetration tester will take. 

2) Maltego CE

Maltego is a visual link analysis and data mining tool and it is the most famous software for performing Open Source Intelligence. It provides a library of plugins, called “transforms”, which are used to execute queries on open sources in order to gather information about a certain target and display them on a nice graph. In fact, differently from the command line tools seen until now, Maltego has a Graphical User Interface through which the user performs his research and analyzes results returned on the graph.

It is developed by Paterva which distributes three different versions: Maltego XL, Classic and CE. We are interested in Maltego CE which stands for Community Edition: this is the non commercial version and it is available for everyone after a quick registration.

Installation

Before proceeding with the installation it is a good idea to register at this link: https://www.paterva.com/web7/community/community.php. In fact, in order to use the software it is mandatory to have a Maltego account which is required at the startup of the application.

If you are using Kali Linux, Maltego CE is already installed. Moreover you will find that Kali has its own custom version called Maltego Chlorine, which has been made on purpose for this distro.
Otherwise you can download the package from https://www.paterva.com/web7/downloads.php#tab-3 and install it on your operating system (the software is available for Windows, Linux or Mac OSX).

# Installation

In Kali Linux, Maltego can be started by navigating in the applications menu by clicking on Applications > Information Gathering > maltegoce like shown in the following image:

![maltego_start](https://user-images.githubusercontent.com/106522935/174518274-3dccd0c4-df61-4379-8b67-e261512472a8.png)

Same thing can be done by clicking on the “Show application” menu:

![maltego_start2](https://user-images.githubusercontent.com/106522935/174518568-b5ffe9e3-bafa-43a7-a23e-eab9a882cc9e.png)

Maltego can also be started by opening the Terminal and typing maltegoce, but since it is not a command line tool, this is not the best choice.

At the start up, after all the modules are correctly loaded, we get prompted with the Startup Wizard which asks for Maltego account credentials:

![maltego_account](https://user-images.githubusercontent.com/106522935/174518641-b091eb7d-a44f-46bd-a8b7-9625b0f13104.png)


If you have inserted them and correctly solved the captcha, you will get a welcome message and the information about the validity of the API key. At the next prompt just leave “Install Transforms from Maltego public servers” which will install the transforms on the client.
At the final screen we get the correct initialization message with different possibilities for starting to use Maltego:

![maltego_ready](https://user-images.githubusercontent.com/106522935/174518705-a1051939-9f41-48cf-ab17-cd492173d4b8.png)

“Run a machine” allows you to run predefined searches, called “machines”: for example, the “Company Stalker” machine gets all email addresses it can find on the web for a certain domain and look for related account on social networks; it also gets documents and extract metadata from them.
Since we want to perform a custom search we need to select “Open a blank graph and let me play around” and then click on “Finish”. This action opens a new empty graph where we can start a new OSINT activity:

![maltego_new](https://user-images.githubusercontent.com/106522935/174518833-8cae6eb6-ca05-4914-b7b3-e010caff4154.png)

We could have also opened a new graph by simply clicking on Maltego icon on the top left choosing “New”.
As the image shows, on the top part we have six tabs:

•Investigate - offers options to quickly search through the graph or to select entities;
•Manage - allows to import/export configurations, manage entities and transforms;
•View - allows to choose which panels are active;
•Organize - sets the node layout mode and the alignment type;
•Machines - allows to run, stop, create and manage machines;
•Collaboration - offers options to share projects and results.

There is a big central window which is where the graph will be developed and on the tab it is reported the name of the graph (you can save the project and give it a proper name).
On the left side we have the “Palette” panel which contains the following categories:

•Devices - adds a node such as a phone or camera;
•Infrastructure - adds a node such as a domain, MX record or Website;
•Locations - adds a node such as a GPS coordinate or location name;
•Malware - adds a node as hash entity;
•Penetration Testing - adds a node which identifies a technology;
•Personal - adds a node such as a document, email address or person name;
•Social Network - adds a node related to social networks like Facebook or Twitter.
Each of them contains objects related to that category: these items can be dragged on the graph and, once placed there, it is possible to use them as starting point for a search activity. This can be done thanks to the application of transforms.

As done in the previous Information Gathering posts, we can use as target the National Institute of Standards and Technology (NIST). We can start by clicking on “Infrastructure” and dragging on the graph a “Domain” object; by double clicking on it we can change its name into “nist.gov”:

![maltego_nist (1)](https://user-images.githubusercontent.com/106522935/174519199-a30a3f62-43d8-4921-8d51-d739405308d4.png)

Now informations are displayed also in the other four panels:

•Run View - contains Transforms and Machines that it is possible to run against the selected object;
•Overview - shows a schematic graph where nodes are represented by colored circles;
•Detail View - displays informations about the selected object;
•Property View - shows properties regarding the selected object.

To run a transform on the object we can either access them through the “Run View” panel or by simply clicking on the object with the right mouse button. “All Transforms” contains all the possible transforms we can apply to that object type, which in this case is a Domain object.
The same transforms can also be found by looking inside the following four groups (of course they vary depending on the object type):

•DNS from Domain;
•Domain owner detail;
•Email addresses from Domain;
•Files and Documents from Domain.

![maltego_transforms](https://user-images.githubusercontent.com/106522935/174519337-00a7637e-243e-4132-9403-9973982b0bd0.png)
