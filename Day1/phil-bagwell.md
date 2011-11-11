# Striving to Make Things Simple and Fast
* Typesafe and epfl
* Threw out chocolates
* To overcome learning curve of tech adoption
* Reduce learning difficulty and increase payoff 
* Parallel collections: automatic parallelization of comprehensions
* good for multicore. Needs good load balancing
* no blocking resizable concurrent hash tries. 
  * immutable snapshots 
  
## the real topic
* vectors -- concatenation takes linear time in size of one of them 
* immutable updatet can be done in nlogn with radix indexing
* index lookup takes advantage of caching
* can concat be done in nlogn?
* Hit on relaxed radix b trees constant time log
* in the end, this efficiency in the language implementation allows developers to take advantage 
