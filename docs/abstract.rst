.. _abstract:

Abstract
--------

.. raw:: html

    <script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
    <hr/>

Matchings and perfect matchings have received considerable attention in graph
theory as well as in other related domains (such as, but not limited to,
algorithms and optimization). There still remain many open problems — such as
`Barnette’s conjecture <https://en.wikipedia.org/wiki/Barnette%27s_conjecture>`_,
`Berge-Fulkerson conjecture <http://garden.irmacs.sfu.ca/op/the_berge_fulkerson_conjecture>`_,
and so on — due to which it continues to remain an active area of research.
At the heart of all this research lies the bottleneck of finding a maximum cardinality
matching in undirected graphs. Edmonds' Blossom algorithm [1]_, introduced in 1965,
was groundbreaking in providing the first polynomial-time solution by effectively
handling odd-length cycles (blossoms) in :math:`\mathcal{O}(|E|\cdot|V|^2)` time.
There are algorithms, with the Linear Programming backbone, that exploit the
properties of the matching polytope for computing a maximum cardinality matching.
For nonbipartite graphs, it either suffers from nontight Linear Programming relaxation,
leading to fractional solutions or otherwise the inclusion of exponential numbers of
the odd-set constraint.

Overtime, there have been several attempts in order to effectively compute the maximum
cardinality matching in general undirected graphs. In 1980, Silvio Micali and Vijay V. Vazirani
presented an algorithm [2]_ that calculates a maximum cardinality matching in
:math:`\mathcal{O}(|E| \cdot \sqrt{V})` time. It is worth noting that the Micali-Vazirani
algorithm, by far, offers the best theoretical runtime known for the concerned problem.
Despite this, there are no publicly available sagemath implementations. It is for this
reason that researchers in this area are at a loss, and are required to implement this
by themselves. Currently, in SageMath, for general undirected graphs, the method
`matching() <https://doc.sagemath.org/html/en/reference/graphs/sage/graphs/graph.html#sage.graphs.graph.Graph.matching>`_,
computes a maximum cardinality matching in :math:`\mathcal{O}(|E|\cdot|V|^2)` either through
Edmonds' algorithm or by using Linear Programming formulation. Ergo, we propose to implement
the :math:`mathcal{O}(|E| \cdot \sqrt{|V|})` Micali-Vazirani algorithm for maximum cardinality
matching in undirected graphs in SageMath, and to make all of that available freely to
students, educators as well as researchers all across the world.

This implementation draws upon the work of Prof. Vazirani [3]_ and the study by Michael Huang
and Clifford Stein [4]_. In addition, a presentation [5]_ delivered by Prof. Vazirani at the Simons
Institute — *A Theory of Alternating Paths and Blossoms, from the Perspective of Minimum Length*
— was consulted to obtain a more comprehensive understanding of the algorithm.

.. raw:: html

    <hr/>
    <b> References </b>
    <hr/>

.. [1] Jack Edmonds. *Paths, Trees, and Flowers*. Canadian Journal of Mathematics.
       Canadian Journal of Mathematics. 17:449–467, 1965. doi:10.4153/CJM-1965-045-4.

.. [2] Silvio Micali and Vijay V. Vazirani. *An \( \mathcal{O}(\sqrt{|V|}\cdot|E|) \)
       algorithm for finding maximum matching in general graphs*. Proceedings of the
       21st Annual Symposium on Foundations of Computer Science (SFCS 1980), 1980. 17–27,
       doi:10.1109/SFCS.1980.12, ISBN 0-8186-1021-4.

.. [3] Vijay V. Vazirani. *A Proof of the MV Matching Algorithm*. 2020. arXiv preprint,
       arXiv:2012.03582 [cs.DS].

.. [4] Michael Huang and Clifford Stein. *Extending Search Phases in the Micali-Vazirani
       Algorithm.* Proceedings of the 16th International Symposium on Experimental Algorithms
       (SEA 2017) (Vol. 75, pp. 10:1–10:19). Dagstuhl, Germany: Schloss Dagstuhl–Leibniz-Zentrum
       für Informatik. :doi:10.4230/LIPIcs.SEA.2017.10. URN urn:nbn:de:0030-drops-76141.

.. [5] Vijay V. Vazirani. *A Theory of Alternating Paths and Blossoms, from the Perspective of
       Minimum Length.* Lecture. Simons Institute for the Theory of Computing. Wednesday,
       October 4, 2023. 02: 00 – 04: 30 PM PT. https://simons.berkeley.edu/events/theory-alternating-paths-blossoms-perspective-minimum-length.

.. raw:: html

    <hr/>