# Modeling the world probabilistically using Bayesian networks in Clojure
* Why Bayesian networks?
  * decisions are traceable--you can answer why
* Credits
  * "Modeling and Reasoning with Bayesian Networks" (more practical
    knowledge than Pearl)
* Standard Bayesian rationale, data is incomplete, redundant, noisy,
  blah blah blah
* Example: document analysis
  * Chas' particular area of interest is in extracting data from
    unstructured documents like SEC filings
* Truth tables
  * look like joint pdfs
* 1 minute Bayesian probability: Bayes law
* fundamental problem, joint probabilities don't scale.  Truth tables
  grow multiplicatively
  * However, with causality, you can form chains of inference: Bayesian Network
  * might manually create a model or build one through various search
    mechanisms
  * reduces computations to nlog(something)
* Raposo: Clojure lib for Bayesian inference and modeling
* Simple modeling syntax using a map



