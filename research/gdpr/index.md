---
layout: default
title: Analyzing GDPR from a Systems Perspective
---

<br>
<img style="float:left; margin-right:25px" src="/img/gdpr.png" width="27%" height="27%"> On May 25th 2018, after nearly two years of deliberation and public debate, the European parliament adopted the [General Data Protection Regulation](https://en.wikipedia.org/wiki/General_Data_Protection_Regulation). This was triggered by an alarming trend in data breaches and privacy violations globally. GDPR declares the protection and privacy of personal data as a fundamental right of all the European people, and thus requires any company dealing with EU customers to comply with it. While essential, achieving compliance is not trivial: [Gartner](https://www.gartner.com/en/newsroom/press-releases/2017-05-03-gartner-says-organizations-are-unprepared-for-the-2018-european-data-protection-regulation) estimates a compliance rate of <50% by the end of 2018.<br><br>

**Why is compliance challenging?** GDPR’s goal of *data protection by design and by default* sits at odd with the traditional system design goals of optimizing for performance, cost, and reliability. As our [first investigation](#1-how-design-architecture-and-operation-of-modern-systems-conflict-with-gdpr) reveals, several design principles and operational practices widely followed in the real-world, conflict with the proposed regulations. These deep-rooted tussles are hard to fix via cosmetic changes. Second, unlike other privacy regulations like HIPAA and FERPA, GDPR is comprehensive: it defines personal data as any information relating to an identifiable natural person as well as gives people broad set of rights over their personal data. As we demonstrate in our [second project](#2-analyzing-the-impact-of-gdpr-on-storage-systems), current generation storage systems incur significant overhead to support these GDPR queries. Finally, though GDPR is clear in its high-level goals, it is intentionally vague in its technical specifications. As a result, system designers do not have well-defined targets, making it harder to achieve and maintain compliance.

**What are our goals?** Our work focuses on understanding and quantifying the impact of GDPR on storage systems and cloud platforms. We are currently developing a benchmark, whose primary goal is to provide a measurable interpretation of GDPR compliance of storage systems. Our long term goal is to design and implement mechanisms and abstractions that make it easy for people to exercise their privacy rights, and for companies to efficiently achieve compliance.

### Publications
<br>
#### 1. How Design, Architecture, and Operation of Modern Systems Conflict with GDPR
*Supreeth Shastri, Melissa Wasserman, and Vijay Chidambaram* <br>
Accepted at [HotCloud 2019](https://www.usenix.org/conference/hotcloud19/). Preprint on [arXiv](https://arxiv.org/abs/1903.09305)

**Summary**: *In this paper, we review GDPR from a system design perspective, and identify how its regulations conflict with the design, architecture, and operation of modern systems. We illustrate these conflicts via the seven privacy sins: storing data forever; reusing data indiscriminately; walled gardens and black markets; risk-agnostic data processing; hiding data breaches; making unexplainable decisions; treating security as a secondary goal. Our findings reveal a deep-rooted tussle between GDPR requirements and how modern systems have evolved. We believe that achieving compliance requires comprehensive, grounds up solutions, and anything short would amount to fixing a leaky faucet in a burning building.* 
<br><br>

#### 2. Analyzing the Impact of GDPR on Storage Systems
*Aashaka Shah, Vinay Banakar, Supreeth Shastri, Melissa Wasserman, and Vijay Chidambaram* <br>
Accepted at [HotStorage 2019](https://www.usenix.org/conference/hotstorage19/). Preprint on [arXiv](https://arxiv.org/abs/1903.04880)

**Summary**: *Motivated by the finding that more than 30% of GDPR articles are related to storage, we investigate the impact of GDPR compliance on storage systems. We illustrate the challenges of retrofitting existing systems into compliance by modifying Redis to be GDPR-compliant. We show that despite needing to introduce a small set of new features, a strict real-time compliance lowers Redis’ throughput by ∼95%. Our work reveals how GDPR allows compliance to be a spectrum, and what its implications are for system designers. We discuss the technical challenges that need to be solved before strict compliance can be efficiently achieved.*
<br><br>

### Get in touch!
<br>
We are a group of CS and law researchers investigating privacy regulations from a systems perspective. We would love to hear from you. Please send a note to [Supreeth](mailto:shastri@utexas.edu) or [Vijay](mailto:vijay@cs.utexas.edu) if you have any questions, feedback, or collaboration.<br><br>


