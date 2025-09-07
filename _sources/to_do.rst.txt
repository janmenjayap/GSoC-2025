.. _to_do:

To Do
-----

1. **Comprehensive improvements to the implementation:**

   - **Extended doctests** covering:

     - best-case scenarios,
     - worst-case time complexity examples, and
     - examples for each method of the class.

   - **Method to collect and report algorithm execution statistics**, including:

     - number of blossoms formed,
     - number of augmenting paths found,
     - number of phases executed,
     - time spent in each phase, etc.

   - **Parallel processing wherever possible** to speed up computation, for example:

     - processing multiple augmenting paths simultaneously, and
     - computing the matching for each connected components of the graph concurrently.

   - **Performance and complexity improvements:**

     - Use a specialized disjoint set union variant to reduce the time to find the :math:`k`-th bud/base of a vertex to :math:`\mathcal{O}(\alpha(m, n))` on RAM models [1]_,
     - Explore and implement further heuristics to optimize the algorithm in practice.

2. **Documentation and comments:**

   - Write detailed comments and documentation for the implementation
   - Provide clear interfaces for:

     - statistics collection,
     - parallel execution features,
     - authors and references, and
     - clear comments using the statements from the original paper [2]_, [3]_.

.. raw:: html

    <hr/>
    <b> References </b>
    <hr/>

.. [1] Harold N. Gabow, Robert Endre Tarjan, *A linear-time algorithm for a special case of disjoint set union.*
       Journal of Computer and System Sciences. Volume 30, Issue 2. 1985. 209-221. ISSN 0022-0000.
       :doi:10.1016/0022-0000(85)90014-5.

.. [2] Michael Huang and Clifford Stein. *Extending Search Phases in the Micali-Vazirani
       Algorithm.* Proceedings of the 16th International Symposium on Experimental Algorithms
       (SEA 2017) (Vol. 75, pp. 10:1–10:19). Dagstuhl, Germany: Schloss Dagstuhl–Leibniz-Zentrum
       für Informatik. :doi:10.4230/LIPIcs.SEA.2017.10. URN urn:nbn:de:0030-drops-76141.

.. [3] Vijay V. Vazirani. *A Proof of the MV Matching Algorithm*. 2020. arXiv preprint,
       arXiv:2012.03582 [cs.DS].

.. raw:: html

    <hr/>