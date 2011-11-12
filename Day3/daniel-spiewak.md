# Functional Data Structures
* Theory and implementation of 5 functional data structures
* 2 kinds, Sequential and Associative
* Should have asymptotic similar peformance to sequential (mutable) counterparts
* What are they?
  * immutable
  * Structural sharing

## Singly linked list
* most stuff is linear time--not great but workable
* structural sharing -- can do this when everything is immutable

## Banker's queue
* want same time for prepend and last (linked list would be O(1) and
  O(n))
* BQ more or less constant time for last
* two linked lists, front and back, enqueue rear, dequeue front
* amortizes the cost of occasionally reversing and concatenating the
  rear list so you can dequeue things from there in constant time

## 2-3 Finger Tree (a better queue)
* complicated
* constant time access to head or tail
* logn time to middle of data structure
* tree with head and tail at root
* complexity when 

## Associative structure: red-black tree
* logn time for most stuff
* linear time for intersect and union
* b-tree
* need to rebalance tree after every update
* unteresting thing is the rebalancing function
* nice concise Scala implementation of the rebalancing function using
  pattern matching (unreadable but concise)

## Bitmapped Vector Trie (combination of the two)
* This is the Clojure vector
* most operations log base 32 n, which for the largest integer is
  about 7
* nested arrays of max length 32

## Modern Archteitures
* Locaity of reference, caching, jvm stuff
* The JVM compensates for the lack of these things cleverly recognizes
  structural patterns and keeps those structures close together in
  memory
  * makes 2-3 finger tree actually slow because jvm gets confused and
    creates lots of cache misses

## references
* read Okasaki "purely functional data structures", meditate on it
