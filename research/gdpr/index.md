---
layout: default
title: GDPR from Systems Perspective
---

<br>
<img style="float:left" src="/img/gdpr.png" width="27%" height="27%" hspace="8"> On May 25th 2018, after nearly two years of public debate, the European parliament adopted the [General Data Protection Regulation](https://en.wikipedia.org/wiki/General_Data_Protection_Regulation). Alarmed by a global trend of data breaches and privacy violations, this regulation declares the protection and privacy of personal data as a fundamental right of all the European people. Thus, any company dealing with EU customers is legally bound to comply with GDPR. While essential, achieving compliance is not trivial: [Gartner](https://www.gartner.com/en/newsroom/press-releases/2017-05-03-gartner-says-organizations-are-unprepared-for-the-2018-european-data-protection-regulation) estimates less than 50% compliance rate by the end of 2018.<br><br>

We take a systems focus in investigating GDPR. First, we examine how GDPR affects the design and operation of modern computing systems. Surprisingly, our analysis reveals that several design principles and architectural elements of real-world systems are at odds with the proposed regulation. We highlight seven such principles and practices, [**the seven privacy sins**](), by discussing how they came to be, reviewing the conflicting regulations, and chronicling their real-world implications. We argue that achieving compliance requires comprehensive, grounds up solutions, and anything short would amount to simply *fixing a leaky faucet in a burning building*.

In our second exploration, motivated by the finding that more than 30% of GDPR articles are related to storage, we investigate GDPR's impact on [**storage systems**](). We illustrate the challenges of retrofitting existing systems into compliance by modifying Redis to be GDPR-compliant. We show that despite needing to introduce a small set of new features, a strict real-time compliance lowers Redis’ throughput by ~95%. We outline the technical challenges that need to be solved before strict compliance can be efficiently achieved.

### Publications
**How Design, Architecture, and Operation of Modern Systems Conflict with GDPR**<br>
*Supreeth Shastri, Melissa Wasserman, and Vijay Chidambaram*<br>
[arXiv]()

**Analyzing the Impact of GDPR on Storage Systems**<br>
*Vinay Banakar, Aashaka Shah, Supreeth Shastri, Melissa Wasserman, and Vijay Chidambaram*<br>
[arXiv]()

### Contact Us 
We would love to hear from you. Please send a note to [Supreeth](mailto:shastri@utexas.edu) or [Vijay](mailto:vijay@cs.utexas.edu) for any questions, feedback, or collaboration.
