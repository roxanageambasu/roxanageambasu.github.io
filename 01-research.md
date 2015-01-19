---
layout: page
title: Research
---

<h3>Research</h3>

Broadly speaking, I am interested in computer systems research, including
distributed systems, security and privacy, operating systems, and
databases. More specifically, my current research focuses on the challenges
and opportunities created by today's emerging technologies, such as cloud
computing and powerful mobile devices.  Brief descriptions of my research projects follow.

<h3>Current Projects</h3>

* **XRay: Increasing the Web's Transparency.**
  Today's Web services accumulate enormous sensitive information -- such as emails, search logs, or locations -- and use them to target advertisements, prices, or products at users. Presently, users have little insight into how their data is used for such purposes. To enhance transparency, we are building **XRay**, a system that predicts what data -- such as emails or searches -- is used to target which ads in Gmail, which prices in Amazon, etc. The mechanism is Web-service independent, though the plugin is not. The insight is to compare ads/prices witnessed by different accounts with similar, but not identical, subsets of the data.  A [paper]({{ site.baseurl }}/publications/usenixsec14xray.pdf) describing XRay appeared at USENIX Security 2014.  The project's website is [here](http://xray.cs.columbia.edu). This work is in collaboration with Prof. [Augustin Chaintreau](http://www.cs.columbia.edu/~augustin/) from Columbia.

* **Modern protection abstractions for modern OSes.**
Data storage abstractions in OSes have evolved enormously. While traditional OSes used to provide fairly low-level abstractions -- files and directories -- modern OSes, including Android, iOS, OSX, and recent Windows, embed much higher-level abstractions, such as relational databases or object-relational models. Despite the change in abstraction, many crucial protection systems, such as encryption or deniable systems, still operate at the old file level, which often renders them ineffective. We are investigating new data protection abstractions
that are more suitable for modern operating systems, including a new *logical data object* abstraction, which corresponds directly
to user-level objects, such as emails, documents, or pictures. Thus far, we've investigated two end-of-spectrum approaches for
implementing logical data objects: (1) expose a new APIs to app programmers (*CleanOS* system, described in an [OSDI 2012 paper]({{ site.baseurl }}/publications/osdi2012cleanos.pdf)) and (2) recognize objects automatically by leveraging structural information from modern storage abstractions (*Pebbles* system, described in an [OSDI 2014 paper]({{ site.baseurl }}/publications/osdi2014pebbles.pdf)">OSDI 2014 paper</a>, done in collaboration with Prof. [Gail Kaiser](http://www.cs.columbia.edu/~kaiser/) from Columbia.

* **Synapse: Data Exchange Done Right.**
Data has become the principal asset of the Internet era, which everyone strives
to acquire and process. A new economy is emerging, in which striking amounts of continuously
changing user data is being sold and shared for others to process upon. That economy
needs to be controlled so that information can be shared efficiently, with strong semantic
guarantees, and securely across multiple applications. To this end, we are building <i>Synapse</i>,
an easy-to-use, strong-semantics, secure Web programming framework for large-scale,
data-driven Web service integrations. This project is in collaboration with Prof.
[Jason Nieh](http://www.cs.columbia.edu/~nieh/) from Columbia.

* **vTube: An Interactive Repository of Executable Content for Long-term Content Preservation.**
Humangous amounts of data, software, and research artifacts are being produced today, including photos, documents, games, applications, and
scientific models.  While many techniques exist to ensure the availability of these digital contents in the short to medium term, little is known about long-term preservation. What will happen with these contents 50 years from now, when most of the libraries, codecs, OSes, and hardware platforms that they were created for will have evolved in non-backward-compatible ways? In collaboration with Prof. <a href="http://www.cs.cmu.edu/~satya">Mahadev Satyanarayanan</a> from CMU and Dr. <a href="http://www.research.att.com/people/Joshi_Kaustubh/">Kaustubh Joshi</a> from ATT, we are building infrastructure necessary for long-term preservation and convenient access of such digital artifacts despite
infrastructural change. Read about our first step toward this goal in our <a href="{{ site.baseurl }}/publications/socc2013vtube.pdf">SoCC 2013 paper</a>, which describes <i>vTube</i>, a YouTube-like system that stores, archives, and streams <i>executable content</i>, i.e., data or software plus all of their dependencies.


<div id="notable-projects">
<h3>Notable Recent Projects</h3></div>

<ul class = "NoIndentNoBullet">

<li><b>Keypad: Auditing File System for Mobile Devices.</b>
With today's limited anti-theft tools, users can neither assuredly restrict
nor remotely monitor a thief's data accesses on a stolen or lost mobile device.
I am currently building Keypad, a new file system that enhances data security
on mobile devices by providing users with post-theft remote control and
fine-grained access auditing. Details about Keypad are available in our
<a href="{{ site.baseurl }}/publications/eurosys2011keypad.pdf">EuroSys 2011 paper</a>,
which won a <font color="red">"Best Student Paper" award</font>.

<li><b>Vanish: Self-destructing Data.</b>
Users' migration to cloud and Web services is causing them to lose
control over the lifetime of their data. Vanish is a self-destructing data
system that allows users to impose timeouts on their Web data, such as emails,
Facebook messages, or Google Docs. The project's
<a href="http://vanish.cs.washington.edu/">web page</a> includes a detailed
description of our Vanish work and links to our prototype. Our initial Vanish
design was described in our 
<a href="{{ site.baseurl }}/publications/usenixsec09-geambasu.pdf">USENIX Security 2009
	paper</a>, which received an <font color="red">"Outstanding Student Paper" award</font>.
</li>

<li><b>Comet: Active Distributed Storage Systems.</b>
Today's cloud storage services, such as Amazon S3 or peer-to-peer DHTs, 
are highly inflexible and impose a variety of constraints on their clients: 
specific replication and consistency schemes, fixed data timeouts,
limited logging, etc.  We witnessed such inflexibility first-hand as part of our
Vanish work, where we used a DHT to store encryption keys
temporarily. To address this issue, we built Comet, an extensible storage
service that allows clients to inject snippets of code that control their
data's behavior inside the storage service. Details about Comet can be found
in our <a href="{{ site.baseurl }}/publications/osdi2010comet.pdf">OSDI 2010 paper</a>.
</li>

</ul>
</div>
</ul>
</div>

