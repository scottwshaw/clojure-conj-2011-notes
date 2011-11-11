# Extending JavaScript Libraries from ClojureScript
* gave a handout
* 3 points
  * clojure is easier than javascript
  * clojure is more fun and safe than javascript
  * it will be an adventure of learning by looking at things
    differently through clojurescript
* it will take a long time if clojure will take over from javascript
  (!?) so the interoperability is an important consideration
* Bendan Eich (creator of javascript) "javascript has a lot of stupid
  in it"
  * Examples: 
	* globals, can be changed from anywhere, even another program --as
      compared to-- clojure where things just don't change
	* namespaces: only created by closures
* Coffeescript will not save you since it really only is syntactical
  improvement
* Using Clojurescript gives you namespaces
* There's a myth that Clojure is only for geniuses
* Access any javascript method via . syntax (.log js/console "hello
  world"), etc. etc.

## Clojure makes it easier to extend javascript libraries than
   javascript native
* (-> js/jQQuery)
   (.select "#main")
   (my-appender "<span>")
   (.text "hello"))
* good to build facades in Clojure for jQuery method calls
* plug for D3

## what we thought we knew until clojurescript showed us otherwise
* you might get hurt
* Uh oh, need to talk about "this"
* referential transparency, use of apply

## Advice
* Tools don't make the artist
* in the end it is the outcome that matters
* we went to the moon with inches and sliderules--we can do what we
  want with PHP if we have to.

	
