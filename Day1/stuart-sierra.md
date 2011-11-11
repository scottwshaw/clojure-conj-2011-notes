# Next Steps
## Serialisation
* prn prints stuff that the reader can consume
* read-string reads it back in
* \*print-dup\* makes sure same type is printed and read
  * need to use #=() as back door into reader when reading back
* resources
  * in leiningen, can put stuff in /resources and read in data
  * improvement on JSON because richer set of types
* Could write your own reader this way

## Interfaces
* All of Clojure implemented as interfaces
* which one? example: (ancestors (class [])) lists lots and lots of
  interfaces
  
## Concurrency
* Interesting use of -> here to apply an infinite sequence of
  functions to an object
* some ways to use java.util.concurrent in Clojure code for specific
  uses and performance improvements
  * Concurrent Collections: can be accessed simultaneuously by
    multiple threads but non-interfering (?)
* Ideas
  * Some research going on about distributed locks and transactions in
    the Clojure community
	
## Other stuff
* clojure.test.generative
  * embed specs in the function definition that check the validity of
    parameters
* clojure.core.logic
  * logic programming
	

