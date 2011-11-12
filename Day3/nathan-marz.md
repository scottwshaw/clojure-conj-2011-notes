# Cacalog
* "I love Clojure in the morning"
* Analyse Tweets about tunisia during the revolution using Cascalog
* Cascalog is a high-level abstraction on top of hadoop map reduce
* Hadoop is 
  * high-latency batch processing
  * fault tolerant
  * ...
* complex logic hard to express in map reduce
* data analysis is programming and you need abstraction and
  composition, a fact often missed in the data community
* Cascalog lets you define and execute over tuples queries composed of predicates
  * functions filters aggregators generators
* (?<- (stdout) [?person] (full-name ?person ?name)
  (extract-first-name ?name :> ...)
  
  (?<- (stdout) [?age] (age ?person) ...)
  * This triggers a join:
  (?<- (stdout) [?person] (follows "emily" ?person) (gender ?person
  ",")) 
* a bunch of code examples now  which are on nathan's github account
* can create subqueries
* <- without the ? defines a query but doesn't execute it

## The Tunisia Data Model
* code examples on https://github.com/nathanmarz/cascalog-conj
* A bunch of relations between people and tweets in JSON format
* Using a first class language (as opposed to SQL variant) lets you
  define interesting functions as part of your queries seamlessly.
* Queries using some functions defined in Clojure and streaming to
  Incanter to produce some nice graphs.  *Nice!*
* 
