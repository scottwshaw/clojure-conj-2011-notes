# Concurrent Stream Processing
* want to do concurrent SPARQL query processing,
  * Source data arriving in streams
* Unix pipes as the inspiration
  * Pipes: asynch, buffered, EOF
* want to be able to fork and join pipes
* pipe protocol
  * enqueue, close, error, dequeue, etc....
* nodes are like a process
  * consist of fields :input-pipe, :output-pipe, :task-fn, etc....
* can create trees of processes that 
* threads run on nodes
* Node activities are queued in response to a callback on a pipe.  A
  thread from the pool (Java ForkJoinPool) will be used to execute
  task asynchronously.
* pipe data can be buffered to disk when heap memory is low
* exceptions, timeouts, etc. are percolated up globally
* Clojure expressions at the leaves of the tree.
* stream operators mirror Clojure sequence operators
* Chunk operators
* Can write macros that implement your own stream operators
* 2 different implementations
  * Compiles
  * evals to stream expressions
* Compiler uses a zipper to walk the tree
* An alternate version that uses eval and macros wasn't as easy to
  understand because macros get complex (too many squiggles and ticks)


