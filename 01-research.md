---
layout: page
title: Research
---

### Theme

Generally speaking, my research spans many areas of computer systems, including distributed systems,
security and privacy, operating systems, and applications of cryptography and machine learning to systems problems.
Much of my ongoing research aims to develop a *new model for privacy* for today's web data-driven world.
Today's web, a complex ecosystem, is largely driven by the collection and monetization of personal data.
Many web services, mobile applications, and third party trackers collect and use our personal data for varied purposes, e.g., to target
ads, personalize recommendations, and fine-tune prices.
At present, we have no window into how our data is being used, and there is little or no accountability required of the services, raising the risk for deceptive and unfair practices.

My team and I seek a new model for how we address such personal privacy issues.
We envision a web environment where users are more aware of the privacy consequences of their online actions and make more informed decisions about the services they use.
In our model, services and applications are held accountable for their actions and are explicitly constructed to protect user privacy.
To forge this new web ecosystem, we design, build, and evaluate:

* **New transparency tools** that increase society's oversight regarding how applications use personal data in order to detect and deter
unfair and deceptive practices;

* **New development tools** that assist programmers in building applications that are privacy-preserving by design; and

* **New abstractions for responsible data management** that promote and facilitate a more rigorous and selective approach to data collection
and retention.


### Ongoing Projects

* **Web transparency tools:**
  Today's Web services are like black boxes.  They use users' personal
  information for all sorts of purposes but the users do not know how their
  data is being used.
  To enhance transparency, we are building a new set
  of scalable infrastructures to detect data uses for targeting and personalization.
  The insight is to compare ads, prices, and other personalized content
  witnessed by different accounts with   similar, but not identical, subsets
  of the data.
  <i>XRay</i>, our first system, detects targeting through correlation
  ([USENIX Security'14 paper]({ site.baseurl }}/publications/usenixsec2014xray.pdf)).
  <i>Sunlight</i>, our second system, more significantly establishes the causes
  of targeting ([CCS'15 paper]({ site.baseurl }}/publications/ccs2015sunlight.pdf)).
  <i>DataObservatory</i>, an in-progress system, detects pieces of arbitrary
  web pages that are personalized or targeted at particular user information.
  These projects are in collaboration with Augustin Chaintreau (Columbia), Daniel Hsu (Columbia),
  and Arvind Narayanan (Princeton).
  Read more on the project's [website](http://columbia.github.io/sunlight/).

* **Testing the fairness of data-driven applications:**
  Today's programmers routinely pass immense and varied kinds of personal
  data through increasingly complex machine learning algorithms, whose
  associations and inferences are difficult to anticipate and analyze.
  This results in a great risk for unintended discriminatory or disparate
  impact effects.
  We are building <i>FairTest</i>, a testing toolkit for programmers to
  discover unintended associations.
  This project is in collaboration with Daniel Hsu (Columbia), Ari Juels (Cornell Tech),
  and Jean-Pierre Hubaux (EPFL).
  Read more in our [tech report](http://arxiv.org/abs/1510.02377).

* **Modern protection abstractions for modern OSes:**
  Data storage abstractions in OSes have evolved enormously. While traditional OSes used to provide fairly low-level abstractions -- files and 
directories -- modern OSes, including Android, iOS, OSX, and recent Windows, embed much higher-level abstractions, such as relational databases or object-relational models. Despite the change in abstraction, many crucial protection systems, such as encryption or deniable systems, still operate at the old file level, which often renders them ineffective. We are investigating new data protection abstractions
that are more suitable for modern operating systems, including a new *logical data object* abstraction, which corresponds directly
to user-level objects, such as emails, documents, or pictures. Thus far, we've investigated two end-of-spectrum approaches for
implementing logical data objects: (1) expose a new APIs to app programmers (*CleanOS* system, described in an [OSDI'12 paper]({{ site.baseurl }}/publications/osdi2012cleanos.pdf)) and (2) recognize objects automatically by leveraging structural information from modern storage abstractions (*Pebbles* system, described in an [OSDI'14 paper]({{ site.baseurl }}/publications/osdi2014pebbles.pdf)).
Our work is driven by our measurement studies of modern application use of traditional OS abstractions -- see our [EuroSys'16 paper]({{ site.baseurl }}/publications/eurosys2016posix.pdf) for some interesting findings.
These projects are in collaboration with Gail Kaiser (Columbia) and Jason Nieh (Columbia).

* **Heterogeneous-database replication:**
  We are building <i>Synapse</i>, a heterogeneous-database replication system,
  which lets programmers of complex, multi-service Web applications to share
  data across services running on very distinct database engines, in real time,
  and with solid consistency semantics.
  We deployed Synapse at a NYC startup.
  Read more in our [EuroSys 2015 paper]({{ site.baseurl }}/publications/eurosys2015synapse.pdf).
  This project is in collaboration with Jason Nieh (Columbia).

* **Virtual machine migration.**
  We are improving virtual machine (VM) migration mechanisms
  by incorporating past state access histories and hints provided
  by the guest operating system.
  For example, we show that state access histories can enable streaming of
  large VMs over wide area and even cellular networks with little loss in the
  VM's interactivity.
  Read more in our [SoCC'15]({{ site.baseurl }}/publications/socc2013vtube.pdf)
  paper.
  This project is in collaboration with Prof. Satya (CMU) and Kaustubh Joshi (ATT Research).


### Notable Past Projects:

* **File auditing for mobile devices:**
  With today's limited anti-theft tools, users can neither assuredly restrict nor
  remotely monitor a thief's data accesses on a stolen or lost mobile device. I
  built <i>Keypad</i>, a new file system that enhances data security on
  mobile devices by providing users with post-theft fine-grained access auditing.
  Read our [EuroSys'11 paper]({{ site.baseurl }}/publications/eurosys2011keypad.pdf")
  (awarded Best Student Paper).

* **Cloud storage customization with active storage.**
  Today's cloud storage services, such as Amazon S3, are highly inflexible and
  impose a variety of constraints on their clients: specific data consistency
  properties, fixed replication factors, limited logging, etc. I built
  <i>Comet</i>, an extensible storage service that allows clients to inject snippets
  of code that control the behavior of their data inside the storage service.
  Read our [OSDI'10 paper]({{ site.baseurl }}/publications/osdi2010comet.pdf").

* **Data lifetime control with self-destructing data.**
  Users' migration to cloud and Web services is causing them to lose
  control over the lifetime of their data. <i>Vanish</i> is a self-destructing data
  system that allows users to impose timeouts on their Web data, such as emails,
  Facebook messages, or Google Docs.
  Read our [USENIX Sec'14 paper]({{ site.baseurl }}/publications/usenixsec2009vanish.pdf")
  (awarded Outstanding Student Paper).

