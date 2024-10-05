# Order Of Volatility
This is a copy-paste from [Computer Forensics Reporter](https://www.computer-forensics-recruiter.com/order-of-volatility/) <br> 
For tools and methods: <br>
[Windows](https://aditya-pratap9557.medium.com/windows-memory-forensics-using-open-source-tools-3ec09930732e)
[Linux](https://cybersecurity.att.com/blogs/security-essentials/volatile-data-acquisition-from-live-linux-systems-part-i)
[Linux memory](https://cybersecurity.att.com/blogs/security-essentials/volatile-data-acquisition-on-linux-systems-using-fmem)
- [Order Of Volatility](#order-of-volatility)
    - [Registers, Cache](#registers-cache)
    - [Routing Table, ARP Cache, Process Table, Kernel Statistics, memory](#routing-table-arp-cache-process-table-kernel-statistics-memory)
    - [Temporary File Systems](#temporary-file-systems)
    - [Disk](#disk)
    - [Remote Logging and Monitoring Data that is relevant to the System in Question](#remote-logging-and-monitoring-data-that-is-relevant-to-the-system-in-question)
    - [Physical Configuration, Network Topology, and Archival Media](#physical-configuration-network-topology-and-archival-media)
---
### Registers, Cache
The contents of CPU cache and registers are extremely volatile, since they are changing all of the time. Literally, nanoseconds make the difference here. An examiner needs to get to the cache and register immediately and extract that evidence before it is lost.
### Routing Table, ARP Cache, Process Table, Kernel Statistics, memory
Some of these items, like the routing table and the process table, have data located on network devices. In other words, that data can change quickly while the system is in operation, so evidence must be gathered quickly. Also, kernel statistics are moving back and forth between cache and main memory, which make them highly volatile. Finally, the information located on random access memory (RAM) can be lost if there is a power spike or if power goes out. Clearly, that information must be obtained quickly.
### Temporary File Systems
Even though the contents of temporary file systems have the potential to become an important part of future legal proceedings, the volatility concern is not as high here. Temporary file systems usually stick around for awhile.
### Disk
Even though we think that the data we place on a disk will be around forever, that is not always the case (see the SSD Forensic Analysis post from June 21). However, the likelihood that data on a disk cannot be extracted is very low.
### Remote Logging and Monitoring Data that is relevant to the System in Question
The potential for remote logging and monitoring data to change is much higher than data on a hard drive, but the information is not as vital. So, even though the volatility of the data is higher here, we still want that hard drive data first.
### Physical Configuration, Network Topology, and Archival Media
Here we have items that are either not that vital in terms of the data or are not at all volatile. The physical configuration and network topology is information that could help an investigation, but is likely not going to have a tremendous impact. Finally, archived data is usually going to be located on a DVD or tape, so it isn’t going anywhere anytime soon. It is great digital evidence to gather, but it is not volatile.