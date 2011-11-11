# From Linear to Incremental
* One of the counterclockwise contributors
* Incremental parsing: remopute teh whole parse tree at a fraction of
  the cost after an edit
* parsing can be cast as a reduction (get-tree (reduce parse-step init
  input))
  * but reduce is somewhat bad ("slightly harmful" according to guy
    steele) because it is inherently sequential
* Lots of stuff about precomputing partial functions from a reduce
  combined with memoization to remember the pieces of the computation
  that haven't changed.
  * LR parsing with 2 stacks, stack transplantation
  * This can do reduction in log time
* Written a demo of this as parsely
  * recomputes the parse tree in response to a change in a faction of
    the time it takes to originally parse 200ms -> 1ms


