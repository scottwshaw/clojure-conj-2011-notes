# Logs as Data
* code as data, html as data markup as data, sql queries as data,
  build specs, cloud deploys, ... as data
* hiding data prevents maniupulating data through simple abstractions
  such as map, seq, fn  (such as Java classes do)
* this allows very general libraries that don't require coupled
  knowledge of underlying data types
* Is current Java logging like this?
  * well, it isn't data because it is an unstructured string
  * simple abstraction? have you looked at a log4j configuration file?
* <<key concept here is that features should be implemented in such a
  way that they can bemanipulatedwiht eht simple general tools
  provided by the language-- this differes from the Java philosophy
  that you need a special purpose framework for every new entity.  I
  think this is a fundamentalphilosophical difference between the fp
  and current enterprise procedural world >>
* Need a fundamental model for crossing logs with events
* mant event streams coming into an aggregator, emitting different
  streams in response to different functions
  * debugging
  * auditing
  * metrics
  
## Example: Heroku Pulse (https://github.com/heroku/pulse.git)
* dashboard grid of graphs from different functions acting on Heroku's
  event stream
  
  (defstat ps-lamch-time-mean
    (mean 60
	  (fn [e] ...)
	  (fn [e] ...)
	  (fn [e] ...)))
* organised in layers of aggregation, statistical calcuations,
  forked presentation
* fundamentally though, this is nothing more than a function operating
  on a stream.
* Event processing is an area where Clojure can really shine
* Example tools: Esper Hadoop Cascading Cascalog Storm Conduit
* Heroku is building an entire team around this concept

# Questions
* This talk has specifically avoided the topic of how you parse
  text-based logs into data-oriented events.  This is necessary
  * OSS projects 
* Currently using TCP as the communication protocol
* Rich: Is the aggregator just an ordinary message queue
  * currently using something called logplex as the aggregator
* data formats are a problem, parsing and maintaining your own
  proprietary format.

