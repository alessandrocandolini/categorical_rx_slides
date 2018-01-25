# Category theory and reactive extensions 
Slides for an introductory presentation about how abstract category theory and functional programming provide interesting and helpful insights into reactive extensions (aka Rx)

Despite not being (intentionally) an implementation of functional reactive programming (FRP) in the strict sense --- Rx lacks the rigorous time semantics in the spirit of the pioneering work by Paul Hudak and Conal Elliott back in their 1997 paper *Functional Reactive Animation* — and leaving room for side effects to bridge with imperative code, reactive extensions are indeed heavily shaped and influenced by several intriguing concepts and ideas borrowed from category theory and functional programming.

After a brief (and mostly incomplete) warm up reviewing few theoretical underpinnings, this talk will then walk through some concrete example to show how
scaring concepts like monads, mathematical duality, etc actually turn to be powerful weapons to help reason about reactive code, avoid common pitfalls & antipatterns, and design and develop better architectures that rely on reactive streams.

The core points will be:
* Rx is *not* a library about asynchronous behaviour; it does much better than that: it provides an abstraction on top of sync vs async behaviour, it allows inversion of control leaving to the consumer the possibility to *declarative* define the "threads" (actually parametrised by schedulers)
* The "reactive" of reactive extensions is not defined in terms of time; it's defined in terms of "push-based" (as opposite to "pull based") collections; this is linked to Observables being rigorously defined as the *dual* of iterables. This again leads to inversion of control on the responsibilities to retrieve the next element of the collection 
* Chainability of Observables is due to the monadic flavour of observables (no attempt to mathematical rigorour here, in particular for non-terminating observables ), allowing to focus on the "happy" path.

Some credits (I'll update the readme with more proper links, this is a preliminary list):
* Pictures are taken from wikipedia 
* The latex template is "metropolis"
* Railway driven development is taken from a beautiful talk about understanding the monads
