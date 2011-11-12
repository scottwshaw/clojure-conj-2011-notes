# Performance in the Wild
* Performance is a cycle you repeat until you're done
  * measure
  * benchmark
  * optimize
* The world is stochastic--you need a model
* You can answer what-if questions if you have a good model that
  measures the stochastic response
* Of course, the model is wrong
  * testing vs prod
  * small vs. large data
  * load balancing?
  * *This isn't an excuse for not building a model and testing*
* Answer the question: what is the *distribution* of latencies for a
  given load, thoughput, transaction mix, plus whatever else
  * *measure latency vs. req/s, not response time/number of users*
* Usually, we plot throughput over time.  Instead, we should be
  plotting the distribution of latencies
* 3 Questions
  * can we meet customer expectations?
  * how much capacity?
  * ...
* So you've done your measurements, you're not fast enough, how do you
  know where you're slow? -> profiling
  * yourkit -- awesome tool
  * lots of hard thinking
* Optimize
  * fix the one slowest thing
  * redesign may be necessary
  * therefore should have started early
* A real-world case study
  * ran jmeter tests every night and emailed results
  * Once an inadvertant 1-char change in a config file created 2x
    slowdown
	* wouldn't have been caught otherwise
  
