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
(1) *new transparency tools* that increase society's oversight regarding how applications use personal data in order to detect and deter
unfair and deceptive practices;
(2) *new development tools* that assist programmers in building applications that are privacy-preserving by design; and
(3) *new abstractions for responsible data management* that promote and facilitate a more rigorous and selective approach to data collection
and retention.


### Ongoing Projects

* **Web transparency tools:**
  Today's Web services are like black boxes. They use users' personal
information for all sorts of purposes but the users do not know how their data is being used.
To enhance transparency, we are building a new set of scalable infrastructures
([XRay]({{ site.baseurl }}/publications/usenixsec2014xray.pdf) and
[Sunlight]({{ site.baseurl }}/publications/ccs2015sunlight.pdf)) to detect data uses for
targeting and personalization. The insight is to compare ads, prices, and other personalized
content witnessed by different accounts with similar, but not identical, subsets of the data.
[http://columbia.github.io/sunlight/](http://columbia.github.io/sunlight/).

* **Testing the fairness of data-driven applications:**
  Today's programmers routinely pass immense and varied kinds of personal
  data through increasingly complex machine learning algorithms, whose
  associations and inferences are difficult to anticipate and analyze.
  This results in a great risk for unintended discriminatory or disparate
  impact effects.
  We are building [FairTest]({{ site.baseurl }}/publications/eurosp2017fairtest.pdf), a
  testing toolkit for programmers to discover unintended associations.
  [http://columbia.github.io/fairtest/](http://columbia.github.io/fairtest/)

* **Selective data systems:**
  We are challenging a common practice in both private and public sectors of collecting vast
quantities of personal information. We ask whether it is possible to build data-driven systems,
such as machine learning-based personalization systems, that are more selective with the data
they collect. This entails pinpointing the data that is valuable for the current and evolving
workload, and either not collecting or setting aside the data that is not truly valuable.
We are constructing tools to create this separation and data management and protection systems
that leverage them to enhance data security and reduce data management costs through selectivity.
Read about our first tool, called Pyramid, in our recent [IEEE S&P paper]({{ site.baseurl }}/publications/oakland2017pyramid.pdf).
And about the overall project on our website: [http://columbia.github.io/selective-data-systems/](http://columbia.github.io/selective-data-systems/).


### Notable Past Projects:

* **Modern protection abstractions for modern OSes:**
Data storage abstractions in OSes have
evolved enormously. Yet, data protection abstractions are still applied at the old abstraction
level, often rendering them ineffective. We are investigating new data protection abstractions
that are more suitable for modern operating systems.
Read about the abstractions we developed thus far in our [OSDI 2012]({{ site.baseurl }}/publications/osdi2012cleanos.pdf),
[OSDI 2014]({{ site.baseurl }}/publications/osdi2014pebbles.pdf), and [EuroSys 2016]({{ site.baseurl }}/publications/eurosys2016posix.pdf)
papers.

* **Heterogeneous-database replication:**
  We build <i>Synapse</i>, a heterogeneous-database replication system,
  which lets programmers of complex, multi-service Web applications to share
  data across services running on very distinct database engines, in real time,
  and with solid consistency semantics.
  We deployed Synapse at a NYC startup.
  Read more in our [EuroSys 2015 paper]({{ site.baseurl }}/publications/eurosys2015synapse.pdf).

* **Virtual machine migration.**
  We improve virtual machine (VM) migration mechanisms
  by incorporating past state access histories and hints provided
  by the guest operating system.
  For example, we show that state access histories can enable streaming of
  large VMs over wide area and even cellular networks with little loss in the
  VM's interactivity.
  Read more in our [SoCC'13]({{ site.baseurl }}/publications/socc2013vtube.pdf) and
  [VEE'16]({{ site.baseurl }}/publications/enlightened-migration.pdf) papers.

* **File auditing for mobile devices:**
  With today's limited anti-theft tools, users can neither assuredly restrict nor
  remotely monitor a thief's data accesses on a stolen or lost mobile device. I
  built <i>Keypad</i>, a new file system that enhances data security on
  mobile devices by providing users with post-theft fine-grained access auditing.
  Read our [EuroSys'11 paper]({{ site.baseurl }}/publications/eurosys2011keypad.pdf")
  (awarded Best Student Paper).

* **Data lifetime control with self-destructing data.**
  Users' migration to cloud and Web services is causing them to lose
  control over the lifetime of their data. <i>Vanish</i> is a self-destructing data
  system that allows users to impose timeouts on their Web data, such as emails,
  Facebook messages, or Google Docs.
  Read our [USENIX Sec'14 paper]({{ site.baseurl }}/publications/usenixsec2009vanish.pdf")
  (awarded Outstanding Student Paper).

