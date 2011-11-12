# Areas of Interest for Clojure's Core

## Leaner
* Need to deliver smaller targets
* No support right now for releasing non-dev builds but there is a lot
  that can be removed

## Unification with ClojureScript
* Unifying to a single AST to support tooling
* Original clojure ast isn't great due to use of dynamic variables and
  other stuff
  
## Clojure in Clojure
* value demonstrated by ClojureScript
* Some stuff about where protocols get implemented, at the bottom
  layer or top that I don't really understand

## invokedynamic
* Will allow faster dynamic variables
* reflection-free interoperability
* Mostly give the ability to optimise

## Leveraging Logic
* "wite Clojure as a logic program and run it backwards to find
  startup ideas"
* queryable programs
* predicate dispatch
  * don't settle for pattern matching
  * core logic might not be fast enough
* << interesting explanation by Rich of an assertion made earlier
  today about pattern matching in the predicate dispatch talk >>

## Parallelism
* fork/join style logic is a reasonable way to handle lots of
  connections--you don't need asynch I/O to do that.  You can have
  pending connections <<Hmm...>>
* but fork/join doesn't support balanced workloads

## Transients and Beyond
* Like the model mentioned earlier where you can have snapshots for a
  mutable object
* Pods - separate the access policy from the data structure
  * Some examples of how you would use a Pod
  * You can have diffrerent policies if you want--multi-threaded
    access, etc. -- involves mutexes, but you have control over it and
    can manage lock acquisition order, etc.

## Accumulators

## Extensible Reader
* Clojure data as a serialisation format--much better than JSON?
  * metadata, more types, keywords
  * However, isn't extensible like XML--end up encoding things as
    nonstandard string formats but then move away from self
    description
* Need more types (but not too many)
* How
  * Tags
* Could this be the wedge into the enterprise?
