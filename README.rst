========================================
Valgrind Plugins Collection
========================================

The goal of this repo is to collect any Valgrind's plugin (official or third party).

Plugins
========================================

+------------------+--------------------------------------------------------+----------------------------+
| Plugins          | Description                                            | Provider                   |
+==================+========================================================+============================+
| Memcheck         | a memory error detector                                | official                   |
+------------------+--------------------------------------------------------+----------------------------+
| Cachegrind       | a cache and branch-prediction profiler                 | official                   |
+------------------+--------------------------------------------------------+----------------------------+
| Callgrind        | a callgraph analyzer                                   | official                   |
+------------------+--------------------------------------------------------+----------------------------+
| Helgrind         | a thread error detector                                | official                   |
+------------------+--------------------------------------------------------+----------------------------+
| DRD              | a thread error detector                                | official                   |
+------------------+--------------------------------------------------------+----------------------------+
| Massif           | a heap profiler                                        | official                   |
+------------------+--------------------------------------------------------+----------------------------+
| Lackey           | an example tool                                        | official                   |
+------------------+--------------------------------------------------------+----------------------------+
| Nulgrind         | the minimal Valgrind tool                              | official                   |
+------------------+--------------------------------------------------------+----------------------------+
| DHAT             | [exp] a dynamic heap analysis tool                     | official                   |
+------------------+--------------------------------------------------------+----------------------------+
| SGCheck          | [exp] a stack and global array overrun detector        | official                   |
+------------------+--------------------------------------------------------+----------------------------+
| BBV              | [exp] basic block vector generation tool               | official                   |
+------------------+--------------------------------------------------------+----------------------------+
| ThreadSanitizer_ | (discontinue) Race detection tools and more            | Google                     |
+------------------+--------------------------------------------------------+----------------------------+
| Fuzzgrind_       | (discontinue?) automatic fuzzing tool                  | Gabriel Campana            |
+------------------+--------------------------------------------------------+----------------------------+
| Flayer_          | (discontinue?) Taint analysis and flow alteration tool | Will Drewry, Tavis Ormandy |
+------------------+--------------------------------------------------------+----------------------------+
| Taintgrind_      | a taint analysis tool (based on Memcheck & Flayer)     | Wei Ming Khoo              |
+------------------+--------------------------------------------------------+----------------------------+




.. _ThreadSanitizer: https://code.google.com/p/data-race-test/
.. _Fuzzgrind: http://esec-lab.sogeti.com/pages/fuzzgrind.html
.. _Flayer: https://code.google.com/p/flayer/
.. _Taintgrind: https://github.com/wmkhoo/taintgrind


FAQ
========================================

Why Google's ThreadSanitizer discontinue ?
------------------------------------------

Google's ThreadSanitizer was originally built on top of Valgrind,
its first release was in 2009.
It was based on the algorithm used by Helgrind, and improve some part of the algorithm.
But a newer version changes to become a compile-time utility (both GCC and LLVM).
So, it's working at GCC and LLVM now (by ``-fsanitize=thread``).
You can click here for further information : `Race detection and more with ThreadSanitizer 2 <http://lwn.net/Articles/598486/>`_

How to make Fuzzgrind work ?
------------------------------

(need some try)

Fuzzgrind seems not being maintained ?
It was built with Valgrind 3.4.1 in 2009, not sure whether works with newer Valgrind.

Further information : `Fuzzgrind: an automatic fuzzing tool <http://esec-lab.sogeti.com/static/publications/09-hacklu-fuzzgrind.pdf>`_

How Flayer works ?
------------------------------

Further information : `Flayer: Exposing Application Internals <https://www.usenix.org/legacy/event/woot07/tech/full_papers/drewry/drewry_html/>`_
