# Predicate Dispatch
* core.logic
  * faithful rendition of mini-Kanren
  * adds some performance enhancements
  * adds a knowledge base capability
* Started with an interest in pattern matching
  * lazy pattern matching
  * led to effcient predicate dispatch (via paper by the self guy)
  * there was some language resistance but the nice thing about
    clojure is you can extend it yourself
  * can we do better than a hard-wired dispatch function as used in
    multimethods
* open dispatch vs. closed dispatch
  * a cond form that tests parameters would be a closed dispatch
  * a predicate matching form would be open
* unification is very similar
* core.logic/unify uses polymorphic dispatch and is simpler
* lots of ideas on doing pattern matching efficiency
* but how do you make it open?
  * supporting dynamism is hard
  * how to add new patterns without losing efficiency?
* non-overlapping clauses is important (inheritance would violate
  this)

## Questions
* maybe RETI has some applicability?

