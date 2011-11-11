# Clojure and Android
* Differences between JVM and Dalvik VM
  * Not the same executable format as JVM
* Dynamic compilation on Android
  * a repl running on the device, pretty cool
  * Wow, pretty impressive, changing the repl itself, uploading it
    into the android device simulator and continuing with the
    dynamically compiled change.
* considerations
  * small package size.  Need to keep small
  * startup time. Clojure takes 2.3 seconds, most apps take a few
    hundred milliseconds
  * small memory: clojure takes up 1.2MB
* Where does all this time and memory go?
  * can't be eliminated
  * lots of the space is taken up by stuff you don't really need on a
    mobile app
  * What about the time?  Most of it is in loading clojure.core and
    garbage collecting during that loading process
* Would help to have a standard library for Clojure/Android
  development
  * github.com/sattvik/neko - boilerplate stuff
  * build tools - Neko has some support for Ant/Android, but need
    better support for standard build tools
* What about Clojurescript
  * good for web development
  * currently not good support for native android features
* Clojure could be first class language for Android
  * dynamic development is killer feature only available through
    clojure
  * Needs better tool support
