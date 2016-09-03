# gctree

The project is to come up with (relatively simple) models of B cell diversification within germinal centers that can be used as part of inference. When we say relatively simple, we mean analogous to the coalescent rather than something like

[Meyer-Hermann, M., Mohr, E., Pelletier, N., Zhang, Y., Victora, G. D., & Toellner, K.-M. (2012). A theory of germinal center B cell selection, division, and exit. Cell Reports, 2(1), 162–174.] (http://doi.org/10.1016/j.celrep.2012.05.010)

The "bright line" dividing the class of models of interest to us are those for which we can compute likelihoods efficiently.

[Paperpile share] (https://paperpile.com/shared/CF07th)  
[Overleaf document] (https://www.overleaf.com/5906733ngwstr)

There's going to be some simulation, validation, etc, with this project. For that we use [nestly] (http://nestly.readthedocs.io/en/latest/).

## Scripts

* TasParse.py - this reads the Tas data excel file, extracts the sequences from lymph node 2 germinal center 1, aligns with muscle, and prints to phyllip format.
* recurse.py - recursion for computing probability of the number of clone leaves and mutant clades for a binary tree with branching prob p and mutation prob q, then using that in an outer recurison level to compute the likelihood of p and q given the entire collapsed tree. Input is breadth-first pairs of comma-separated counts and descendant numbers.



        1
       / \
      1   ^
     /
    4