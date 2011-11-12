# Macronomicon
* A macro koan--what is the true power of the macro?
* programs writing programs

## A history
* C - preprocessor directives
* C++ template metaprogramming
* OCaml

## Lisp Macros 
* A gun that shoots backwards
* McCarthy's original eval with macros added by Timothy Hart
 * (eval (eval (...))
* control flow and binding with macros can be done equally elegantly
  in other ways in Ruby 
* Baysick: Scala that looks like BASIC
* Mapping dilema: the underlying abstraction pokes through
* Other use cases
  * ...
  
## Hygene (what is it?)
* problems with namespaces - expansion qualifies the variables in the
  curent namespace

## DSLs
* hard to write so that underlying language doesn't bubble up
* instead, create MSLs (mood-specific languages)
* Why wait for Rich?
  * you can use macros to create new syntax things

* Primacy of Semantics vs. Primacy of Syntax
* Can you create a syntax that directly expresses the semantics so
  they go away?
* Primacy of data
* What's the fastest way to multiply two numbers?  "take the answer
  and put it there"
  * Do the calculations in the compiler so it's there before runtime
