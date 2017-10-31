Program site: https://www.sigops.org/sosp/sosp17/program.html
Questions site: https://app.sli.do/event/e3ouyhid/ask

Q: When the skewness is shifted, there is any policy of deleting/rearranging guards? and overhead about this? Thank you.
A: Currently, PebblesDB doesn't have a policy to delete or rearrange guards. FLSM is designed in such a way to balance all the data between the guards well, but we could definitely explore more about rebalancing guards in FLSM. 

Q: How often do you have to change guards and what's the overhead of doing so?
A: In PebblesDB, once the guards are chosen, they are not changed. But when a new guard is inserted in between two existing guards, the files in the guards need to be split according to the new guard and this happens asynchronously during the background compaction. This overhead of introducing a new guard is amortized in the cost of background compaction which anyways happens. 

Q: 'In most cases', is there any bound for write time?in worst case, what is the # of write times? The worse case may influence tail latency, right?
A: The bound for the write time heavily depends on the limit set on the number of level 0 files. As the limit increases, the write throughput also increases and hence write latency decreases. For a given limit on the number of level 0 files, FLSM always higher write throughput compared to other key-value stores for random-writes experiment. 

Q: I wan to study the IO amplification problem in detail. Some of the latest papers appear in MSST17 and TPDS17, how can I download your paper? Thank you.
A: https://dl.acm.org/authorize.cfm?key=N47264

Q: I wonder about the space fragmentation and how to deal with redundant keys in same level. It looks like FLSM does not deduplicate keys when it merges a guard.
A: Good question. We do have little overhead in terms of space amplification (very nominal - around 2- 5%). We did an experiment where we inserted 5M key-value pairs 10 times (total 50M key-value pairs with only 5M unique keys) and we saw that PebblesDB had around 2-5% overhead with respect to the space amplification compared to the other key-value stores. 

Q: If all the keys have low number(skewness) and guards cannot divide into multiple sub-sections, isn't it same with LSM (Which may be rare)?
A: In such a skewed case, more data might be present within a few guards (closer to LSM) but FLSM still reduces write amplification. Also, depending on the data set, a configurable parameter can be used to tune the number of guards desired, with this config, we can increase the number of guards for such a skewed data. 
