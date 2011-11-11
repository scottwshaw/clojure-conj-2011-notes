# ClojureScript
* Chris is one of the authors of "Joy of Clojure"
* Clojure, ClojureScript, Clojure, Closure, Clojure, Closure,
  etc. etc.
* Tour of some of the internals
* Clojure vector compiles directly ot javascript arrays
* Maps compile differently depending on the type of keys (ObjMap or
  HashMap)
  * creates a string representation of keywords using a special
    unicode character
* Set becomes a set
* Ooh!  Can extend an imported type dynamically and have the extension
  method available immediately to an existing instance.
  * Example: implement ILookup interface on a gs/Map object so Clojure
    map (get) function works
  * Introduces problems of composability if there is a clash of
    interfaces with the same method
  * This isn't how regular Clojure does protocols
* How do you implement macros?
  * Look more closely at the eval step
  * ...
  * Macros end up as Clojure code, no javascript has been executed yet
* Question: are you looking at porting the regular Clojure
  implementations of collections that support really big collections
  in memory?
  * Answer: people aren't doing that sort of thing in Javascript *yet*
    but would be necessary
	

