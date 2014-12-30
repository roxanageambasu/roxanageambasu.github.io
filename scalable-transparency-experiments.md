---
layout: page-notrack
---

## Scalable Web Transparency Experiments

Our Scalable Web Transparency project ([http://xray.cs.columbia.edu/](http://xray.cs.columbia.edu/)) aims to build
the very first generic tools that can answer questions about targeting on the Web
at scale.  Examples of questions we seek to answer include: 

- What do advertisers target?
- How do third-party Web trackers use the data they collect to target the
users?
- How spread is personalization and discrimination based on social
data on the Web?
- Do services share data with one another?

To answer these and other questions, we have built a system, called XRay, that reveals
data targeting by measuring correlation between specific data inputs (be they emails,
searches, or visited products) with data outputs (such as ads or recommended products).
Its correlation mechanism is service agnostic and easy to instantiate on various services.
For example, it lets a data owners track how their emails are used to target ads in Gmail;
and how previously viewed videos or products videos are used to target new recommendations
in YouTube and Amazon, respectively. Briefly, XRay correlates inputs with outputs by
populating a number of extra user profiles with subsets of the inputs and comparing the
outputs in these different accounts to grasp correlation. Of course, the details are more
complex and they require careful intertwining of theory and systems, details of which can
be found in our [USENIX Security 2014 paper](http://matlecu.github.io/xray/public/usenix14lecuyer.pdf).
Our main evaluation result is that XRay can achieve high precision and recall
of its data use predictions, as well as asymptotic causation assurances, with only a modest
number of shadow profiles (logarithmic in the number of inputs under certain assumptions).
This suggests great scaling prospects.

Going forward, we plan to leverage XRay and related concepts to run a series of measurement
studies that answer interesting questions about personal data targeting on the Web at
large scale.  The remainder of this page details the experiments we plan to run, as well as our
AWS-based methodology.

### Question 1: What Do Advertisers Target?

We plan to create a snapshot of Google's targeted ads on a large number of keywords: tens of thousands.
Many of these keywords will be benign and will provide information on the volume of targeting on various topics
and the types of campaigns advertisers run. Other more sensitive keywords will try to elicit information on the
darker corner of online ads. As a teaser, our small-scale studies have already discovered ads for easy car loans
that targeted users based on their emails expressing financial difficulty, as shown on our
[website](http://matlecu.github.io/xray/3-use-cases/#table). We also found numerous ads strongly correlated to
keywords like cancer, depression, Alzheimer's, or pregnancy. Intuitively, such targeting could be dangerous for
end-users, especially if it is extremely non-obvious from the ad's text, as were many of the associations we
found with XRay. An unsuspecting user might click on an ad, thereby revealing sensitive information to an
advertiser who could use it to the user's detriment. In our new measurement study, we plan to measure and
categorize such targeting at large scale.

### Question 2: How Do Third-party Trackers Target the Users?

We plan to study for the first time ad targeting based on third-party trackers. We will simulate a
population of users browsing various websites (and within each website, individual articles), and will study
the targeting of the ads that they get on arbitrary websites (through XRay-like correlation). We will use
Mozilla's Lightbeam tool to detect trackers on arbitrary websites, AdBlock to detect ads on arbitrary websites,
and XRay to relate the trackers (as inputs) to the ads (as outputs).  Specific questions of our measurement
study include: Are there major third parties that are the origin of more targeting than others in this workload?
How long does it take until a particular tracker starts targeting on a particular piece of data? How frequent is
re-targeting applied?

### Question 3: How Spread Is Personalization on the Web?

Advertising is just one type of service where we already know targeting happens. In recent years,
however, there has been some speculation recently on whether other services leverage user's data
to target, personalize, or discriminate various other products.  For example,
[some have argued](http://money.cnn.com/2013/08/26/technology/social/facebook-credit-score/) that
lenders are using Facebook information to decide on loans. Our measurement
seeks to check this hypothesis at scale. We will develop a tool that crawls the Web from the vantage
point of multiple different user profiles and relates consistent differences in the outputs with any
differences in the profiles that appear to strongly correlate with them.  We will develop heuristics
to narrow the comparison to "interesting" elements within a page (e.g., portions including the "$"
sign, which will likely be prices). We will release all data and code publicly.  We and other
researchers will be able to visualize the consistent differences and attribute them to specific profile
aspects. They will judge on a case-by-case basis whether they represent discrimination or just
innocuous personalization.

### AWS-Based Methodology

We plan to run these and other experiments, as well as the development and testing that prepares them, on 10
AWS large instances over the next two years.  These instances will crawl the Web from the vantage points of
various profiles and will store cookies, tracking information, ads, and/or page contents in EBS and/or S3.
We will then process on this data, performing the necessary correlations.  We may use the Elastic Map/Reduce
service for this. We will store the result data sets in S3 and will make all data available publicly.  We will
also host a service for a year that lets researchers or others interested in the data access it without
downloading the full amount.  We are already running a demo service on AWS at [http://data.lec.io/](http://data.lec.io/).

All experiments will be designed carefully to adhere to AWS's policies as well as good crawling practices.
We will severely rate limit our crawlers on any given domain to prevent disruption of the crawled services. We
will adhere to robots.txt.  We will always declare our identity in full, both in any profile names and in our
user-agent.  We will not click on any ads, perform any spamming activity, or interact with real users' data.
If any details are required about our experiments, or if any concerns arise, we would be happy to discuss and
adapt our methods.  Running these experiments right is tremendously important for us.

