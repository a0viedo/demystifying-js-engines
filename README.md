This is a list of resources I used to learn about virtual machines in general, from an architecture point of view to optimizations and garbage collection strategies. I've also put together some parts into a talk format, you can see the slides [here][slides].

Contributions are very welcome!

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Virtual machines](#virtual-machines)
  - [JavaScript Engines](#javascript-engines)
    - [V8](#v8)
    - [JavaScriptCore](#javascriptcore)
    - [ChakraCore](#chakracore)
    - [SpiderMonkey](#spidermonkey)
    - [Benchmarks](#benchmarks)
  - [Inline caches](#inline-caches)
  - [Garbage collection](#garbage-collection)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

Emoji | Represents 
:---: | --- 
:bar_chart: | Blog post
:page_facing_up: | White paper
:computer: | Code
:microphone: | Podcast
:movie_camera: | Slides
:pencil: | Documentation

# Virtual machines

- :movie_camera: [Dynamic Compilation and Adaptive Optimization in Virtual Machines][dynamic-compilation-and-adaptive-optimization] - Stephen Fink, David Grove, and Michael Hind
- :page_facing_up: [On-stack replacement][osr] - Soman and Krintz
- :page_facing_up: [Optimizing Dynamically-Typed Object-Oriented Languages With Polymorphic Inline Caches][optimizing-dynamic-languages] - Hölzle, Chambers and Ungar
- :page_facing_up: [Adaptive optimization for self: reconciling high performance with exploratory programming][optimization-for-self]  - Hölzle
- :page_facing_up: [A Survey of Adaptive Optimization in Virtual Machines][survey-vm] - Arnold, Fink, Grove, Hind and Sweeney
- :page_facing_up: [A Simple Graph-Based Intermediate Representation][graph-based-ir] - Click
- :page_facing_up: [Combining Analyses, Combining Optimizations][combining-analyses-combining-optimizations] - Click

## JavaScript Engines
### V8
- :bar_chart: [A tour of V8 garbage collection][a-tour-of-V8-gc] - Jay Conrod
- [V8's compilers resources][v8-jits-resources] - Thorsten Lorenz
- [V8's garbage collector resources][v8-gc-resources] - Thorsten Lorenz
- :movie_camera: [TurboFan JIT Design][v8-turbofan-jit-design] - Ben L. Titzer
- :bar_chart: [Sea of Nodes][sea-of-nodes] - Fedor Indutny
- :bar_chart: [Digging into TurboFan JIT][digging-into-turbofan-jit] - V8's blog
- :bar_chart: [Jank Busters Part One][jank-busters-1] - V8's blog
- :bar_chart: [JavaScript and V8’s TurboFan][js-and-v8-turbofan] - Ariya Hidayat
- :page_facing_up: [Instrumenting V8 to Measure the Efficacy of Dynamic Optimizations on Production Code][instrumenting-v8] - Maass and Shafer
- :bar_chart: [V8 resources][v8-resources] - Vyacheslav Egorov

### JavaScriptCore
- :bar_chart: [Introducing FTL JIT][introducing-ftl-jit] - Webkit blog
- :bar_chart: [Introducing B3 JIT compiler][introducing-b3-jit] - Webkit blog
- :pencil: [Bare Bones Backend][b3-docs] - Webkit Documentation
- :pencil: [B3 Assembly IR][b3-assembly-ir-docs] - Webkit Documentation
- :pencil: [B3 IR][b3-ir-docs] - Webkit Documentation
- :pencil: [FTL JIT][ftl-docs] - Webkit Documentation

### ChakraCore

- :computer: [List of performance hint descriptions][chakracore-perf-hints] - ChakraCore's repository
- :microphone: [Chakra, Microsoft's Open Source JavaScript Engine][javascript-air-chakracore] - JavaScriptAir
- :pencil: [ChakraCore Architecture overview][chakracore-arquitecture-overview] - ChakraCore's wiki

### SpiderMonkey
- :bar_chart: [Compacting Garbage Collection in SpiderMonkey][compacting-gc-in-spidermonkey] - Mozilla Hacks
- :bar_chart: [SpiderMonkey Internals][spidermonkey-internals] - MDN


### Benchmarks
- [Introducing the JetStream Benchmark Suite][jetstream]
- [Sunspider][sunspider]
- [Octane][octane]
- [Kraken][kraken]
- [Dromaeo][dromaeo]
- [AreWeFastYet?][AWFY]

## Inline caches

- :bar_chart: [PICing on JavaScript for fun and profit][picing] - Chris Leary

## Garbage collection

- :bar_chart: [Back to basic: Series on dynamic memory management][dynamic-mem-mgmt] - MSDN
- [Memory Management Reference][memory-management-reference]
- :page_facing_up: [A non-recursive list compacting algorithm][a-nonrecursive-list-compacting-algorithm] - Cheney
- :page_facing_up: [Generation Scavenging][generation-scavenging] - Ungar
- :page_facing_up: [Reconciling Responsiveness with Performance in Pure Object-Oriented Languages][perf-oo-languages] - Hölzle and Ungar
- :page_facing_up: [Garbage Collection in an Uncooperative Environment][GC-in-an-uncooperative-env] - Boehm
- :page_facing_up: [Garbage Collection with Ambiguous Roots][GC-with-ambiguous-roots] - Bartlett
- :page_facing_up: [Quantifying the Performance of Garbage Collection vs. Explicit Memory Management][gc-perf-vs-explicity-mem] - Hertz and Berger
- :page_facing_up: ['Infant Mortality' and Generational Garbage Collection][infant-mortality-and-gc] - Baker
- :page_facing_up: [Fast Conservative Garbage Collection ][fast-conservative-gc] - Shahriyar, Blackburn and McKinley




[picing]: http://blog.cdleary.com/2010/09/picing-on-javascript-for-fun-and-profit
[chakracore-perf-hints]:https://github.com/Microsoft/ChakraCore/blob/master/lib/Runtime/Base/PerfHintDescriptions.h
[GC-in-an-uncooperative-env]: http://www.hboehm.info/spe_gc_paper/preprint.pdf
[GC-with-ambiguous-roots]: http://www.hpl.hp.com/techreports/Compaq-DEC/WRL-88-2.pdf
[gc-perf-vs-explicity-mem]: http://people.cs.umass.edu/~emery/pubs/gcvsmalloc.pdf
[dynamic-mem-mgmt]: https://blogs.msdn.microsoft.com/abhinaba/2009/01/25/back-to-basic-series-on-dynamic-memory-management/
[memory-management-reference]: http://www.memorymanagement.org/
[survey-vm]: https://www.complang.tuwien.ac.at/andi/vm-survey.pdf
[infant-mortality-and-gc]: http://home.pipeline.com/~hbaker1/YoungGen.html
[a-tour-of-V8-gc]: http://jayconrod.com/posts/55/a-tour-of-v8-garbage-collection
[a-nonrecursive-list-compacting-algorithm]: https://people.cs.umass.edu/~emery/classes/cmpsci691s-fall2004/papers/p677-cheney.pdf
[generation-scavenging]: https://people.cs.umass.edu/~emery/classes/cmpsci691s-fall2004/papers/p157-ungar.pdf
[perf-oo-languages]: https://www.cs.ucsb.edu/~urs/oocsb/papers/toplas96.pdf
[introducing-ftl-jit]: https://webkit.org/blog/3362/introducing-the-webkit-ftl-jit/
[introducing-b3-jit]: https://webkit.org/blog/5852/introducing-the-b3-jit-compiler/
[dynamic-compilation-and-adaptive-optimization]: https://www.research.ibm.com/people/d/dgrove/papers/pldi04-tutorial.pdf

[compacting-gc-in-spidermonkey]: https://hacks.mozilla.org/2015/07/compacting-garbage-collection-in-spidermonkey/
[javascript-air-chakracore]: https://javascriptair.com/episodes/2016-01-27/
[chakracore-arquitecture-overview]: https://github.com/Microsoft/ChakraCore/wiki/Architecture-Overview
[spidermonkey-internals]: https://developer.mozilla.org/en-US/docs/Mozilla/Projects/SpiderMonkey/Internals
[v8-gc-resources]: https://github.com/thlorenz/v8-perf/blob/master/gc.md
[instrumenting-v8]: https://www.cs.cmu.edu/~mmaass/pdfs/CMU-ISR-13-103.pdf
[fast-conservative-gc]: https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/conservative-gc-oopsla-2014.pdf
[graph-based-ir]: http://www.oracle.com/technetwork/java/javase/tech/c2-ir95-150110.pdf
[combining-analyses-combining-optimizations]: https://www.researchgate.net/publication/2394127_Combining_Analyses_Combining_Optimizations
[v8-turbofan-jit-design]: https://docs.google.com/presentation/d/1sOEF4MlF7LeO7uq-uThJSulJlTh--wgLeaVibsbb3tc/edit?usp=sharing
[sea-of-nodes]: http://darksi.de/d.sea-of-nodes
[digging-into-turbofan-jit]: https://v8project.blogspot.com.ar/2015/07/digging-into-turbofan-jit.html
[jank-busters-1]: https://v8project.blogspot.com.ar/2015/10/jank-busters-part-one.html
[js-and-v8-turbofan]: https://ariya.io/2014/08/javascript-and-v8-turbofan
[jetstream]: https://webkit.org/blog/3418/introducing-the-jetstream-benchmark-suite/
[conservative-gc-algorithm-overview]: http://www.hboehm.info/gc/gcdescr.html
[dromaeo]: http://dromaeo.com
[kraken]: http://krakenbenchmark.mozilla.org
[octane]: https://developers.google.com/octane/
[sunspider]: https://webkit.org/perf/sunspider/sunspider.html
[osr]: https://www.cs.ucsb.edu/~ckrintz/papers/osr.pdf
[ignition-talk]: https://www.youtube.com/watch?v=r5OWCtuKiAk

[optimizing-dynamic-languages]: http://hoelzle.org/publications/ecoop91.pdf
[optimization-for-self]: http://hoelzle.org/publications/urs-thesis.pdf

[v8-jits-resources]: https://github.com/thlorenz/v8-perf/blob/master/compiler.md
[AWFY]: https://arewefastyet.com/
[slides]: https://slides.com/a0viedo/demystifying-js-engines

[v8-resources]: http://mrale.ph/v8/resources.html


[ftl-docs]: http://trac.webkit.org/wiki/FTLJIT
[jsc-docs]: http://trac.webkit.org/wiki/JavaScriptCore
[b3-docs]: https://webkit.org/docs/b3/
[b3-assembly-ir-docs]: https://webkit.org/docs/b3/assembly-intermediate-representation.html
[b3-ir-docs]: https://webkit.org/docs/b3/intermediate-representation.html