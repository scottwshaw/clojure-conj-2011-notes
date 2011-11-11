# Clojail
* Stuart Halloway's introduction, priceless
* Anthony is author of Try Clojure, 17 y.o.
* If you allow someone to inject code to your systems via and IRC bot
  or something, you need a sandbox
* hard part is sandboxing Clojure itself, not the type of sandbox the
  JVM provides--like what if the namespace gets corrupted.
* Try Clojure, 4Clojure, Lazybot all need sandboxing
* Clojail is an all-purpopse sandbox for Clojure
* Takes a set of things from Java that might cause trouble--if you try
  ot use those it trips an alarm.
* times out any long-running operation after a configurable timeout
  (default 10s)
* sets a maximum number of things you can def.  If exceeded, it undefs
  the n previous
  * Can set up defs on init that are excepted
* Can also set up bindings that apply to the whole sandbox

## Implementation
* first explode and flatten the expressions then check each form
  * Uses juxt, which is comp left-to-right instead of right-to-left
* second, instruments code to check things at runtime
  * like replacing . with a dot macro
* timeouts on threads by creating a special threadgroup with a timeout
  (thunk-timeout)
  * Disallows use of any threadpool stuff like agents or futures
* Amazingly, implementation of the sandbox function fits on a slide,
  albeit with small font
* Try Clojure runs on Heroku (based on Noir framework)
  * Each user has their own namespace
* 4Clojure uses "dynamic sandboxing"
* Lazybot
* Guidelines
  * Use JVM sandbox whereever possible
  * avoid sharing namespaces
  * don't allow def in one shared namespace




