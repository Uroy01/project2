1. Describe how your prefetcher works.
The customer prefetcher that I used is a Next Line + Predicted Next Miss (NL+PNM) prefetcher.In this case, first sequential prefetcher is implemented which that takes an
input, then my prefetcher predicts what  will be the next miss and prefetches those lines. It checks the next missed line after the address is called. If the next missed line after an address is called is the same twice in a row, previously then my prefetcher will 
prefetch this consecutively missed line as well. The prefetcher will prefetcher will prefetch the two most recently consecutively missed lines.

2. Explain how you chose that prefetch strategy.
I selected this prefetching strategy because one becuase it did not improve prefetcher efficiency using any other methods. I did my research on other strategies, but saw that the other strategies try to improve prefetching efficiency by finding clever ways to optimize
prefetching with regards to prefetching latency and when lines need to be prefetched in regards to when they may be needed. however, it seemed like the simulator did no support this kind of efficiency. 

3. Discuss the pros and cons of your prefetch strategy.
Pros: This prefetcher handles things very well like linked lists, where there may be lines that are often called sequentially that are not 
spacially near each other in memory.
Cons: If there is no pattern in how the data is called, or the data is mostly spacially local, then the Predicted Next Miss portion of my prefetcher induces
additional overhead from a normal Sequential prefetcher without much added benefit. 

4. Demonstrate that the prefetcher could be implemented in hardware (this can be as simple as pointing to an existing hardware prefetcher using the strategy or a paper describing a hypothetical hardware prefetcher which implementsyour strategy).
According to my research - The paper "The FNL+MMA Instruction Cache Prefetcher" by Andre Seznec details how this prefetcher could work using what the author calls an I-Shadow cache, although the paper mostly focuses on the implementation of a more complicated version of the prefetcher I implemented called the FNL+MMA prefetcher. 

5. Cite any additional sources that you used to develop your prefetcher.
I did several researches from several books - few of them is Computer system architecture by Jean loop Baer, Computer Architecture by John L Hennessy and modern Computer Architecture by Jim Ledin. I took reference from these books to understand how prefetcher works and based on that, created my own.
